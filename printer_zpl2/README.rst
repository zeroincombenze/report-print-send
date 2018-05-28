[![Build Status](https://travis-ci.org/zeroincombenze/report-print-send.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/report-print-send)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/report-print-send/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/report-print-send?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/report-print-send/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/report-print-send/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/report-print-send/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


















































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

ZPL II Label printing
=====================

This module extends the **Report to printer** (``base_report_to_printer``)
module to add a ZPL II label printing feature.

This module is meant to be used as a base for module development, and does not provide a GUI on its own.
See below for more details.

Installation
------------






Nothing special, just install the module.

Configuration
-------------






To configure this module, you need to:

#. Go to *Settings > Printing > Labels > ZPL II*
#. Create new labels

It's also possible to add a label printing wizard on any model by creating a new *ir.values* record.
For example, to add the printing wizard on the *product.product* model :

.. code-block:: xml

    <record model="ir.values" id="wizard_wizard_print_product_label">
        <field name="name">Print Product Label</field>
        <field name="key">action</field>
        <field name="key2">client_action_multi</field>
        <field name="model">product.product</field>
        <field name="value" eval="'ir.actions.act_window,' + str(ref('printer_zpl2.action_wizard_print_record_label_view'))"/>
    </record>

Usage
-----







=====

To print a label, you need to call use the label printing method from anywhere (other modules, server actions, etc.).

.. code-block:: python

    # Example : Print the label of a product
    self.env['printing.label.zpl2'].browse(label_id).print_label(
        self.env['printing.printer'].browse(printer_id),
        self.env['product.product'].browse(product_id))

You can also use the generic label printing wizard, if added on some models.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/144/10.0

Known issues / Roadmap
----------------------






* Add a button to generate the ir.values for a model
* Develop a "Designer" view in a separate module, to allow drawing labels with simple mouse clicks/drags

Bug Tracker
-----------






Bugs are tracked on `GitHub Issues
<https://github.com/OCA/report-print-send/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us smashing it by providing a detailed and welcomed feedback.

Credits
-------






Images

* Odoo Community Association: `Icon <https://github.com/OCA/maintainer-tools/blob/master/template/module/static/description/icon.svg>`_.






### Contributors






* Sylvain Garancher <sylvain.garancher@syleam.fr>

### Funders

### Maintainer










.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit https://odoo-community.org.

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
