# CBL 93 – Site du Club de Lutte de Bagnolet

Site du CBL 93 exporté depuis Claude Design, publié sur GitHub Pages, domaine `cbl93.com` :
https://cbl93.com/

## Structure

| Fichier | URL |
| --- | --- |
| `index.html` | `/` |
| `cours/index.html` | `/cours` |
| `inscription/index.html` | `/inscription` |
| `club/index.html` | `/club` |
| `contact/index.html` | `/contact` |

- `support.js` : runtime `dc-runtime` qui rend les composants
- `images/` : logo, QR code du dossier, illustrations, affiches
- `CNAME` : domaine personnalisé pour GitHub Pages

Les chemins vers `/images/` et `/support.js` sont **absolus** : les pages vivent dans
des sous-dossiers, un chemin relatif casserait depuis `/cours/` et consorts.

Site statique, aucun build : servir le dossier tel quel.
