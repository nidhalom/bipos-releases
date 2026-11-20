# Bipos — logiciel de caisse

Bipos est un logiciel de caisse pour supérettes, boulangeries et commerces de proximité,
sous Windows 10 et 11. Il fonctionne sans Internet, installé sur le PC du magasin.

- Vente au comptoir avec lecteur de code-barres, écran tactile et clavier.
- Impression des tickets (58 ou 80 mm), tiroir-caisse.
- Produits, familles, photos, articles au poids.
- Réception de marchandise, étiquettes, stock.
- Clôture de caisse (Z), rapports, sauvegardes automatiques.
- Balances étiquettes Aclas (avec l'installation faite par l'installateur).

Page de présentation : [index.html](index.html) (avec captures d'écran dans `img/`).

## Télécharger

La dernière version est dans l'onglet **Releases** de ce dépôt :
**Bipos 1.5.1** → `Bipos_1.5.1_public.zip`.

Le zip contient seulement :

| Fichier | Rôle |
|---|---|
| `Bipos.exe` | le logiciel de caisse |
| `INSTALLER.bat` | installe Bipos dans `C:\Bipos` et crée le raccourci « Bipos » sur le Bureau |
| `LISEZ-MOI.txt` | les étapes d'installation et d'activation |

Il faut « Microsoft Edge WebView2 Runtime », déjà présent sur Windows 10/11 à jour.

## Installation et activation

1. Décompresser le zip, puis double-cliquer sur `INSTALLER.bat`.
2. Lancer Bipos : il affiche « Ce poste n'est pas activé » et un **code du poste**
   (12 caractères, ex. `K7Q2-9MXA-4F3D`).
3. Envoyer ce code par WhatsApp (les QR codes à l'écran ouvrent WhatsApp avec le message prêt).
4. Le **code d'activation** revient par WhatsApp : c'est un long code (103 caractères).
   Le copier-coller en entier dans la case, puis « Activer ».

Chaque code d'activation ne fonctionne que sur le PC qui a donné le code du poste.

Contact : WhatsApp +213 555 16 85 49 ou +213 772 61 01 54.

## Nouveautés de la version 1.5.1

- Activation plus sûre : la licence est vérifiée par signature numérique (Ed25519).
- Les codes d'activation de la version 1.5.0 (16 caractères) ne fonctionnent plus :
  après la mise à jour, Bipos l'explique à l'écran et il suffit de demander un nouveau code.
  Le code du poste ne change pas, les produits et les ventes ne sont pas touchés.

## Vérifier le téléchargement

Empreinte SHA-256 de `Bipos_1.5.1_public.zip` :

```
6b906f2df5c05fe9b4da63eedb249947244d21757138e6dab89634764004ed7c
```

Sous Windows (PowerShell) : `Get-FileHash .\Bipos_1.5.1_public.zip -Algorithm SHA256`.

---

Ce dépôt contient seulement la présentation et les versions publiées de Bipos, pas son code source.
© 2026 Nidhal Kissoum.
