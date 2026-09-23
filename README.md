# tavoo.be

Site vitrine de **[Tavoo](https://www.tavoo.be)** — l'intendance des PME : gestion administrative, suivi financier, assurances et agents IA pour les indépendants et PME de Bruxelles et du Brabant wallon.

Tavoo est un nom commercial de Gregory Goemaere SRL et de JD Capital SRL.

## Structure

```
site/                 Le site en ligne — tout ce dossier est déployé
  index.html                                Accueil
  facturation-electronique-peppol.html      Service 01
  gestion-administrative.html               Service 02
  audit-assurances.html                     Service 03
  agents-ia.html                            Service 04
  a-propos.html                             À propos et contact
  sitemap.xml
  robots.txt
assets/               Logos et bannières (hors site)
archive/              Anciennes versions, pour mémoire
.github/workflows/    Déploiement automatique
```

## Caractéristiques techniques

- HTML/CSS statique, sans framework ni étape de build : chaque page est autonome.
- Polices : Bricolage Grotesque, Spectral, IBM Plex Mono (Google Fonts).
- Mesure d'audience : Google Analytics 4, dans le `<head>` de chaque page.
- Prise de rendez-vous : [Cal.com](https://cal.com/greg-tavoo/diagnostic-45-minutes)

## Modifier le site

1. Modifier le fichier HTML voulu dans `site/`.
2. **Le CSS est dupliqué dans chaque page.** Une modification de style doit être reportée dans les six fichiers.
3. Toute nouvelle page doit être ajoutée dans la navigation (`<nav class="tabs">`) des six pages et dans `sitemap.xml`.
4. Tester en local : ouvrir `site/index.html` dans un navigateur.
5. Commit et push sur `main` : le déploiement se lance automatiquement.

## Déploiement

Un push sur `main` qui modifie `site/` déclenche l'envoi FTP vers le serveur. Lancement manuel possible depuis **Actions** > *Déploiement tavoo.be* > *Run workflow*.

Secrets requis dans *Settings > Secrets and variables > Actions* : `FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD`. Ils ne sont jamais visibles dans le code, même sur un dépôt public.

## À faire

- [ ] Bannière de consentement cookies
- [ ] Page vie privée / cookies
- [ ] Photos sur la page À propos

## Droits

Le code est visible à titre de référence. Les textes, l'identité visuelle et le nom Tavoo restent la propriété de leurs auteurs — © Tavoo, tous droits réservés.
