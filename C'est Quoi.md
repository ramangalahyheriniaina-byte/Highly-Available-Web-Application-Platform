 Highly-Available-Web-Application-Platform(plateforme d'application web a haute disponibilite)

 C'est une Infrastructure concue pour garantir l'application afin qu'il soit accesible aux utilisateur en permanence, malgree les pannes materielle, logiecielle ou les trafics.

 Objectif :
        - Minimisee les interruption de services (99.99 %)


 Pilier du plateforme :
    - Redondance (Eliminer les point de defaillance unique)
        Pour evitee une panne isolee ne fasse tomber toutes l'appplication, il faut dupliquee :
            * Serveur redondants /au lieu d'un seul serveur on utilse groupe de serveur si l'un tombe , les autres prenent le relais
        
            * Replication des bases de donnees /Les donnee dont replique en temps reel sur plusieur instances

            * Zone de disponibilitee /Les Serveur sont repartis sur des centres de donnee geographiquements distincts pour suivre a une pannee local(incendie, coupure electrique, etc ...)



Load Balancer	-> Répartit le trafic et isole les serveurs défaillants.
Auto Scaling	-> Ajuste dynamiquement la puissance de calcul.
Multi-AZ	    -> Garantit la survie de l'infrastructure en cas de catastrophe locale.
Bases de données HA	-> Assure la continuité des données sans perte.