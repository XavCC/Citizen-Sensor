---
title: Capteurs océanographiques opensource / application biologie marine
description : Projet Explore Roland Jourdain - Concarneau-Partenaires = Astrolabe Expédition, Patrice L'Helgouarch, François Legrand, Xavier Coadic, Sylvain Pujol
image_url: https://framapic.org/l4Wug9xsExZI/Tih53AQwMhbO.jpg
---

# [[#OceanisOpen](https://explore.hackpad.com/ep/search/?q=%23OceanisOpen&via=sbt8S4FfmD6)] Capteurs océanographiques opensource / application biologie marine

Projet Explore Roland Jourdain - Concarneau

_Partenaires : Astrolabe Expédition, Patrice L'Helgouarch, François Legrand, Xavier Coadic  _[LabOSe](https://hackpad.com/LabOSe-Laboratoire-Open-Source-dexpriences-libres-et-distribues-SA2B7bDZcbV) , _Sylvain Pujolle_

## Ressources

Réseaux de capteurs citoyens:

*   [SmartCitizens](https://smartcitizen.me/kits/) + cartes
*   [Citizen Sensors](http://citizensensor.cc/) , DIY pollution monitoring
*   The OpenCTD [[On github](https://github.com/OceanographyforEveryone/OpenCTD) ] is a low-cost, open-source CTD for researchers and citizen scientists.          [](http://www.oceanographyforeveryone.com)[http://www.oceanographyforeveryone.com](http://www.oceanographyforeveryone.com/)   
*   Oceanography for Everyone - [The OpenCTD](https://www.rockethub.com/projects/26388-oceanography-for-everyone-the-openctd) ![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_GR2HxhulMMN_p.445644_1460468169710_CrowdCRDBody.jpg)

**Participants : **

*   **François Legrand / Trésorier du CREPP (association de robotique) de Lorient / développeur indépendant / code et Arduino**

*   **Romain / Association Astrolabe Expédition / Biologie moléculaire /**

**Solutions abordées : **

**Design global**

## Solutions abordées

**PARTIE 1 / Capteurs **
<undefined><li>**Capteur de conductivité**</li></undefined>

*   sonde Arduino à 1,5 euros d'hygrométrie / mesure analogique et numérique
*   à étalonner avec des solutions ou des outils scientifiques précis
*   Ré-étalonnage à évaluer régulièrement

<undefined><li>**Capteur de profondeur**</li></undefined>

<undefined><li>**Les capteurs sont connectés à une carte Arduino**</li></undefined>

*   Récupération de l'information et des valeurs 
*   Alimenté en 5V
*   Différents types 

        *   Uno : le plus simple
    *   Nano : miniaturisé
    *   Mega : beaucoup de capteurs possibles

*   On peut y brancher le transmetteur 5 Ghz

**PARTIE 2 / Traitement de l'information**
<undefined><li>**Le Raspberry est la partie programmable des capteurs**</li></undefined>

*   Ordinateur de base alimenté en 5V
*   Programme intermédiaire pour comprendre les mesures

<undefined><li>**Interface ergonomique**</li></undefined>

*   [JeeDOM ](https://www.jeedom.com/site/fr/) est installé sur une carte SD dans le Raspberry
*   Paramétrer le démarrage de l'acquisition de donnée

        *   Scénario : 

**PARTIE 3 / Scénarios d'usage de la sonde contenant les capteurs : **

![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_sbt8S4FfmD6_p.445644_1460990128804_20160416_153034[1].jpg)

Exemple de montage arduino pour système DIY de capteur

![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_sbt8S4FfmD6_p.445644_1460990182125_20160416_153040[1].jpg)

Exemple de station domotique avec raspberry pour piloter le déclenchement des capteurs

![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_sbt8S4FfmD6_p.445644_1460990319820_20160416_153055[1].jpg)

[La version smartphone de JeeDOM](https://www.jeedom.com/site/fr/) 

pour piloter à distance les déclenchements des capteurs et traiter les données collectées.

## PARTIE 4 / Prototypage

**Etape 1 :**

Un tube PVC de 3 mètres, gradué à l'extérieur, et contenant à son extrémité : 

*   une sonde de température - DS18B20 pour commencer), 
*   un capteur de pression MS5535C
*   un capteur de conductivité. 
*   Un Arduino pour gérer cela, relié à un PC par un cable USB

Quand cela fonctionne sur les pontons dans le port, on passe à l'étape suivante
<undefined><li>**Utiliser une sonde PT 1000 avec arduino pour mesure de Température / **2, 3 or 4-wire RTD interface capability</li></undefined>

*   Carte [Max3 1865 RTD](https://datasheets.maximintegrated.com/en/ds/MAX31865.pdf) 
*   1 arduino UNO
*   [max31855_4ch_spi_example.zip](http://www.playingwithfusion.com/include/getfile.php?fileid=7023)                     
*   1 sonde pt 1000, [thermomètre à résistance de platine](https://fr.wikipedia.org/wiki/Thermom%C3%A8tre_%C3%A0_r%C3%A9sistance_de_platine)  ou 2 ou 3 ou 4
*   Github [Arduino Driver Library](https://github.com/olewolf/arduino-max31865/blob/master/MAX31865.h) for the MAX31865
*   Schéma Max31865 avec sonde T° pt 1000 puis arduino + Max31865

![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_sbt8S4FfmD6_p.445644_1466851675526_7900.gif)

![](https://hackpad-attachments.s3.amazonaws.com/explore.hackpad.com_sbt8S4FfmD6_p.445644_1466859366426_MAX31865-sch.png)
