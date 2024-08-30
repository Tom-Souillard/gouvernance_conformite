
### **Synthèse**
- **Analyse d'Impact sur la Sécurité (AIS)** : Processus permettant d'identifier et d’évaluer les conséquences potentielles sur la sécurité de l'information en cas d'incident affectant un actif critique.
- **Objectif** : Quantifier les impacts sur la **confidentialité**, l'**intégrité**, et la **disponibilité** de l'information, afin de prioriser les mesures de protection et les plans de continuité.
- **Exigences ISO 27001** : L'AIS fait partie de la gestion des risques, conformément à la clause A.8 (Gestion des actifs) et A.16 (Gestion des incidents).
- **Résultat** : Priorisation des actifs critiques et actions correctives pour minimiser les risques.

---

### **Développement**

#### **1. Définition de l'Analyse d'Impact sur la Sécurité (AIS)**
L'**Analyse d'Impact sur la Sécurité** (AIS) est un processus systématique qui vise à évaluer les effets négatifs potentiels sur la sécurité de l'information lorsqu'un actif critique est compromis ou impacté par un incident. Ce processus permet de comprendre les impacts sur les trois piliers fondamentaux de la sécurité de l’information :
- **Confidentialité** : La protection des données contre un accès non autorisé.
- **Intégrité** : L’assurance que les données ne sont ni altérées ni modifiées de manière non autorisée.
- **Disponibilité** : La garantie que les données et systèmes sont accessibles en permanence lorsque cela est nécessaire.

L'AIS est essentiel pour la planification des **plans de continuité** et de **réponse aux incidents**, car il aide à prioriser les mesures de sécurité en fonction des impacts potentiels.

**Exemple** : Si un serveur hébergeant une base de données clients est indisponible, l’AIS évaluerait les impacts de cette indisponibilité sur la productivité, la satisfaction client, et les risques de violation de données.

#### **2. Étapes de l'Analyse d'Impact sur la Sécurité**

##### **2.1. Identification des actifs critiques**
La première étape consiste à identifier les **actifs critiques** de l’organisation. Il s’agit d’identifier les actifs qui ont une valeur importante pour l’organisation, notamment ceux qui jouent un rôle central dans les opérations de l'entreprise ou ceux qui contiennent des données sensibles.
- **Outils utilisés** : Inventaire d’actifs, registre des risques, entretiens avec les parties prenantes.

**Exemple** : Les actifs critiques d'une société de commerce électronique peuvent inclure les serveurs de paiement, les bases de données clients, et les plateformes de gestion des commandes.

Voici un **exemple d'identification des actifs critiques** dans le cadre de l'ISO 27001 :

| **ID de l'actif** | **Nom de l'actif**        | **Type d'actif**   | **Critères de criticité**                                  | **Impact potentiel**                                      |
|-------------------|---------------------------|--------------------|------------------------------------------------------------|-----------------------------------------------------------|
| A001              | Serveur de paiement        | Physique           | Traitement des transactions financières                     | Perte financière, non-conformité PCI DSS                   |
| A002              | Base de données clients    | Informationnel      | Contient des informations personnelles et sensibles (RGPD)  | Vol d'identité, sanctions juridiques, atteinte à la réputation |
| A003              | Logiciel ERP               | Logiciel           | Gère les processus financiers et logistiques de l'entreprise| Perturbation des opérations, perte de productivité         |
| A004              | Employé IT                 | Humain             | Responsable de la gestion des systèmes critiques            | Mauvaise gestion des incidents, faille de sécurité         |

Critères d'identification :
- **Valeur pour l’organisation** : Un actif est critique si sa compromission entraîne des impacts significatifs sur les opérations.
- **Impact financier, légal et opérationnel** : Actifs susceptibles de provoquer des pertes financières ou des problèmes de conformité.

Ce tableau aide à classer et prioriser les actifs qui nécessitent des contrôles de sécurité renforcés.

##### **2.2. Évaluation des scénarios d'incidents**
Une fois les actifs identifiés, différents scénarios d’incidents doivent être définis pour chacun. Il s’agit de situations où l'actif pourrait être compromis, détruit, ou rendu indisponible.
- **Exemples de scénarios** : Attaque par ransomware, panne matérielle, vol de données, ou sabotage interne.

**Exemple** : Une panne de serveur de base de données critique peut résulter d'une attaque DDoS (Déni de service) ou d'une erreur de configuration.

**Évaluation des scénarios d'incidents**

