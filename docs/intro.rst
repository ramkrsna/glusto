.. _introduction:

Glusto is a framework designed to provide features commonly used in a
remote/distributed environment via a single and easy-to-access object.

It started out as a port of some shell ssh functions I had written
and was meant for use in PyUnit* tests and config scripts for Gluster.

I've removed the Gluster specifics from this package. Feel free to give it a
go, and please let me know how it works out.

Some of the key concepts and features of Glusto:

* Glusto inherits from multiple classes providing configuration (yaml, json, ini), remote connection (SSH, SCP, RPyC), ANSI color output, logging, and unit test functionality (PyUnit, PyTest, Nose)--presenting them in a single global Class object.

* Glusto also acts as a global class for maintaining state and configuration data across multiple modules and classes.

* Glusto provides a wrapper utility (``/usr/bin/glusto``) to help make configuration files available to test cases from the command-line.

Adding Glusto utilities to a Python module is as simple as an import.

Example:
    To use Glusto in a module::

        from glusto.core import Glusto as g

.. note:: It is no longer necessary to say "Glusto Importo!" out loud
   before executing scripts using the Glusto module. The import statement is
   more than sufficient.
