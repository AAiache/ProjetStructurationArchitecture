Rapport du projet de structuration
============================
<span style="color:#5F983F">Étude des réseaux liés aux autoroutes de France</span>  

**Réalisé par :**  
>- Amina Aiache  
>- Imane Bih
 
**Encadré par :**  
>- M. Emmanuel Bardière     

Master 2 : Technologies des Systèmes d'Information (TSI)  
Ecole Nationale des Sciences Géographiques (ENSG)  
11 Janvier 2016  


##Contexte du Projet  
Dans le cadre de notre formation, nous avons ce projet de structuration et de modélisation qui a pour but de prendre contact avec des sociétés ou organismes qui ont la gestion d'un Système d'information afin de proposer une modélisation d'une utilisation identifiée de façon précise.  
L'objectif étant d'arriver à modéliser une problématique autour d'un réseau, d'un Système d'Information avec toutes ses composantes.  
Dans notre cas, nous avons assayé de contacter plusieurs organismes, notamment les aéroports de Paris, la SNCF et d'autres.  
Nous avons reçu une première réponse de la part de l'aéroport de Paris Charles de Gaulle, où il nous ont demandé de leur donner plus de détails sur le projet et son déroulement, nous avons bien répondu clairement, mais nous n'avons pas reçu une réponse définitive.  
Nous avons eu le même problème avec la SNCF.  
Malheureusement aucun n'organisme n'a donc accepté de nous accueillir, ce qui a fait que nous avons changé de sujet plusieurs fois, et finalement nous avons choisi de travailler sur un sujet qui soit le plus documenté sur internet, affin que nous puissions le réaliser sans avoir effectué une visite.  
##Introduction
Nous avons choisi de travailler sur les réseaux liés au réseau autoroutier en France, car ils mettent à disposition à travers leur site web et d'autres sources une documentation solide, qui nous a permis de proposer une modélisation d'une problèmatique que nous avons imaginée.  
Dans ce rapport, nous essayons tout d'abord de présenter les réseaux qui sont associés au réseau autoroutié. Par la suite, nous avons imaginé qu'il y a un problème qui va touché l'un ou tous les réseau, et nous allons imaginer comment on va intervenir pour résoudre le problème.  
## 1 - Identification des réseaux liés aux autoroutes de France
Pour arriver à identifier ces réseaux, nous avons déterminé tous les cas d'utilisation qui sont inclus dans le SI des autoroutes, comme le montre la figure suivante:  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagramGlobal.png)  
Nous allons maintenant expliquer chacun des cas d'utilisation à part.  
### 1-1 - Gestion du trafic routier  
Le diagramme des cas d'utilisation suivant l'explique:  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram1.png)  
Les panneaux lumineux qui indiquent en temps réel les éventuels incidents que les usagers risquent de rencontrer. En période normale ils peuvent donner quelques conseils de prudence. 
Le troisième cas d'utilisation indique comment réagir en face de fortes affluences sur les autoroutes qui ont une influence sur la gestion du trafic.  
### 1-2 - Gestion du réseau de la fibre optique (FO)
La figure suivante montre les cas d'utilisations inclus dans ce cas:  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram2.png)  
Les informations trandmise au serveurs de données sont parfois destinées à être affichées dans les panneaux à message variable, et/ou diffusées par Radio.  
Par contre il y a des données qui sont destinées à être transmise auw secours lorsqu'il s'agit d'un incident.  
### 1-3 - Gestion du réseau hydraulique
Ce qui expliqué dans le diagramme suivant:  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram3.png)  
### 1-4 Gestion du réseau électrique  
Comme le montre la figure suivante:  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram4.png)  
### 1-5 Gestion du réseau de stations météorologiques  
Le réseau autoroutier de la France est équipé de capteurs météo qui sont placées sur les bords de l'autoroute. C'est un réseau de stations pour recueillir des données météorologiques.  
Le diagramme suivant montre les différents cas d'utilisation de la gestion du réseau de stations météo :  

![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram5.png)  
### 1-6 Gestion des secours  
L'une des principales missions des autoroutes de France est d'assurer la sécurité des usagers et des équipements de l'autoroutes. Les cas d'utilisation de la gestion des secours sont explicité dans le diagramme qui suit :  
 
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/UseCaseDiagram6.png)  
## 2 - Intervention sur le réseau : cas d'un incendie  
### 1-2 - Définition du problème  
**Qui :** Un camion-citerne transportant du gaz  
**Quoi :** Explosion du camion  
**Où** Près d'une station de péage  
**Conséquences :**  
- Un grand nombre de morts et de bléssés (usagers et agents d'autoroutes)  
- De nombreuses voitures ont étés brûlées en plus du camion  
- La station a été partiellement brûlée  
- Coupure d'eau et d'électricité  
- Dégradations au niveau du réseau de la fibre optique est donc la transmission du flux de données a été coupé.  
**Problèmatique :** Comment faire intervenir tous les réseaux pour résoudre le problème ?  
### 1-3 - Modélisation de la résolution du problème en utilisant l'UML  
Nous allons donc proposer une modélisation des étapes de la résolutions du problème, par ordre chronologique, depuis que l'incident s'est produit jusqu'à la réparation de tous les réseaux.  
Nous avons d'utiliser des diagrammes de séquence parce que, si les diagrammes de cas d'utilisation listent des interactions avec des acteurs en spéciant les grandes fonctions d'un système, les diagrammes de séquences permettent de décrire **comment** les éléments d'un système et les acteurs interagissent. C'est donc le diagramme le mieux adapté qui va nous permettre de montrer comment tous les réseaux du système vont être utilisés en vue de résoudre une situation de crise.  
#### 1-3-1 - Étape 1 : Alerter tous les services concernés de l'incident  
Ce diagramme de séquence illustre l’action de l’usager depuis la détection de l’incident, la recherche du poste d’appel d’urgence et la déclaration au PC de sécurité qui va à son tour avertir le service concerné pour envoyer  les secours nécessaires à la zone de danger.  
  
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/AppelTéléphonique.png)  