1. **Serveur de paiement** (ID: A001)
   - **Scénario d'incident** : 
     - **Attaque par ransomware** : Chiffrement des données du serveur de paiement, rendant les transactions financières impossibles.
     - **Impact** : Perte de revenus en raison de l'indisponibilité du service, non-conformité PCI DSS, risques juridiques et amendes.
     - **Mesures** : Sauvegardes régulières, chiffrement, surveillance continue des logs, et pare-feu.

2. **Base de données clients** (ID: A002)
   - **Scénario d'incident** :
     - **Violation de données** : Un attaquant accède aux informations personnelles (PII) des clients.
     - **Impact** : Sanctions RGPD, vol d'identité des clients, atteinte à la réputation.
     - **Mesures** : Chiffrement AES-256, authentification multifactorielle, audits réguliers des accès.

3. **Logiciel ERP** (ID: A003)
   - **Scénario d'incident** :
     - **Panne logicielle** : Le système ERP devient inaccessible à cause d'une panne technique ou d'une erreur de mise à jour.
     - **Impact** : Interruption des opérations logistiques et financières, retard dans les livraisons et pertes de productivité.
     - **Mesures** : Plan de continuité des opérations, redondance du système, sauvegardes.

4. **Employé IT** (ID: A004)
   - **Scénario d'incident** :
     - **Erreur humaine** : Un administrateur IT modifie par inadvertance les paramètres d'accès des systèmes critiques, causant une panne ou une faille de sécurité.
     - **Impact** : Indisponibilité des systèmes critiques, risque d'intrusion.
     - **Mesures** : Formation régulière, séparation des responsabilités, suivi des actions via journaux d'audit.

Ces scénarios montrent l’importance d’évaluer les impacts sur la sécurité des actifs critiques, permettant d’anticiper les incidents, de réduire les risques et de mettre en place des mesures correctives conformes à l'ISO 27001.

##### **2.3. Analyse des impacts**
Cette étape consiste à quantifier et qualifier les impacts d’un incident potentiel sur la sécurité des informations. Cela inclut l’impact financier, juridique, opérationnel, ou sur la réputation. Les impacts sont généralement classés en fonction de leur gravité (faible, modéré, élevé).
- **Confidentialité** : Risque de fuite de données.
- **Intégrité** : Possibilité de modification non autorisée des données.
- **Disponibilité** : Interruption des opérations métiers critiques.

**Exemple** : Une entreprise bancaire pourrait subir de lourdes amendes et une perte de réputation si une violation des données clients survient, mettant en péril la confidentialité.

**Exemple d’Analyse des impacts**

1. **Serveur de paiement (A001)**
   - **Confidentialité** : Faible impact direct, mais en cas de compromission des données clients lors des transactions, un vol de données serait grave.
   - **Intégrité** : Si les données des transactions sont modifiées, cela entraînerait des erreurs de facturation.
   - **Disponibilité** : Impact majeur ; chaque heure d'indisponibilité entraînerait des pertes financières immédiates et des clients mécontents.

2. **Base de données clients (A002)**
   - **Confidentialité** : Impact très élevé. Une violation des données clients entraînerait de graves sanctions (RGPD) et des poursuites judiciaires.
   - **Intégrité** : Si les données sont altérées, cela pourrait entraîner de fausses informations clients, créant des problèmes de service.
   - **Disponibilité** : Impact modéré ; bien que critique, des solutions de sauvegarde rapide peuvent minimiser l'indisponibilité.

3. **Logiciel ERP (A003)**
   - **Confidentialité** : Impact faible, les données du ERP ne sont pas très sensibles.
   - **Intégrité** : Impact élevé. Une corruption des données de l'ERP pourrait entraîner une mauvaise gestion des stocks, des commandes et des finances.
   - **Disponibilité** : Impact élevé. Toute indisponibilité affecterait directement les opérations logistiques et financières de l’entreprise, entraînant des pertes économiques.

4. **Employé IT (A004)**
   - **Confidentialité** : Impact modéré ; si l’employé accède à des données non autorisées, cela pourrait causer des violations internes.
   - **Intégrité** : Impact élevé. Une erreur dans la gestion des systèmes critiques pourrait causer des interruptions ou des vulnérabilités.
   - **Disponibilité** : Impact élevé si des systèmes critiques deviennent inaccessibles ou compromis à la suite d'une mauvaise manipulation.

L’analyse des impacts permet de comprendre les conséquences potentielles d'un incident sur la **confidentialité**, **intégrité**, et **disponibilité** des actifs critiques. Cette évaluation permet d'identifier les priorités pour renforcer les contrôles de sécurité et mettre en place des plans de réponse adaptés.

