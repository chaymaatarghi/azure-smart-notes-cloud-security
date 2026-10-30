# Smart Notes — Azure Cloud Security

Projet académique collectif de sécurité cloud réalisé à l'EFREI Paris.

**[Application de démonstration](https://sn-dev-app.azurewebsites.net/)** · **[Code source du projet collectif](https://github.com/sidiprograms11/AZURE-PROJECT)**

> Ce dépôt personnel présente l'architecture, les contrôles de sécurité et ma contribution au projet. Le code source collectif est conservé dans le dépôt d'origine. La disponibilité actuelle de l'application en ligne n'est pas garantie.

## Objectif

Concevoir une application web permettant de créer, consulter et supprimer des notes, avec stockage dans Azure SQL Database et mise en pratique de mesures de sécurité cloud.

## Architecture et technologies

| Composant | Rôle |
| --- | --- |
| Azure App Service | Hébergement de l'application web |
| Azure SQL Database | Stockage des notes |
| Azure Key Vault | Stockage des paramètres sensibles |
| Managed Identity | Accès aux services Azure sans identifiants dans le code |
| Azure Monitor et Application Insights | Supervision et journalisation |
| Bicep | Description de l'infrastructure en tant que code (IaC) |

Le projet comprend également des fichiers GitHub Actions pour les déploiements d'infrastructure et d'application dans le dépôt collectif.

## Sécurité étudiée et mise en œuvre

- Gestion des secrets avec **Azure Key Vault** et **Managed Identity**.
- Configuration applicative via les variables d'environnement d'**Azure App Service**.
- Analyse des menaces selon **STRIDE** : usurpation, altération, répudiation, divulgation, déni de service et élévation de privilèges.
- Classification des données et analyse **DICP** (disponibilité, intégrité, confidentialité, preuve/traçabilité).
- Collecte des événements et supervision avec **Azure Monitor / Application Insights**.

**Périmètre :** l'intégration complète de Microsoft Entra ID pour l'authentification des utilisateurs, un WAF, des Private Endpoints et un plan de reprise après sinistre sont identifiés dans le rapport comme **améliorations futures**, et non comme fonctionnalités déjà déployées.

## Tests documentés

Le rapport de projet présente des tests réussis portant sur :
1. L'accessibilité de l'application via Azure App Service.
2. La création et la consultation de notes.
3. La connexion à Azure SQL Database.

Ces résultats correspondent à la démonstration réalisée pendant le projet académique ; ils ne constituent pas une validation de l'état actuel du service en ligne.

## Ma contribution

**Chaymaa Targhi — Hébergement applicatif Azure :**
- Travail sur **App Service Plan** et **Azure Web App**.
- Configuration des paramètres d'application et intégration avec les services de supervision et d'identité.
- Participation à l'architecture et à la documentation de sécurité du projet collectif.

## Équipe et attribution

Projet réalisé par **Chaymaa Targhi, Inès El Ghouaouta, Sidi Gano et Yann Tio**, encadré dans le cadre du cursus EFREI Paris.

Le code applicatif et les fichiers d'infrastructure sont accessibles dans le **[dépôt GitHub de l'équipe](https://github.com/sidiprograms11/AZURE-PROJECT)**. Ce dépôt de portfolio ne revendique pas l'écriture individuelle de l'ensemble du code.

## Limites et pistes d'amélioration

- Authentification des utilisateurs via Microsoft Entra ID.
- Renforcement de l'exposition réseau avec WAF et Private Endpoints.
- Gestion plus fine des rôles applicatifs.
- Sauvegarde, résilience et plan de reprise après incident.

## Références

- [Application Smart Notes](https://sn-dev-app.azurewebsites.net/)
- [Dépôt collectif et code source](https://github.com/sidiprograms11/AZURE-PROJECT)
