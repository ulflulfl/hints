# Python cheat

Some Python hints for myself as a Python novice. Especially differences to C/C#/Java ...

See: [Coding Conventions](python-coding-conventions.md) for a big mess ...

## Table of Contents

* **[Data Types](#data-types)**
  * [Types and Casting](#types-and-casting)
  * [Global](#global)
  * [Strings](#strings)
  * [Lists](#lists-arrays)
  * [Dictionaries](#dictionaries)
* **[Control Flow](#control-flow)**
  * [if](#if)
  * [switch](#switch-matchcase)
  * [Exceptions](#exceptions)
  * [Terminate Program](#terminate-program)
* **[Files and Folders](#files-and-folders)**
  * [Infos](#infos)
  * [Current Dir](#current-dir)
  * [Iterate](#iterate)
  * [Manipulate](#manipulate)
  * [Input / Output](#input--output)
* **[System](#system)**
  * [Sleep](#sleep)
  * [Read environment variable](#read-environment)
  * [Machine name](#machine-name)
  * [Check for Running Debugger](#check-for-running-debugger)
* **[Console](#console)**
  * [Console Output](#console-output)
  * [Console Input](#console-input)
  * [Set Console Title](#set-console-title)
  * [Set Console Colors](#set-console-colors)
* **[Web](#web)**
* **[Open Office (pandas)](#open-office-pandas)**
  * [Install pandas](#install-pandas)
  * [Iterate Rows](#iterate-rows)
* **[External Processes](#external-processes)**
  * [Process Execution](#process-execution)
  * [Process Manipulation (psutils)](#process-manipulation-psutils)

---

## Data Types

### Types and Casting

```
x = "3"
y = 3
z = 3.0

x = str(3)
y = int(3)
z = float(3)

print(type(x))
```

### Global

```
def func():
    global a
    a = "fantastic"

func()
print("Global: " + a)
```

### Strings

Various methods: https://www.w3schools.com/python/python_strings_methods.asp

#### Creation

```
r"C:\abc"
f"text with {variable}"
f"text with {variable:.2f}"		# two decimals of a float
fr"C:\text\{variable}"
```

* r: text ignoring escape chars (especially for Windows paths)
* f: format variable content into the string

Links:

* Escape chars: https://www.w3schools.com/python/python_strings_escape.asp
* Formatting: https://www.w3schools.com/python/python_string_formatting.asp

#### Checks

Contains and StartsWith:

```
if "string" in myString:
    ...

if myString.startswith(prefix):
    ...
```

#### Split

```
for line in textBlob:
    print(line)

text[1:3] # including 1, excluding 3
text[:4]  # from start, excluding 4
text[4:]  # including 4 to the end

text = "a, b"
print(a.split(",")) 	# returns ['a', ' b']
```

#### Changes

```
text.upper()
text.lower()
text.strip()	# remove leading and trailing spaces
text.replace("a", "b")
```

### Lists (Arrays)

```
some_names = [
    "Alice",
    "Bob",
]

list_in_list = [
    ["Alice", "Merton"],
    ["Bob", "Hope"],
]

alice = some_names[0]
n = len(some_names)
for name in some_names:
    print(name)
some_names.pop(0) # removes first item
some_names.remove("Alice")
```
Other list/array actions: https://www.w3schools.com/python/python_arrays.asp

### Dictionaries

Key:Value store.

```
person = {
    "first": "Alice",
    "name": "Merton",
    "year": 1993
}
person = dict(first = "Alice", name = "Merton", year = 1993)

print(person)
print(person["name"])
print(len(person))
```

https://www.w3schools.com/python/python_dictionaries.asp

---

## Control Flow

### if

```
if a==b and not c==d or e!=f:
    print(a)
elif not a==b:
    print(b)
else:
    print(c)
```

### switch (match/case)

```
match variable:
    case "a" | "b":
        # do a
    case _:
        # default
```

### return

```
return a, b, c
```

### Exceptions

```
try:
    # action
except PermissionError:
    # reaction
except OSError as error:
    if error.errno == 41:
        # more ...
except Exception as error:
    # more ...
```

### Terminate Program

```
exit(1)
```

Unfortunately, there is no exit code standard ...
https://stackoverflow.com/questions/1101957/are-there-any-standard-exit-status-codes-in-linux

Maybe some common ones:

* 0: ok
* 1: general error
* 2: command line usage error
* x: other failure ...

---

## Files and Folders

```
import os
```

### Infos

```
os.path.exists(dirOrFile)
os.path.isdir(dir)
os.path.isfile(file)
os.path.getsize(file)

joinedPath = os.path.join(dir, file)
extension = os.path.splitext(file)[1]
```

### Current Dir

```
cwd = os.getcwd()
os.chdir(dir)
```

### Iterate

```
for dirsAndFiles in os.listdir(dir):
    ...
```

### Manipulate

```
os.makedirs(dir)
os.remove(file)
os.rmdir(dir)
```

### Input / Output

```
with open("infile.txt", 'r', encoding='utf8') as infile:
    with open("outfile.txt", 'w', encoding='utf8') as outfile:
        while line := infile.readline():
            outfile.write("pre-" + line + "\n")
```

File modes: https://www.w3schools.com/python/python_file_handling.asp

---

## System

### Sleep

```
import time
time.sleep(100/1000)    # sleep 100 ms
```

### Read environment variable

```
import os
userprofile = os.environ['USERPROFILE']
```

### machine name

```
import platform
name = platform.node()
```

### Check for running debugger

Not perfect, will probably only work with VS Code:

```
isDebuggerRunning = os.environ.get('DEBUGPY_RUNNING') == "true"
```

---

## Console

### Console Output

```
print("\rtext", end='', flush=True)
```

* \r "carriage return" will point cursor at the start of the console line
* end='' avoids a newline (console won't jump to the next line)
* flush=True prints out immediately on (Windows) console (as end='' causes the output to be buffered and not shown immediately)

### Console Input

Wait for "enter key" pressed:

```
text = input("Enter a text:")
```

Wait for single "any key" press (Windows only, there seems to be no easy portable way)

```
import msvcrt
selected = msvcrt.getch().decode('ASCII')
```

### Set Console Title

Set the title of the console window:

```
system("title " + title)
```

### Set Console Colors

https://stackoverflow.com/questions/287871/how-do-i-print-colored-text-to-the-terminal

```
CRED = '\33[31m'
CGREEN = '\33[32m'
CBLUE = '\33[34m'
CEND = '\33[0m'
print(CRED + "red" + CEND)
print(CGREEN + "green" + CEND)
print(CBLUE + "blue" + CEND)
```

---

## Web

```
import urllib.request
urllib.request.urlopen("url").read()
```

---

## Open Office (pandas)

Use pandas for handling of data e.g. in LibreOffice .ods files.

https://www.w3schools.com/python/pandas/default.asp

### Install pandas

```
pip install pandas
```

TODO: use venv

### Iterate rows

```
import pandas as pd

df = pd.read_excel("test.ods", "sheet", engine="odf")
print(df)
for index, row in df.iterrows():
    contentFromCell = str(row["Column Header"])
```

---

## External Processes

### Process Execution

```
import subprocess
```

#### Simple Execution

```
command = "doit parameter"
result = subprocess.run(command, stdout=sys.stdout)
returned = result.returncode
```

#### Output to String

```
command = "choco outdated"
result = subprocess.run(command.split(), capture_output=True, text=True)
returned = result.returncode
for line in result.stdout.splitlines():
    ...
```

#### Output to File

```
command = f"choco list -lo -r -y"
with open("output.txt", 'w', encoding='utf8') as outfile:
    subprocess.run(command, stdout=outfile, stderr=subprocess.STDOUT)
```

### Process Manipulation (psutils)

Platform independent process handling.

#### Install psutils

```
pip install psutil
```

TODO: use venv

#### Search for Process

```
for proc in psutil.process_iter(attrs=['pid', 'name']):
    if proc.info['name'] == "explorer.exe":
        ...
```

#### Terminate Process

```
proc.terminate()
proc.kill()
```

Terminate is gracefully shutdown, kill is hard kill.