##### **2.4. Priorisation des impacts**
Les actifs ayant le plus grand impact potentiel en cas de compromission sont priorisés pour des mesures de protection supplémentaires. L'analyse permet de déterminer quelles ressources doivent être les plus protégées et quelles actions doivent être prises en priorité pour assurer leur sécurité.

**Exemple** : Dans un centre de traitement des paiements, les systèmes traitant des informations de cartes de crédit seront prioritaires pour la protection, conformément aux obligations légales (ex : PCI DSS).

**Critères de priorisation** (dans le cadre de l'ISO 27001)

Les **critères de priorisation** permettent de classer les actifs en fonction de l'impact potentiel sur la sécurité de l’information, afin de mieux cibler les efforts de protection. Voici les critères clés pour prioriser les actifs identifiés dans l’analyse d’impact :

1. **Criticité des actifs** :
   - **Actifs critiques** : Ceux dont l'indisponibilité entraînerait une paralysie des opérations (ex : serveur de paiement).
   - **Actifs sensibles** : Contenant des données confidentielles, comme les bases de données clients.

   **Exemple** : Un serveur de paiement serait priorisé en raison de son impact sur les revenus, suivi de la base de données clients pour des raisons de conformité RGPD.

2. **Conséquences légales et réglementaires** :
   - Les actifs dont la compromission entraînerait des sanctions réglementaires ou des amendes importantes (ex : base de données clients dans le cadre du RGPD).

   **Exemple** : La base de données clients serait prioritaire pour éviter les amendes RGPD en cas de violation de données.

3. **Impact financier** :
   - Actifs dont la perte ou l’indisponibilité entraînerait des pertes économiques directes, comme les systèmes financiers et ERP.

   **Exemple** : L’ERP serait classé en priorité élevée pour éviter les interruptions dans la gestion des stocks et les flux financiers.

4. **Impact sur la réputation** :
   - Actifs dont la compromission affecterait directement l’image publique ou la confiance des clients.

   **Exemple** : La fuite de données personnelles via la base de données clients aurait un impact majeur sur la réputation de l'entreprise.

5. **Fréquence des incidents passés** :
   - Les actifs ayant déjà subi des incidents ou identifié comme étant vulnérables aux menaces sont priorisés pour limiter les futurs risques.

   **Exemple** : Si un serveur de paiement a déjà été ciblé par une attaque DDoS, il doit être renforcé et priorisé pour éviter une nouvelle attaque.

6. **Temps de rétablissement nécessaire** :
   - Actifs dont la récupération est plus longue ou complexe doivent être priorisés pour garantir leur disponibilité continue.

   **Exemple** : Un serveur critique avec un long temps de rétablissement en cas d’incident doit bénéficier de mesures de redondance.

Les critères de priorisation permettent de concentrer les ressources et les efforts de sécurité sur les actifs présentant les impacts les plus graves en cas d'incident, en fonction de la criticité, des conséquences légales, de l'impact financier et sur la réputation, ainsi que des incidents passés.


**Priorisation des impacts pour les actifs identifiés**

1. **Serveur de paiement (A001)** :
   - **Priorité : Très haute**
   - **Critères** :
     - Impact financier direct en cas d'indisponibilité.
     - Conséquences juridiques graves si non-conformité avec les normes PCI DSS.
     - Perte de confiance des clients.
   - **Conclusion** : Le serveur de paiement doit être la priorité absolue pour éviter tout incident qui affecterait les revenus et la conformité.

2. **Base de données clients (A002)** :
   - **Priorité : Très haute**
   - **Critères** :
     - Risques juridiques et financiers majeurs (RGPD) en cas de fuite.
     - Répercussions importantes sur la réputation.
   - **Conclusion** : La base de données clients est une priorité élevée pour la protection de la confidentialité et la conformité légale.

3. **Logiciel ERP (A003)** :
   - **Priorité : Haute**
   - **Critères** :
     - Impact élevé sur l'intégrité des données (stocks, finances) en cas de panne ou de corruption.
     - Interruption des opérations commerciales.
   - **Conclusion** : Bien que l’impact financier soit moins direct que celui du serveur de paiement, l’ERP reste une priorité élevée.

4. **Employé IT (A004)** :
   - **Priorité : Moyenne**
   - **Critères** :
     - Risque modéré de violation interne ou d'erreur humaine.
     - Impact modéré sur la continuité des opérations en cas de mauvaise gestion des systèmes.
   - **Conclusion** : La formation et la surveillance des actions des employés IT doivent être prises en compte, mais l’impact est inférieur aux actifs technologiques.

**Priorisation globale** :
1. **Serveur de paiement** (A001) – **Très haute priorité**
2. **Base de données clients** (A002) – **Très haute priorité**
3. **Logiciel ERP** (A003) – **Haute priorité**
4. **Employé IT** (A004) – **Priorité moyenne**

Cette priorisation permet de concentrer les efforts sur les actifs avec le plus d'impact potentiel en termes financiers, juridiques, et de réputation.

##### **2.5. Définition des actions correctives**
Après avoir évalué les impacts, des mesures préventives et correctives sont mises en place pour limiter les risques et atténuer les conséquences en cas d'incident. Cela inclut l'amélioration des politiques de sauvegarde, des plans de réponse aux incidents et des procédures de continuité des activités.
- **Actions correctives** : Renforcement des contrôles d’accès, amélioration du chiffrement, mise en place de systèmes de redondance pour les actifs critiques.

**Exemple** : Si un impact élevé est identifié sur la disponibilité d’un serveur critique, la solution pourrait inclure une redondance géographique et un plan de reprise après sinistre.


**Exemple des actions correctives suite à la priorisation globale**

1. **Serveur de paiement (A001)** – **Très haute priorité**
   - **Action corrective** : Mettre en place une **redondance géographique** pour garantir la disponibilité continue en cas d'attaque DDoS ou de panne. Mise à jour des pare-feux et installation d'un système de détection d’intrusion (IDS) pour prévenir les attaques.
   - **Chiffrement** : Renforcer le chiffrement des transactions avec TLS et surveiller les journaux d'accès en temps réel.
   - **Sauvegarde** : Sauvegarde journalière des transactions financières.

2. **Base de données clients (A002)** – **Très haute priorité**
   - **Action corrective** : Renforcer les contrôles d'accès en intégrant une **authentification multifactorielle (MFA)** pour les utilisateurs accédant aux données clients.
   - **Chiffrement AES-256** des données clients sensibles et révision des politiques de conservation des données pour respecter le RGPD.
   - **Audit de sécurité** : Audits de sécurité trimestriels sur la base de données pour identifier toute vulnérabilité.

3. **Logiciel ERP (A003)** – **Haute priorité**
   - **Action corrective** : Implémentation d'un **plan de continuité d'activité** (PCA) avec une sauvegarde des données critiques toutes les heures. Assurer que les correctifs logiciels sont appliqués rapidement via un programme de gestion des mises à jour automatisées.
   - **Tests de redondance** : Vérification régulière des systèmes de redondance pour l’ERP, et des sauvegardes hors site pour protéger les données des stocks et des finances.

4. **Employé IT (A004)** – **Priorité moyenne**
   - **Action corrective** : Organisation de formations supplémentaires sur la sécurité pour les administrateurs systèmes. Mise en place d’une **séparation des privilèges** pour éviter que des erreurs humaines n’affectent les systèmes critiques.
   - **Audit des actions** : Surveillance plus étroite des actions administratives via des journaux d’audit centralisés pour suivre toutes les modifications.

Ces actions correctives permettent de renforcer la sécurité des actifs critiques en priorisant la disponibilité, la confidentialité, et l'intégrité des systèmes selon leur importance. Ces mesures respectent les exigences de l'ISO 27001 et réduisent significativement les risques identifiés lors de l'analyse d'impact.

#### **3. Conformité à l'ISO 27001 dans le cadre de l'AIS**

L’AIS répond à plusieurs exigences de l’ISO 27001, en particulier les clauses relatives à la gestion des actifs et des incidents :
- **Clause A.8 – Gestion des actifs** : L'inventaire des actifs critiques et leur classification en fonction de leur importance sont des éléments fondamentaux de l'AIS.
- **Clause A.16 – Gestion des incidents** : L'AIS fait partie du processus de gestion des incidents pour identifier et répondre aux menaces pesant sur les actifs critiques.
- **Clause 6.1 – Actions pour traiter les risques liés à la sécurité de l’information** : L’AIS aide à évaluer les risques et à définir des actions correctives pour les atténuer.

### **Conclusion**
L'**Analyse d'Impact sur la Sécurité** (AIS) est un outil indispensable pour identifier les risques pesant sur la sécurité de l’information et mettre en œuvre des mesures adaptées. En respectant les exigences de l'ISO 27001, l'AIS permet d'améliorer la résilience de l'organisation face aux incidents, en garantissant la protection des actifs critiques et la continuité des activités.