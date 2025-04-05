## Coding Conventions

Links:

* "PEP 8 – Style Guide for Python Code" https://peps.python.org/pep-0008/ or https://pep8.org/
* "PEP 257 – Docstring Conventions" https://peps.python.org/pep-0257/
* "Google Python Style Guide" https://google.github.io/styleguide/pyguide.html
* "Code Style" from "The Hitchhiker’s Guide to Python!" https://docs.python-guide.org/writing/style/

**:warning: Warning: The following is a big mess ...**

### :heavy_check_mark: Tabs or Spaces

Use spaces, avoid tabs.

### :heavy_check_mark: Blank Lines

Surround top-level function and class definitions with two blank lines.

### :heavy_check_mark: Source File Encoding

Code should always use UTF-8, and should not have an encoding declaration.

All identifiers use ASCII-only identifiers, and SHOULD use English words wherever feasible.

### :question: Imports

* Imports should usually be on separate lines
* Imports are always put at the top of the file, just after any module comments

TODO:
import mypkg.sibling
vs.
from mypkg import sibling

### :construction: Comments

Comments should be complete sentences. The first word should be capitalized, unless it is an identifier that begins with a lower case letter.

### :heavy_check_mark: Class Names

Class names should use the CamelCase convention.

### :question: global variables

### :construction: Function and Variable Names

Function names should be lowercase, with words separated by underscores as necessary to improve readability.

Variable names follow the same convention as function names.

### :construction: Method Names and Instance Variables

Use the function naming rules: lowercase with words separated by underscores as necessary to improve readability.

### :construction: Constants

Constants are usually defined on a module level and written in all capital letters with underscores separating words. Examples include MAX_OVERFLOW and TOTAL.
