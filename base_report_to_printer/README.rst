[![Build Status](https://travis-ci.org/zeroincombenze/report-print-send.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/report-print-send)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/report-print-send/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/report-print-send?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/report-print-send/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/report-print-send/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/report-print-send/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)
































































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Report to printer
=================
This module allows users to send reports to a printer attached to the server.


It adds an optional behaviour on reports to send it directly to a printer.

* `Send to Client` is the default behaviour providing you a downloadable PDF
* `Send to Printer` prints the report on selected printer

Report behaviour is defined by settings.


Settings can be configured:

* globaly
* per user
* per report
* per user and report


After installing enable the "Printing / Print Operator" option under access
rights to give users the ability to view the print menu.


To show all available printers for your server, use the
`Settings/Configuration/Printing/Update Printers from CUPS` wizard.


Then go to the user profile and set the users printing action and default
printer.

Caveat

The notification when a report is sent to a printer will not be
displayed for the deprecated report types (RML, Webkit, ...).

Dependencies

This module requires pycups
https://pypi.python.org/pypi/pycups


Installation
------------




Configuration
-------------




Usage
-----







Known issues / Roadmap
----------------------




Bug Tracker
-----------




Credits
-------








### Contributors





* Ferran Pegueroles <ferran@pegueroles.com>
* Albert Cervera i Areny <albert@nan-tic.com>
* Davide Corio <davide.corio@agilebg.com>
* Lorenzo Battistini <lorenzo.battistini@agilebg.com>
* Yannick Vaucher <yannick.vaucher@camptocamp.com>
* Lionel Sausin <ls@numerigraphe.com>
* Guewen Baconnier <guewen.baconnier@camptocamp.com>

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on its own cloud infrastructure.
[Zeroincombenze® distribution](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Everytime, every Odoo DB and customized code can be deployed on local server too.

[//]: # (end copyright)

[//]: # (addons)

[//]: # (end addons)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
