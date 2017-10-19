==================
 RST Requirements
==================

Don't forget to keep correct rst format.

.. contents::
   :local:
   :depth: 1

Extra lines
===========

Dont' forget about additional lines for correct formatting

Raw RST
-------
::

    This and next sentences are joined together.
    To split sentences to paragraphs you must add add empty line.

    Splited sentence 1.

    Splited sentence 2.

    Lists below doesn't rendered correctly, because extra line is required:
    * 1
    * 2
    * 3

    The same for sublist:

    * 1
      * 1.1
      * 1.2
      * 1.3
    * 2

    Correctly formated lists:

    * 1
    * 2
    * 3

      * 3.1
      * 3.2
      * 3.3

    * 4

Rendered RST
------------

This and next sentences are joined together.
To split sentences to paragraphs you must add add empty line.

Splited sentence 1.

Splited sentence 2.

Lists below doesn't rendered correctly, because extra line is required:
* 1
* 2
* 3

The same for sublist:

* 1
  * 1.1
  * 1.2
  * 1.3
* 2

Correctly formated lists:

* 1
* 2
* 3

  * 3.1
  * 3.2
  * 3.3

* 4


References to menu
==================

Use double back-quotes with **spaced** slash for menus: ::

    OK:
    * Open menu ``Settings >> Parameters >> System Parameters``

    BAD
    * Open menu ``Settings>>Parameters>>System Parameters``
    * Open menu "Settings >> Parameters >> System Parameters"
    * Open menu ''Settings >> Parameters >> System Parameters''
    * Open menu ``Settings > Parameters > System Parameters``

Fields
======

Use bold format for fields::

    * Set **Name** and **Date** values

Checkboxes
==========

Same as Fields but draw box (with mark or without), e.g.::

    * Set  **[x] Use Longpooling**
    * Switch **[ ] Use Longpooling** off

Buttons
=======
Use square brackets in double back-quotes to name buttons. Keep letter cases the same as in UI. ::

    OK:
    * click ``[Save]``

    Bad:
    * click ``[save]``

Selections
==========

Use arrow symbol ``->`` to specify value in selection and many2one fields: ::

  * Choose ``Partner -> Administrator``


Titles and sections
===================

.. code-block:: rst

    OK:
    ===========================
     Correctly formatted Title
    ===========================

    Correctly formatted section
    ===========================

    BAD:
    ===========================================
    No spaces at the beggining and end of title
    ===========================================

    =============================
     No space at the end of title
    =============================

    =======================================
    Incorrect number of signs in title
    ========================================

    ================
    Incorrect number of signs in title
    ================

    Incorrect number of signs in section
    =====================================

    Incorrect number of signs in section
    ===================================

