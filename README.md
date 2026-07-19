# Highly-Available-Web-Application-Platform
Projet realisee

#Architecture
VM_1 : Reverse Proxy + Load Balancer
    * Nginx
    * SSL (protocole de sécurité fondamental qui chiffre les données    échangées entre un navigateur web et un serveur) /TLS(Let's Encrypt)
    * Monitoring Agent (logiciel installé sur un serveur. Il collecte en  temps réel des données : Ram, CPU, etat )

VM_2 : Application Server
    * Docker
    * Application(node.js,Pyhon Flask)
    * CI CD Deployement

VM_3 : Database + Monitoring
    * PostgresSQL
    * Prometheus
    * Grafana

Logique : 
INTERNET -> VM_1 (Nginx LoadBalancer) -> VM_2 (Docker, Application) -> VM_3 (DB ,Grafana, Prometheus)


Appretissage dans cet projet :

INFRASTRUCTURE /
                Linux Administration
                Resaux(DNS, Reverse Proxy, SSL)
                Firewall(UFW)
DevOps /
        Docker
        Docker compose
        Git
        Github Actions / GitLab CI

Cloud / 
        Provisionnement des VM
        Securisation des serveurs
        Monitoring
SRE /
        Logs
        Metrics
        Alerting
