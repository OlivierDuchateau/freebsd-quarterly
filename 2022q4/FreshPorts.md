## FreshPorts - help wanted ##

Link:	 https://freshports.org/[FreshPorts]
Link:	 https://news.freshports.org/[FreshPorts blog]

Contact: Dan Langille <dan@FreeBSD.org>  

FreshPorts and FreshSource have reported
upon FreeBSD commits for 20 years. They cover all commits,
not just ports.

FreshPorts tracks the commits and extracts data from the
port Makefiles to create a database of information useful
to both port maintainers and port users.

For example, link:https://www.freshports.org/security/acme.sh/[https://www.freshports.org/security/acme.sh/] shows
the history of this port, back to its creation in May 2017.

### Converting the backend repository ###

This topic deals with the FreshPorts code repository. The
front end (website) was converted from subversion to git several
years ago. The back end, which processes FreeBSD commits and
updates the database, is still on subversion. I have
wanted to convert these repositories to git for some time.

I would like help with this please. I'll give you a copy of the 
repositories and you give me back several git repos (one for each).
They will be uploaded to link:https://github.com/FreshPorts[https://github.com/FreshPorts] (our project
on GitHub).

These are the existing subversion repos:

* ingress (code for the back end)
* database schema
* backend - monitoring code
* packaging - scripts for cutting new tarballs - deprecated via git
* daemontools - now misnamed, because the scripts use daemon(8)
* periodics - scripts started by periodic(8)
* ports - for the FreeBSD packages which install the above

### I won't be running FreshPorts forever ###

It's been over 22 years and I know others must take over eventually.
I'd like to start that process now. There are several aspects to
FreshPorts:

* FreeBSD admin (updating the OS and packages)
* front end code (website - mostly PHP)
* back end code (commit processing - perl, python, shell)
* database design (PostgreSQL)

The database does not change very often and requires little maintenance
compared to the applications and OS. The website pretty much runs itself.
From time to time, a change to the FreeBSD ports infrastructure breaks
something or requires a modification, but there is rarely any urgency
to fix that. This is not a huge time commitment. There is a lot of
learning. While not a complex application, FreshPorts is also not
trivial.

