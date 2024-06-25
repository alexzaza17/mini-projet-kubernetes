#﻿# Fankem
## Alex Junior
### Eazytraining 18th DevOps Bootcamp
#### Period: march-april-may

Application

Il est question ici pour nous de deployer wordpress a l aide des fichiers manifest. Nous avons tout d abord creer le fichier:
- Un service Cluster ip mysql-service.yml: permet d' exposer notre application mysql(backend) uniquement a l interieur du cluster. 
- Un volume persistence claim(pvc) mysql-pvc.yml: il permettra de consommer le volume persistent (pv) de notre backend(base de donnees mysql), ici nous n avons pas defini le pv car il sera mis en place de facon automatique 
- deployer mysql avec le fichier mysql-deployment: permet de deployer l'application mysql(backend) c est a dire notre base de donnees. Notre pod va consommer le pvc. 
- Un voume persistent claim(pvc) pour wordpress-pvc.yml: il permettra de consommer le volume persistent (pv) de notre frontend(wordpress), pareil pour ce volume le pv sera creer automatiquement et ne depassera 1Go
- deployer wordpress avec le fichier wordpress-deployment: qui permettra le depoyment du frontend (wordpress qui permet de creer les sites web et les blogs) notre application. Notre pod viendra consommer le volume persistence volume que nous avons mis en place  
- Un service nodePort wordpress-service.yml: permet d'exposer (les pods) notre application via le port 30001 a l exterieur de la machine. En attaquant la machine avec l adresse ip de notre vm mikube et le port on obtient l application wordpress(frontend)


![Mobaxterm](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/852ee5ae-1d9d-480d-b2a6-e27a5fa4831b)


![describe](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/8e45bfb2-12d5-41a9-a84f-2366f96f2a45)


![describe2](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/5f95d2f0-e6e7-4ec2-86f2-5473faadfa99)


![describe3](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/b302ce57-2daf-4211-a5e4-a4d703721c53)


![wordpress](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/f545a104-6a6b-4f2d-b868-21e1245a12a3)


![wordpress2](https://github.com/alexzaza17/mini-projet-kubernetes/assets/159175882/df0bd726-1664-428f-95e7-5ee45b48ce5e)
