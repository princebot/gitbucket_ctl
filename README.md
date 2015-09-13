# gitbucket_ctl
Management utility for the wonderful gitbucket project, reminiscent of init scripts

### Quickstart

* Clone this project
* Run `gitbucket install`
* Run `gitbucket start`


### About

**gitbucket** [https://github.com/takezoe/gitbucket] is an awesome self-hosted GitHub clone. Unlike others, it's dead-simple to set up: no database configuring, no web-server management---it's all just a single .WAR file that you run.

It's well-documented for using in production environments. However, my use case is different: I like it as a quick-and-dirty way to share code at work or other environments where posting it to one of the many cloud-hosted code-sharing sites would be inappropriate. And gitbucket couldn't be simpler for this.

However, it didn't have a management utility. It can integrate with OS X's `launchctl`, but lacked a simple / direct way to do it ad-hoc.

So I made this **gitbucket control script**. It can install, remove, start, stop, report status---basically, anything you'd expect from a SysV style `service PROG start|stop|reload|etc` script.

This is still a work in progress---posted it just to share with some friends. Needs help strings and refactoring, as well as more testing.
### Usage

```
gitbucket help
gitbucket start|stop|status|restart
gitbucket instaall|uninstall|upgrade
```

By default, `gitbucket start` spins up a gitbucket instance on localhost at port 8080, default credentials root/root.

You can, however, pass options to `gitbucket start` like so:
```
gitbucket start host=HOST port=PORT home=GITBUCKET-DATA-DIRECTORY
```

### TODO

* ~~Fix color-display bug on OS X systems~~
* Add man page
* Refactor / organize code
* Add docstrings for functions
* Add code comments
* Test on more operating systems (CentOS and OS X tested so far)
