# Forge

Which source code forge (aka: "git server") to use for my small homelab in 2025?

## Motivation

For years I'm using two places to store my git repositories:

* public stuff: [GitHub.com](https://github.com/)
* private stuff: plain ssh to my self hosted file server

Using plain ssh works nicely in a single user scenario, but it lacks some comfort compared to GitHub.

Thought it was time to improve this ...

## Plain ssh, gitea, Forgejo, GitLab, GitHub or what?

What is the best for my self hosted private git stuff?

My criteria:

* open source
* used by me (only single user needed)
* about 10 git repos to host
* an overview of the repositories and such comfort
* self hosted local server (I'll use GitHub.com for public stuff)
* runs in a container (no complicated server installation please)
* "reasonable" resource usage on the server
* maybe add a test runner later
* no fancy CI/CD features like code scanners needed

There is a longer list of possible source code forges at: https://en.wikipedia.org/wiki/Forge_(software)#Examples

The notable alternatives I had a look at ...

### Plain ssh

For years, I'm using plain ssh access to my local server without any special git server SW. To do this, I use an URL like:

```
ulfl@server.lan:/data/system/git/abc
```

As a single user this works nicely, don't know how well this works in multi user scenarios.

Compared to GitHub, this local "ssh only" access feels pretty bare bone now.

### gitea

* runs locally in a container
* Web-UI with a repository overview and more
* low (container) resource usage
* test runner possible (e.g. in another container)
* switched to a freemium model in 2022, now company driven
* open source core with "paid enterprise features"

I'm unsure if important features will be "enterprise only" in the future. As I don't need "fancy groupware" features, I'll probably be ok even with a limited future core functionality.

### Forgejo

* hard fork of gitea, so similar feature set
* open source, community driven

I like the idea of a community driven open source project and dislike the switch of gitea to a commercial company.

However, the future pace of forgejo is unclear to me. What drove me away is the - for me - confusing documentation and reading some mailing list discussions.

### GitLab

* more capable than gitea
* (much?) higher resource usage than gitea

Much higher resource usage drove me away from GitLab, I haven't even tried GitLab.

### GitHub

* Not open source!
* No simple local (container) setup available
* I'll use it only for public stuff on GitHub.com

### Conclusion

* GiHub can't be used in the homelab
* GitLab seems to be too resource hungry for my small home server
* plain ssh lacks some comfort
* Forgejo's future is unclear to me
* gitea seems to be the way to go for me

Thought I'll give gitea a try. Forgejo might be a future alternative if gitea is crippled down too much ...

More at: [gitea.md](gitea.md)
