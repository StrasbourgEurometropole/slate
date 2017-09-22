---
title: Strasbourg.eu - Référence de l'API

language_tabs:
  - shell

toc_footers:
  - <a href='https://www.strasbourg.eu'>Strasbourg.eu</a>
  - <a href='https://github.com/tripit/slate'>Documentation générée par Slate</a>

includes:
 - events/title
 - events/all
 - events/get
 - events/by-date
 - events/by-category
 - events/by-place
 - events/by-locale
 - events/themes
 - events/types
 - events/publics

 - places/title
 - places/get
 - places/by-sig
 - places/by-type
 - places/by-territory
 - places/by-territory-and-type
 - places/by-name
 
 - interests/title
 - interests/get
 - interests/user-interests
 - interests/update-user-interests

 - favorites/title
 - favorites/types
 - favorites/get
 - favorites/add
 - favorites/delete
 
 - notifications/title
 - notifications/types
 - notifications/channels
 - notifications/settings
 - notifications/set-settings
 - notifications/get
 - notifications/add

 - categories/title
 - categories/territories
 - categories/services

search: true
---

# Introduction

Bienvenue sur la documentation des APIs de Strasbourg.eu. 

Ces APIs vous permettront d'accéder à différentes données de Strasbourg.eu comme les événements et les lieux de l'Eurométropole de Strasbourg.

# Authentification

Certaines APIs sont publiques, d'autres sont protégées par une authentification HTTP.

Les APIs publiques sont indiquées comme telles dans la documentation.

Vous devez posséder un compte utilisateur sur Strasbourg.eu pour accéder aux endpoints protégés.

Deux méthodes sont possibles pour s'authentifier auprès de l'API :

* Ajoutez le header HTTP `Authorization: Basic KEY` à chacune de vos requêtes, où KEY est la valeur en base 64 de la chaine de caractères 'username:password' : , vous pouvez utiliser un encodeur en ligne comme [celui-ci](http://www.motobit.com/util/base64-decoder-encoder.asp) pour effectuer l'encodage

* Ajoutez 'username:password@' devant chaque URL des endpoints de l'API (`https://www.strasbourg.eu/api/...` devient `https://username:password@www.strasbourg.eu/api...`)
