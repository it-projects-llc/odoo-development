====================
 Docs and manifests
====================

Files
=====

**All** files from this section ought to be fully [*]_ prepared **before** any other files in new module. It helps you to review requirements again before you start.


.. toctree::
   :maxdepth: 1

   README.rst.rst           
   usage-instructions
   __manifest__.py
   changelog.rst.rst
   icon.png.rst

Notes
=====

.. toctree::
   :maxdepth: 2

   rst-requirements           
   doc-files-understanding

Template handling
=================

Download templates:

.. code-block:: sh

    cd PATH/TO/MODULE-ROOT/

    # __manifest__.py
    wget https://raw.githubusercontent.com/it-projects-llc/odoo-development/master/docs/dev/docs/templates/__manifest__.py
    # __README__.rst
    wget https://raw.githubusercontent.com/it-projects-llc/odoo-development/master/docs/dev/docs/templates/__manifest__.py
    mkdir doc
    cd doc
    # doc/index.rst
    wget https://raw.githubusercontent.com/it-projects-llc/odoo-development/master/docs/dev/docs/templates/doc/index.rst
    # doc/changelog.rst
    wget https://raw.githubusercontent.com/it-projects-llc/odoo-development/master/docs/dev/docs/templates/doc/changelog.rst
    cd ..
    #

Update templates:

.. code-block:: sh

    # SETTINGS
    # {braces} AND text inside them must be replaced to appropriate value (without braces)

    # set your name
    # you can add it to to your ~/.bashrc, e.g.
    # export DEVELOPER_NAME="Ivan Yelizariev"
    # export DEVELOPER_GITHUB_USERNAME=yelizariev
    DEVELOPER_NAME="{Ivan Yelizariev}"
    DEVELOPER_GITHUB_USERNAME={yelizariev}

    # this command returns name of current folder, so you MUST be at module's root
    TECHNICAL_NAME=`basename $PWD`

    # to get commit sha use following inside odoo repo: "git show HEAD | head" 
    ODOO_REVISION={ODOO_COMMIT_SHA_TO_BE_UPDATED}

    # module description
    MODULE_NAME="{SOME Non-technical name}"
    MODULE_SUMMARY="{SHORT module description for REAMDE and manifest}"

    # Repository: choose one of the options
    REPO_NAME=access-addons
    REPO_NAME=l10n-addons
    REPO_NAME=mail-addons
    REPO_NAME=misc-addons
    REPO_NAME=odoo-saas-tools
    REPO_NAME=odoo-telegram
    REPO_NAME=pos-addons
    REPO_NAME=website-addons

    # Branch: choose one of the options
    ODOO_BRANCH=11.0
    ODOO_BRANCH=10.0
    ODOO_BRANCH=9.0
    ODOO_BRANCH=8.0

    # Category: shoose one of the options
    MODULE_CATEGORY="Accounting"
    MODULE_CATEGORY="Discuss"
    MODULE_CATEGORY="Document Management"
    MODULE_CATEGORY="eCommerce"
    MODULE_CATEGORY="Human Resources"
    MODULE_CATEGORY="Industries"
    MODULE_CATEGORY="Localization"
    MODULE_CATEGORY="Manufacturing"
    MODULE_CATEGORY="Marketing"
    MODULE_CATEGORY="Point of Sale"
    MODULE_CATEGORY="Productivity"
    MODULE_CATEGORY="Project"
    MODULE_CATEGORY="Purchases"
    MODULE_CATEGORY="Sales"
    MODULE_CATEGORY="Warehouse"
    MODULE_CATEGORY="Website"
    MODULE_CATEGORY="Extra Tools"

    # icon: choose one of options
    ICON=access
    ICON=barcode
    ICON=mail
    ICON=misc
    ICON=pos
    ICON=saas
    ICON=stock
    ICON=telegram
    ICON=website
    ICON=website_sale

    # EXECUTING
    mkdir -p static/description
    # static/description/icon.png
    wget https://raw.githubusercontent.com/it-projects-llc/odoo-development/master/docs/images/module-icons/${ICON}/icon.png -o static/description/icon.png

    sed -i "s/{MODULE_NAME}/${MODULE_NAME}/g" __manifest__.py README.rst doc/index.rst
    sed -i "s/{Put some short introduction first.}/${MODULE_SUMMARY}/g" README.rst
    sed -i "s/{SHORT_DESCRIPTION_OF_THE_MODULE}/${MODULE_SUMMARY}/g" __manifest__.py
    sed -i "s/{MODULE_CATEGORY}/${MODULE_CATEGORY}/g" __manifest__.py
    sed -i "s/{DEVELOPER_NAME}/${DEVELOPER_NAME}/g" __manifest__.py README.rst doc/index.rst
    sed -i "s/{DEVELOPER_GITHUB_USERNAME}/${DEVELOPER_GITHUB_USERNAME}/g" __manifest__.py README.rst doc/index.rst
    sed -i "s/{REPO_NAME}/${REPO_NAME}/g" README.rst
    sed -i "s/{BRANCH}/${ODOO_BRANCH}/g" README.rst
    sed -i "s/{TECHNICAL_NAME}/${TECHNICAL_NAME}/g" README.rst
    sed -i "s/{VERSION}/${ODOO_BRANCH}/g" README.rst
    sed -i "s/{ODOO_COMMIT_SHA_TO_BE_UPDATED}/${ODOO_REVISION}/g" README.rst



.. [*] The only exception could be made for lists of files in ``__manifest__.py`` (*"data"*, *"qweb"*, *"demo"* fields).
