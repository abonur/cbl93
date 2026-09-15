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
- `vendor/` : React et ReactDOM 18.3.1 (UMD), servis depuis le domaine.
  `support.js` les chargeait depuis unpkg.com ; chaque page declare desormais un
  `window.__resources` qui redirige ces deux URLs vers `/vendor/`. Aucun appel
  reseau externe : si unpkg tombe, le site continue de fonctionner.
  Les fichiers ont ete verifies contre les empreintes SRI presentes dans `support.js`.
- `images/` : logo, QR code du dossier, illustrations, affiches
- `CNAME` : domaine personnalisé pour GitHub Pages

Les chemins vers `/images/` et `/support.js` sont **absolus** : les pages vivent dans
des sous-dossiers, un chemin relatif casserait depuis `/cours/` et consorts.

Site statique, aucun build : servir le dossier tel quel.
