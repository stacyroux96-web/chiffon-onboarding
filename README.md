# CHIFFON — Portail d'onboarding (prototype)

Portail statique responsive, destiné à une démonstration pédagogique du parcours d'intégration chez CHIFFON : **Administratif**, **Accueil**, **Formation**.

## Publication sur GitHub Pages

1. Créer un dépôt GitHub (par ex. `chiffon-onboarding`).
2. Envoyer **à la racine** `index.html`, `styles.css`, `app.js` (et ce README).
3. Dans **Settings → Pages**, choisir **Deploy from a branch**, branche **main**, dossier **/(root)**, puis **Save**.
4. Ouvrir l'URL GitHub Pages fournie par GitHub. Le site est adapté aux téléphones et aux ordinateurs.

## Ce qui fonctionne immédiatement

- Navigation et barre de progression en 3 sections, cases à cocher et progression sauvegardée via `localStorage` sur l'appareil.
- Quiz interactifs (entreprise et RGPD), validation des modules, questionnaire de satisfaction local.
- Profil fictif personnalisable, organigramme illustratif, répertoire de contacts à compléter et accueil sécurité.
- Boutons ouvrant des **brouillons d'e-mail** vers des adresses **fictives** (aucun envoi automatique).

## Ce qui reste à connecter AVANT un déploiement réel

| Fonction | État de cette démo | Solution à prévoir |
|---|---|---|
| Contrat, justificatifs administratifs, signature | Pas de dépôt, pas de signature | SIRH/coffre-fort documentaire sécurisé avec gestion des habilitations et signature |
| Alertes e-mail RH et manager | Liens `mailto:` seulement | Service d'automatisation authentifié (Microsoft Power Automate, par exemple) |
| Planification dans l'agenda manager | Non réalisée | Microsoft Graph/Power Automate après authentification et autorisations |
| Présentation vidéo | Visuel de remplacement | Vidéo hébergée et insérée après validation des droits |
| Contacts, organigramme, modules | Données d'exemple | Référentiel RH validé et maintenu |
| Enquête et suivi multi-utilisateur | Sauvegarde navigateur uniquement | Base sécurisée, authentification, rôles et consentements appropriés |

### Sécurité et RGPD

**GitHub Pages est un hébergement statique public.** Ce prototype ne comporte **ni authentification**, ni backend, ni contrôle d'accès, ni base de données. Il ne convient pas au stockage de contrats, copies de pièces d'identité, données personnelles ou résultats RH réels. Éviter toute donnée réelle dans les champs du prototype : leur contenu reste en `localStorage` et peut être accessible à quelqu'un utilisant le même appareil/profil de navigateur. Ne jamais placer de secrets ou d'informations privées dans le dépôt public.

Pour un vrai déploiement : hébergement de l'interface, connexion à un SIRH/documentaire sécurisés, authentification Microsoft Entra ID ou équivalent, rôles par utilisateur, journalisation, règles de conservation, information des salariés et validation avec le DPO/RSSI. Réserver GitHub Pages à une maquette utilisant des données fictives.

## Personnalisation rapide

- Changer les e-mails fictifs (`EX_RH` et `EX_MANAGER`) dans `app.js` **uniquement pour la démo des brouillons**.
- Remplacer les contacts, le planning et l'organigramme illustratifs par des données validées.
- Remplacer le bloc vidéo par une vidéo autorisée (respecter les éventuels paramètres de confidentialité).
- Changer les textes, couleurs et typographies dans les fichiers HTML/CSS.

## Note sur le dossier source

Source : *ANNEXE 1 DESCRIPTIF DE L'ENTREPRISE* (CHIFFON). Environ 450 salariés, ancrage Auvergne-Rhône-Alpes, accessoires éthiques fabriqués en France, pratiques RH peu structurées et onboarding actuel inexistant, laissé à l'initiative des managers. Les coordonnées, responsables nominatifs, le vrai organigramme opérationnel et les outils informatiques ne sont pas fournis dans cette annexe : ils ne sont donc pas inventés.
