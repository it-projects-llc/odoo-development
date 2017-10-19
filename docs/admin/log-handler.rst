===================
 ``--log-handler``
===================

::

   --log-handler=PREFIX:LEVEL

Setups a handler at LEVEL for a given PREFIX. This option can be repeated. 

For example, if you want to have DEBUG level for module `telegram <https://github.com/it-projects-llc/odoo-telegram/tree/9.0/telegram>`_ only, you can run it with parameter::

   --log-handler=odoo.addons.telegram:DEBUG

To disable werkzeug logs add following parameter::

   --log-handler=werkzeug:CRITICAL

Log levels
==========

* CRITICAL
* ERROR
* WARNING
* INFO
* DEBUG
* NOTSET
