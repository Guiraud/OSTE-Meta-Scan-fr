Voici la traduction en français du contenu du fichier README.md :

# OSTE-Meta-Scanner
![Projet Logo](OSTEscaner/images/meta.png)
Ce projet vise à simplifier le domaine de l'analyse dynamique de la sécurité des applications. Le métascanner OSTE est un scanner de vulnérabilités Web complet qui combine plusieurs scanners DAST, dont Nikto Scanner, OWASP ZAP, Nuclei, SkipFish et Wapiti.

## Table des matières

- [Introduction](#introduction)
- [Caractéristiques](#caractéristiques)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Contribution](#contribution)
- [Licence](#licence)
- [Captures d'écran](#captures-d'écran)

## Introduction
Ce logiciel offre une interface graphique conviviale qui présente un rapport complet pour chaque analyse, rendant le processus de scan très facile et intuitif.

L'objectif principal de ce scanner est les vulnérabilités d'injection Web telles que l'injection SQL, l'injection XSS, l'injection de commandes système, l'injection XML et bien d'autres. De plus, il fournit une liste des vulnérabilités prises en charge par chaque scanner, en plus des vulnérabilités d'injection.

Nous proposons deux types de rapports. Le premier est un rapport consolidé au format JSON, qui comprend les rapports importants de chaque scanner. Il contient des détails tels que la vulnérabilité, l'URL correspondante, le paramètre utilisé, la commande Curl, le vecteur d'attaque, une description de la vulnérabilité, etc.

Le deuxième rapport est un fichier HTML qui met en évidence spécifiquement les attaques par injection réussies. Nos résultats et décisions sont basés sur un nouvel algorithme d'apprentissage proposé lors de la présentation ("A Meta-Scan based approach for the detection of injection vulnerabilities in Web applications.", -Université du 8 mai 1945 à Guelma, Département d'informatique, présenté par : SEYYID TAQY EDINE OUDJANI, supervisé par: DR. ABDELHAKIM HANNOUSSE. 2023). [https://dspace.univ-guelma.dz/jsp ui/handle/123456789/15028].

## Caractéristiques

Liste des principales vulnérabilités prises en charge :
1. Injection
  - Injection SQL
  - Cross Site Scripting
  - Injection de commandes système
  - Injection XML
  - Injection XSLT
  - Entités XML externes
  - Injection de code
  - Injection dans l'en-tête de l'hôte
  - Injection HTML
  - Injection de modèle (côté serveur)
  - Injection CRLF
  - Injection OGNL
2. Autres vulnérabilités (consultez le dépôt de chaque scanner pour une liste complète.)
  - Liste des vulnérabilités prises en charge par Skipfish.
  - Liste des vulnérabilités prises en charge par Wapiti.
  - Liste des attaques actives d'OWASP ZAP.
  - Liste des vulnérabilités prises en charge par Nikto (spécifié : Tunning 9 et 4).
  - Modèle CVE Nuclei.

## Installation
### Installation sous Mac OS M2
```ZSH
brew update 
brew upgrade
brew install nuclei
pip3 install wapiti3
pip3 install Pillow
pip3 install matplotli
```
### Installation sous Linux

Le processus d'installation nécessite un ensemble spécifique de prérequis. Bien que ce projet soit principalement pris en charge sur Kali Linux, il peut également être compatible avec d'autres systèmes d'exploitation :

1. OWASP zaproxy:
  - kaliLinux: [ sudo apt install zaproxy ]
  - Autres OS: [ https://github.com/zaproxy/zaproxy ]

2. Wapiti:
  - kaliLinux: [ sudo apt install wapiti ]
  - Autres OS: [ https://wapiti-scanner.github.io/ ]

3. Skipfish:
  - kaliLinux: [ sudo apt install skipfish ]
  - Autres OS: [ https://gitlab.com/kalilinux/packages/skipfish ]

4. Nikto :
  - kaliLinux: [ sudo apt install nikto ]
  - Autres OS: [ https://github.com/sullo/nikto ]

5. Nuclei:
  - kaliLinux: [ sudo apt install nuclei ]
  - Autres OS: [ https://github.com/projectdiscovery/nuclei ]

6. Python 3 * Bibliothèques:
  - customtkinter
  - zapv2
  - jinja2
  - webbrowser
  - PIL
  - matplotlib
  - BeautifulSoup
  - pprint

7. Prérequis optionnels pour plus de fonctionnalités:
  - Serveur XAMP
  - NPM

(Remarque: Veuillez noter que je créerai un script bash pour automatiser les étapes d'installation pour les utilisateurs de Linux dès que possible.)

## Utilisation

Après avoir cloné le dépôt sur votre machine locale, vous pouvez lancer l'application en exécutant la commande python3 Metascan.py.

Ensuite, vous pouvez naviguer dans l'interface de l'application.

## Contribution

L'auteur initial accueille les contributions pour améliorer et perfectionner ce projet.
soit par un don:
  [![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/oudjanisaye)

soit par votre pouvoir d'esprit. Pour contribuer, veuillez suivre ces directives :

   1. Forkez le dépôt et créez une nouvelle branche pour votre contribution.
   2. Assurez-vous que votre code respecte les normes de codage du projet.
   3. Effectuez vos modifications, en traitant le problème spécifique ou en ajoutant l'amélioration proposée.
   4. Testez minutieusement vos modifications.
   5. Commitez vos modifications et fournissez un message de commit clair et descriptif.
   6. Poussez vos modifications vers votre dépôt forké.
   7. Soumettez une Pull Request, en détaillant les modifications que vous avez apportées et en fournissant toutes les informations ou contextes pertinents.

Veuillez noter que toutes les contributions seront examinées par les mainteneurs du projet. Nous apprécions votre effort et ferons de notre mieux pour fournir des commentaires dans les meilleurs délais.

Si vous avez des questions ou avez besoin d'une clarification, n'hésitez pas à nous contacter via le système de suivi des problèmes ou en contactant directement les mainteneurs du projet.

## Licence

Ce projet est sous la licence GNU GENERAL PUBLIC LICENSE Version 3, 29 juin 2007.

Ce projet a pour but pédagogique et vise à simplifier l'évaluation globale de la cybersécurité. Cependant, nous tenons à souligner que nous ne sommes pas responsables de toute utilisation malveillante de cette application. Il est crucial que les utilisateurs de ce logiciel fassent preuve de responsabilité et de comportement éthique. Nous vous recommandons fortement de notifier les cibles ou les personnes impliquées avant d'utiliser ce logiciel.

## Captures d'écran
![Interface principale](ScreenShots/Screenshot_2023-05-31_15-09-04.png)

## Contact
   linkdin:(https://www.linkedin.com/in/oudjani-seyyid-taqy-eddine-b964a5228)