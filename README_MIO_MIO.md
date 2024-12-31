[![Build Status](https://runbot.odoo.com/runbot/badge/flat/1/master.svg)](https://runbot.odoo.com/runbot)
[![Tech Doc](https://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/documentation/17.0)
[![Help](https://img.shields.io/badge/master-help-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/forum/help-1)
[![Nightly Builds](https://img.shields.io/badge/master-nightly-875A7B.svg?style=flat&colorA=8F8F8F)](https://nightly.odoo.com/)

Odoo
----

Odoo is a suite of web based open source business apps.

The main Odoo Apps include an <a href="https://www.odoo.com/page/crm">Open Source CRM</a>,
<a href="https://www.odoo.com/app/website">Website Builder</a>,
<a href="https://www.odoo.com/app/ecommerce">eCommerce</a>,
<a href="https://www.odoo.com/app/inventory">Warehouse Management</a>,
<a href="https://www.odoo.com/app/project">Project Management</a>,
<a href="https://www.odoo.com/app/accounting">Billing &amp; Accounting</a>,
<a href="https://www.odoo.com/app/point-of-sale-shop">Point of Sale</a>,
<a href="https://www.odoo.com/app/employees">Human Resources</a>,
<a href="https://www.odoo.com/app/social-marketing">Marketing</a>,
<a href="https://www.odoo.com/app/manufacturing">Manufacturing</a>,
<a href="https://www.odoo.com/">...</a>

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured <a href="https://www.odoo.com">Open Source ERP</a> when you install several Apps.

Getting started with Odoo
-------------------------

For a standard installation please follow the <a href="https://www.odoo.com/documentation/17.0/administration/install/install.html">Setup instructions</a>
from the documentation.

To learn the software, we recommend the <a href="https://www.odoo.com/slides">Odoo eLearning</a>, or <a href="https://www.odoo.com/page/scale-up-business-game">Scale-up</a>, the <a href="https://www.odoo.com/page/scale-up-business-game">business game</a>. Developers can start with <a href="https://www.odoo.com/documentation/17.0/developer/howtos.html">the developer tutorials</a>


pasos:
=====================>INICIALES<=========================
0.- Descomprimir ProyectoOdoo.rar
0.1 - Cambiar el nombre de la carpeta odoo-17.0+e.20241018 a ProyectoOdooUdemy
0.2 - Entrar a la carpeta ProyectoOdooUdemy y luego a VisualStudioCode
1.- python  -m venv venv
2.- source venv/Scripts/activate 
2.- pip install setuptools wheel
3.- pip install -r requirements.txt
4.- crear un usuario en postgre con todos los privilegios(full privilegios)
    userodo   admin
5.- crear una BASE DE DATOS de nombre: 
    odoodb

    copiar el contenido de : C:\Users\mhernandez.FOSPUCA\Documents\ProyectoOdoo\odoo-bin
    en la raiz del proyecto:
    C:\Users\mhernandez.FOSPUCA\Documents\ProyectoOdoo\odoo-17.0+e.20241018 ( ProyectoOdooUdemy)

    en el archivo odoo.conf, QUE FUE COPIADO DE LA CARPETA odoo-bin cambiar:

       db_user = userodo
       db_password = admin
       db_name = odoodb
       addons_path = C:/Users/mhernandez.FOSPUCA/Documents/ProyectoOdoo/odoo-17.0+e.20241018/odoo/addons
       

6.- ejecutar:
    python odoo-bin.py -r dbuser -w dbpassword --addons-path=addons -d mydb

    este:
    python odoo-bin.py -r userodo -w admin  -d odoodb -i base 
    (-i base), se ejecuta una sola vez, porque es para crear las tablas

    quitamos esto --addons-path=addons, porque ya lo tiene en el path en odoo.conf


========== CUANDO YA ESTE TODO LISTO  ====

7.- Crear el gitignore
    
8.- Activar el ambiente virtual
    source venv/Scripts/activate 

7.- levantar el server.
    python odoo-bin.py -r userodo -w admin -d odoodb 

    http://localhost:8040

documentacion:
https://www.odoo.com/documentation/17.0/es_419/administration/on_premise/source.html

Control de Cambio:
git commit -m "28-12-2024 - Creating the new project"
git commit -m "30-12-2024 - Setting the project"
git commit -m "31-12-2024 - Creating the new module"

requirements.txt
source .venv/Scripts/activate


voy por el modulo 13 de la session 2, Creatin our Module Structure