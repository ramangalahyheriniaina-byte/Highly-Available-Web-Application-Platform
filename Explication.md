# Highly-Available-Web-Application-Platform

Reverse Proxy + Load Balancer 
1. Serveur Proxy (Forward Proxy) : Réseau Interne vers Externe
    Le proxy classique se place du côté des utilisateurs (réseau interne) pour les connecter à Internet (réseau externe).

Fonctionnement : 
     L'utilisateur se connecte au Proxy → 
     Le Proxy envoie la requête sur Internet → 
     Le Proxy reçoit la réponse et la transmet à l'utilisateur.

Principaux usages :
    * Filtrage des acces : Bloque l'acces aux site non confome a la politique
    * Contournemenent des filtres : Permet de contourner les mesure geographique(souvent associe aux technologie VPN)
    * Anomylisation : Masque l'addresse IP reelle de l'utilisateut sur Internet
    * Optiomisation de la navigation : Accelere le chargement vie ma mise en cache (Sauvegarde locale des pages) et la compression des donnees.
    * Tracabitlite : Enregistre l'ensembre des requetes dans des fichier de logs pour suivre et analysee les connection


2. Reverse Proxy : Réseau Externe vers Interne
    Se deplace du cote des serveurs. Il recoit les requetes du public(internet) et les redirige vers les bon serveurs internes

Fonctionnement :
    L'internaute tape une URL proxy ->
    Le reverse Proxy Interroge le serveur web interne cache

Principaux usages :
    * Sécurité et Masquage : Cache l'existence et l'adresse IP des serveurs web internes.
    * Chiffrement SSL/TLS : Gère les certificats HTTPS à un seul endroit pour décharger les serveurs web (SSL Offloading).
    * Authentification : Centralise le contrôle d'accès et la gestion des droits des utilisateurs avant d'atteindre les applications.  
    * Performances : Compresse les données, filtre les contenus lourds et gère le cache global pour alléger la charge des serveurs en arrière-plan.


3. Load Balancer (LB) : Répartition de charge
    Distribue le trafics de maniere equilitable entre plusieur serveurs pour evitee la surcharge d'un seul equipement. il s'agit souvent comme une reserse Proxy evoluee.

Principaux algorithmes de routage :
    * RP( Round Robin ) : Tour de role simple. Le premiere requete va au serveur 1; la 2eme va sur le servuer 2
    * WRR (Weighted Round Robin) : Tour de role ponderee. On envoie plus de trafic vers les serveur les plus puissants.
    * LC (Leaste Connections) : Moins de connexion. La requete est envoyer au serveur qui gere actuellement le moins de client actifs
    * WLC (Weighted Least Connections) : Moins de connection pondere. Combinee le nombre de connextion actives et la puissance du serveur.
    * IP Hash (KK / AS) : Persistance de session. L'address IP du client est hachee pour s'assurer qu'un meme utilisateur retombe toujours sur le meme serveur


DOCKER : 
    Logiciel Open source permet d'emâqueter et d'executer des application dans une environnements isoles appele CONTENEURS. Garantir un programme fonctionne exactement de la meme maniere sur n'importe ordinateur.

CI / CD (Intégration et Déploiement/Livraison Continus):
     Methode qui automtise les etape entre l'ecriture d'une code et sa mise a disposition pour les utilisateur. Permet de pulier les mise a jour frequence, fiables, haute qualitee tout en limitant les erreur manuelles

PostgresSQL :
    Systeme de gestion de base de donnee(SGBD), permet de stocker, organise et recupere des donnee complexe de maniere securisee.

Prometheus : 
    Outils de surveillance et d'alerte open-source concu pour les infrastructure et les application moderne. temps reel, stocker sous formee de donnee , permet aux equipe de suivre les perfommances et d'etre aleretee en cas d'anomalie.

Grafana : 
    Plateforme d'analyse et de visualisation des donnees. Elle permet de transformee des donnee brute provenant de multples sources(Serveur; base de donnee, cloud) en tableau de bord et en graphique en temps reel.