#### 1-3-2 - Étape 2 : Intervention des secours  
Ce diagramme modélise l’intervention de différentes entités de secours : pompier, ambulance, secouriste, police et gendarme pour garantir la sécurité des usagers, la lutte contre la propagation de l’incendie, la protection des biens, transporter les blessées vers un établissement hospitalier ,et sans oublier les secouristes qui disposent généralement du matériel nécessaire à la surveillance et aux premiers soins des blessés. 
 
![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/InterventionSecours.png)  

#### 1-3-3 - Étape 3 : Gestion du trafic  
Le diagramme ci-dessous a pour but de  mette en evidence la relation entre les différentes entités de système de gestion du trafic autoroutier lors de l’explosion d’un camion transporteur de gaz près d’une station de péage , et décrire  la réaction du système face à cet incident sur le réseau autoroutier, tout en détaillant le rôle de chacune des entités et les multiples tâches dont elles sont chargées depuis le recueilde l’information jusqu’à les différents étape d’intervention . Ces informations sont retransmises aux automobilistes via les panneaux à message variable pour signaler un incident, et aussi par l’intermédiaire d’Autoroute Info qui est la radio. Ceci a pour objectif la sécurité des usagers de l’autoroute, que ce soit les usagers1 qui sont loin de danger  pour éviter  les bouchons et de conseiller une sortie ou un itinéraire plus favorable, ou bien les usagers2 qui sont dans la zone de danger afin de les secourir.  

![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/GestionTrafic.png)  

#### 1-3-4 - Étape 4 : Réaliser une enquête sur place  
Nous n'avons pas pu trouver une source d'informations officielle, et donc c'est nous qui avons imaginé que cette étape est essentielle avant de commencer à réparer les réseaux.  
Elle consiste a envoyer des experts sur place, en réseau hydraulique, éléctrique et en réseau de la fibre optique afin de s'assurer qu'il n'y a pas de vrais dangers qui peuvent donner lieu à d'autres incidents. S'il y a donc toute sorte de danger, on va la résoudre avant tout. Le digramme de séquence suivant montre les détailles de cette étapes :

![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/RéaliserEnquêteSurPlace.png)  

#### 1-3-5 - Étape 5 : Nétoyer le lieu de l'incident  
Dans cette étape, nous avons modéliser comment l'on va vider le lieu de l'incident de tous les restes, il n'ya plus de présence humaine à ce stade car on a évacué le lieu auparavant.  
On va ainsi enlever toutes les voitures endommagées et tous les restes afin de pouvoir laver l'autoroute. C'est ce qu'explique le diagramme suivant : 

![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/NétoyerLieuIncident.png)  

#### 1-3-6 - Étape 6 : Réparer les réseaux  
Cette étape constitue la dernière étape. On commence donc par réparer tous les réseaux et on effectue un test pour s'assurer que la transmissions des flux se fait bien avant de réparer les chaussées.  
Ci-dessous le dernier diagramme de séquence : 

![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/RéparerRéseaux.png)  

## 3 - Diagramme de classes  
En ce qui concerne le diagramme de classes, nous avons proposé un diagramme de classes général, mais de point de vue réseau, et donc il n'est pas lié au cas d'intervention sur le réseau que nous avons fait.  
**AttenuateurChoc :** Si un usager sort accidentellement de la chaussée, les glissières de sécurité amortiront le choc et limiteront ses conséquences. Les glissières en terre-plein central empêchent le franchissement des voies.  
**IndicateurVent :** Le long des autoroutes, des mâts avec des manches à air, "des chaussettes", rouges et blanches striées, indiquant la direction et l'intensité du vent.  
**BandeUrgence :** La bande d'urgence à droite de la file normale de circulation n'est pas une aire de repos : ne s'y arrêter qu'en cas de danger réel.  
**PanneauMessageVariable :** Les panneaux lumineux indiquant en temps réel les éventuels incidents que les usager risquent de rencontrer. En période normale ils peuvent donner quelques conseils de prudence.  
**EcranAntiEblouissement :** Dans les descentes ou les courbes, les usagers pouvent être éblouis par les phares des voitures circulant dans l'autre sens. Des palettes bien orientées, posées sur les glissières du terre-plein central leur évitent toute vision directe des phares.  
Un **PK** est un point kilométrique est une marque ou repère utilisé pour localiser un point le long d'une voie de transport, notamment dans notre cas le long d'une autoroute. Elle est calculée en mesurant en kilomètres la portion de voie comprise entre le point localisé et un point zéro (topographie) propre à chaque voie, servant d'origine du repère.  


![MacDown logo](/Users/amina/Desktop/ProjetStructurationArchitecture/Diagrammes/ClassDiagram1.png)  

##Conclusions et perspectives
##Biobliographie