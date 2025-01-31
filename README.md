Abstract/Features
================================================================================

Pysilhouette is a 100% pure Python daemon which executes background job commands
queued in database. It is mainly used for web application to execute background tasks.

Install
================================================================================

See 'INSTALL'.


License/Copying
================================================================================

Copyright (c) 2009-2012 HDE, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


Packages Pysilhouette depends on
================================================================================

* python >= 2.7
* SQLAlchemy = 1.4


Directory Structure
================================================================================

```
|-- AUTHORS
|-- ChangeLog
|-- INSTALL
|-- INSTALL.ja
|-- LICENSE
|-- MANIFEST.in # for distutils packaging
|-- README
|-- README.ja # Japanese version of this file.
|-- debian
|   |-- README.Debian
|   |-- changelog
|   |-- compat
|   |-- control
|   |-- copyright
|   |-- dirs
|   |-- docs
|   |-- performerd.init
|   |-- postinst
|   |-- postrm
|   |-- preinst
|   |-- prerm
|   |-- pycompat
|   |-- rules
|   |-- schedulerd.init
|   |-- silhouetted.default
|   `-- silhouetted.init
|-- doc
|   `-- epydoc.cfg # Configuration file for epydoc
|-- sample # Sample programs using pysilhouette.
|   |-- log.conf.example # Example config file for logging function.
|   |-- rc.d
|   |   `-- init.d
|   |       |-- asynperformerd # init script for the asynperformer daemon
|   |       |-- asynschedulerd # init script for the asynschedulerd daemon
|   |       |-- performerd # init script for the performer daemon
|   |       |-- schedulerd # init script for the scheduler daemon
|   |       `-- silhouetted # init script for the watch daemon
|   |-- redhat.spec # Spec file for RPM building.
|   |-- scripts
|   |   |-- dummy.py
|   |   |-- insert_dummy.py
|   |   |-- sendmail.py
|   |   |-- test_failure.py
|   |   `-- test_success.py
|   |-- silhouette.conf.example # Example config file for Pysilhouette
|   |-- sysconfig
|   |   `-- silhouetted
|   `-- whitelist.conf.example # Example config file for whitelist function
|-- pysilhouette
|   |-- __init__.py
|   |-- asynperformer.py
|   |-- asynscheduler.py
|   |-- command.py
|   |-- daemon.py # Daemonizing function.
|   |-- db # Database related files.
|   |   |-- __init__.py
|   |   |-- access.py # Database operation.
|   |   |-- model.py # Database table model.
|   |-- er.py
|   |-- log.py
|   |-- performer.py # Performer daemon (executes job commands)
|   |-- prep.py # Initialize functions.
|   |-- scheduler.py # Scheduler daemon (schedules job command executions)
|   |-- silhouette.py # Watch daemon (watched performer/scheduler daemons)
|   |-- tests # Testing related files.
|   |   |-- __init__.py
|   |   |-- suite.py
|   |   |-- testprep.py
|   |   |-- testutil.py
|   |   `-- testworker.py
|   |-- uniqkey.py # Unique key for the instance.
|   |-- util.py
|   `-- worker.py
|-- setup.cfg # Configuration for distutils packaging.
|-- setup.py # Main command for distutils packaging.
`-- tools # Tools for development/operation.
    |-- epydoc.sh
    |-- psil-cleandb
    |-- psil-set
    `-- sqlite2other.py
```

Acknowledgment
================================================================================
SQLAlchemy people.
HDE, Inc. and other related members.
All people in Python community.
