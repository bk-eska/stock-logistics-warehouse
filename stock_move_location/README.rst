===================
Move Stock Location
===================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:1bbc0d0f6cd9c8298d132633b14522ed340f1f669c6fec8170f9f5347c3138e5
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fstock--logistics--warehouse-lightgray.png?logo=github
    :target: https://github.com/OCA/stock-logistics-warehouse/tree/16.0/stock_move_location
    :alt: OCA/stock-logistics-warehouse
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/stock-logistics-warehouse-16-0/stock-logistics-warehouse-16-0-stock_move_location
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/stock-logistics-warehouse&target_branch=16.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module allows to move entire location of products from one place to
another and move only selected quantities.

**Table of contents**

.. contents::
   :local:

Usage
=====

-  A new menu item Operations > Move from location... opens a wizard
   where 2 locations can be specified.
-  Select origin and destination locations and press "IMMEDIATE
   TRANSFER" or "PLANNED TRANSFER"
-  Press ADD ALL button to add all products available
-  Those lines can be edited. Move quantity can't be more than a max
   available quantity
-  Move doesn't care about the reservations and will move stuff anyway
-  If during your operation with the wizard the real quantity will
   change it will move only the available quantity at the button press
-  Products will be moved and a form view of picking that did that will
   show up
-  If "PLANNED TRANSFER" is used - the picking won't be validated
   automatically

If you want to transfer a full quant:

-  Go to Inventory > Products > Products and click "On hand" smart
   button or Inventory > Reporting > Inventory, the quants view will be
   opened.
-  Select the quantities which you want move to another location

If you go to the Inventory Dashboard you can see the button "Move from
location" in each of the picking types (only applicable to internal
transfers). Press it and you will be directed to the wizard.

|image1|

To enable this option, check "Show Move On Hand Stock" in the Picking
Type configuration.

|image2|

If you want transfer everything from stock.location

On a draft picking, add a button to fill with moves lines for all
products in the source destination. This allows to create a picking to
move all the content of a location. The Origin Location must have stock.
The Destination Location has to be a final location. If some quants are
not available (i.e. reserved) the picking will be in partially available
state and reserved moves won't be listed in the operations. Use barcode
interface to scan a location and create an empty picking. Then use the
fill with stock button.

.. |image1| image:: https://user-images.githubusercontent.com/147538094/281480833-208ea309-0bad-43e7-bd6f-8384520afe00.png
.. |image2| image:: https://user-images.githubusercontent.com/147538094/281479487-45fa4bde-36be-4ba1-8d54-8e707b89459e.png

Known issues / Roadmap
======================

Change the current implementation (suggested by Denis Roussel from
ACSONE):

-  A new parameter on stock picking types : 'Product Change Location'
   (with a little help).
-  With this, go to the dashboard, create a picking with that type.
-  Add a button on the picking form which is visible with that type that
   fill in the picking as now
-  Nice to have: add a magic button on locations that with context
   creates a new picking of that type with the origin location already
   filled in.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/stock-logistics-warehouse/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/stock-logistics-warehouse/issues/new?body=module:%20stock_move_location%0Aversion:%2016.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
-------

* Julius Network Solutions
* BCIM
* Camptocamp

Contributors
------------

-  Mathieu Vatel <mathieu@julius.fr>
-  Mykhailo Panarin <m.panarin@mobilunity.com>
-  Joan Sisquella <joan.sisquella@forgeflow.com>
-  Jordi Ballester Alomar <jordi.ballester@forgeflow.com>
-  Lois Rilo <lois.rilo@forgeflow.com>
-  Héctor Villarreal <hector.villarreal@forgeflow.com>
-  Tecnativa <tecnativa.com>

   -  Sergio Teruel
   -  João Marques

-  Jacques-Etienne Baudoux <je@bcim.be>
-  Iryna Vyshnevska <i.vyshnevska@mobilunity.com>
-  Alexei Rivera <arivera@archeti.com>
-  Abraham Anes <abraham@studio73.es>
-  Quartile <https://www.quartile.co>

   -  Aung Ko Ko Lin

Maintainers
-----------

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/stock-logistics-warehouse <https://github.com/OCA/stock-logistics-warehouse/tree/16.0/stock_move_location>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
