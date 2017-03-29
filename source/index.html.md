---
title: Strasbourg.eu - Référence de l'API

language_tabs:
  - shell

toc_footers:
  - <a href='https://www.strasbourg.eu'>Strasbourg.eu</a>
  - <a href='https://github.com/tripit/slate'>Documentation générée par Slate</a>

includes:
 - events
 - categories
search: true
---

# Introduction

Bienvenue sur la documentation des APIs de Strasbourg.eu. 

Ces APIs vous permettront d'accéder à différentes données de Strasbourg.eu comme les événements et les lieux de l'Eurométropole de Strasbourg.

# Authentication

L'accès à l'API est protégé par une authentification HTTP. Vous devez posséder un compte utilisateur sur Strasbourg.eu pour y accéder.

Deux méthodes sont possibles pour s'authentifier auprès de l'API :

* Ajoutez le header HTTP `Authorization: KEY` à chacune de vos requêtes, où KEY est la valeur en base 64 de la chaine de caractères 'username:password' : , vous pouvez utiliser un encodeur en ligne comme [celui-ci](http://www.motobit.com/util/base64-decoder-encoder.asp) pour effectuer l'encodage

* Ajoutez 'username:password@' devant chaque URL des endpoints de l'API (`https://www.strasbourg.eu/api/...` devient `https://username:password@www.strasbourg.eu/api...`)
