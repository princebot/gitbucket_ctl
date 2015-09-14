# gitbucket_ctl
super-convenient init-style commands and logging for the ever-awesome **[GitBucket Server](https://github.com/takezoe/gitbucket)**

### Quickstart

```
gitbucket help|install|restart|uninstall|upgrade

gitbucket start [[host=HOST] [port=PORT] [data=DIRECTORY]]

gitbucket stop [PID [PID...]]

gitbucket status [PID [PID...]]
```

1. `git clone https://github.com/princebot/gitbucket_ctl.git && cd gitbucket_ctl`
2. `./gitbucket install && ./gitbucket start`
3. There is no step three—you now have a GitBucket Server instance running on http://localhost:8080 that you can log into using uid->root/pw->root. Going forward, **gitbucket** will be in $PATH, so you can call it without prepending ./. Man page is accessed via `gitbucket help`.

### About

**gitbucket**  is  a  management  utility  that adds easy command-line management to **[GitBucket Server](https://github.com/takezoe/gitbucket)**, enabling you to quickly stop and start GitBucket
Server, get information on running instances, and install, uninstall, or update GitBucket Server with short init-style commands. Additionally, gitbucket wraps GitBucket Server with simple logging and log rotation.

**GitBucket  Server** is an awesome GitHub-clone that’s dead-simple to use --- no database set-up, no web-server
configuration, just a single .WAR file you can run directly using command-line arguments. I made this **control script** for my own use-case: I often want to share code in a quick-and-dirty way, but on internal networks rather than cloud-based codesharing sites. And GitBucket Server works great for that using this utility:

* **gitbucket install && gitbucket start** (if the server is not installed), *or*
* **gitbucket start** (if you already have it)

And that's pretty much it: gitbucket makes an already user-friendly application absurdly simple to use.

For more info, git-clone **gitbucket** and check out the man page.

Enjoy!
