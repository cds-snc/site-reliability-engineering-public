# Processus de gestion d’incidents au SNC

Les employé·e·s du SNC peuvent signaler un incident dès qu’on perçoit un problème.
Pour ce faire, il suffit de saisir « /incident {ce qui ne fonctionne pas} » dans Slack, puis d’appuyer sur la touche «  Entrée  ».
Cette opération activera notre robot SRE-bot, qui mènera les actions suivantes :
Créer un nouveau canal Slack avec le titre **#incident-{date}-{ce qui ne fonctionne pas}**;
Démarrer une nouvelle conférence vidéo persistante dans Google Meet;
Ouvrir un nouveau document dans GoogleDocs en utilisant le modèle de rapport d’incident dans notre référentiel d’incidents situé dans Google Drive;
Partager les liens dans la conférence vidéo et le document dans le nouveau canal Slack;
Ajouter une entrée dans la feuille de suivi d’incidents;
Nommer la personne qui a déclaré l’incident comme **commandant ou commandante de l’incident (CI)** et comme **responsable des opérations (RO)**; et
Publier un message dans le canal **#incident-sre**.

## Régler le problème

> « Les déploiements rapides, fréquents et sécurisés sont la marque de fabrique des opérations logicielles efficaces. Pourquoi? Parce que ces changements sont plus stables, fonctionnent bien la plupart du temps, et apportent de l’énergie et de l’élan aux équipes d’ingénierie. »  
*Source : https://increment.com/reliability/high-performing-team-trust/*

En général, le ou la CI assigne immédiatement le ou la RO, et contacte l’équipe de communications et les personnes chargées de la résolution de l’incident.

Toute personne désireuse ou capable d’aider peut participer à la résolution de l’incident. Cependant, le ou la CI en demeure responsable et détient l’autorité sur le travail effectué.

Cette dernière personne ou un·e membre mandaté de travailler sur l’incident documente le travail en cours, tandis que les membres responsables de la résolution de l’incident publient des messages sur le chat servant à retracer ce qui est fait.

Nous procédons donc à la mitigation ou à la résolution de l’incident immédiate selon le cas.

L’automatisation de nos systèmes de vérifications, tests et déploiements nous permet d’apporter des changements à la production rapidement.

## L’Analyse rétrospective sans reproches

> «  Il y a rétroaction lorsque des informations de sortie d’un système lui sont retournées en entrée dans le cadre d’une chaîne de causalité qui forme un circuit ou une boucle. »  
*Source : https://en.wikipedia.org/wiki/Feedback*

Une fois qu’on a répondu à l’urgence, nous nous réunissons pour faire le bilan de l’incident.

C’est au cours de cette analyse rétrospective sans reproches que nous examinons le document d’incident où nous avons consigné les notes de l’incident.

**Cliquez sur ce lien pour avoir accès au [modèle de rapport d’incident de produit](modele_de_rapport_dincident_de_produit.md).**

Le format et le contenu du document répondent à une démarche qui nous permet de discuter de l’incident de manière logique.

Nous examinons les éléments suivants pour les incidents:

Ce qui s’est passé;

- La nature de l’impact de l’incident sur l’organisme;
- La façon dont il a été détecté;
- La façon dont l’incident a été déclenché, ainsi que le ou les éléments qui l’ont déclenché (système automatisé, employé·e, quelqu’un à l’extérieur de l’organisme);
- La cause profonde qui explique l’incident;
- Là où nous avons échoué, là où nous avons réussi et là où nous avons eu de la chance; and
- Les mesures que nous avons adoptées et celles que nous devons encore prendre.

Les mesures à prendre à la suite de cet incident sont ajoutées aux backlogs des équipes qui en sont chargées pour être ensuite classées par ordre de priorité et faire l’objet de travaux.

En effet, certains incidents sont moins urgents que d’autres.

Par exemple, la rotation des clés susceptibles d’être piratées par accès à nos serveurs peut s’avérer urgente, mais il est préférable d’attendre qu’une solution durable soit mise en place.

En revanche, la rotation d’une clé qui peut être piratée à partir d’Internet s’impose et exige une intervention immédiate, peu importe la difficulté qui pose cette tâche.

L’analyse rétrospective sans reproches ferme la boucle de rétroaction sur l’incident, réduit les chances qu’il se reproduise et nous prépare mieux à l’éventualité d’un nouvel incident ou d’une situation similaire.

## Principes importants

Nous croyons fermement aux principes suivants et nous efforçons de les mettre en pratique :

### 1. Les personnes sont bien intentionnées.

Personne au SNC n’essaie de briser les choses, chacune et chacun fait de son mieux avec les informations dont il dispose.

### 2. Il faut éviter les reproches.

Ce qui ne fonctionne pas au SNC est imputable à l’organisation.

Cela arrive parce que nous n’avons pas mis en place les mesures nécessaires pour l’empêcher.

### 3. Les choses finissent toujours par se briser.

Peu importe ce que nous faisons, il y aura toujours une panne quelque part.
Il faut tenir pour acquis que les choses finissent toujours par se briser.
