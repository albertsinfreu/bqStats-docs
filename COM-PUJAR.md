# Pujar els MD a un repo nou públic

Els fitxers d’aquesta carpeta (README.md, DETALLS_JORNADA.md, PER_JUGADOR.md) ja tenen commit.

## Opció A: Des del navegador + terminal

1. **Crea el repo a GitHub:**  
   https://github.com/new  
   - Nom: `bqStats-docs` (o el que vulguis)  
   - Públic  
   - **No** afegeixis README, .gitignore ni llicència (el repo ha d’estar buit)

2. **Enllaça i puja** (a la terminal, dins d’aquesta carpeta `docs-public`):

```bash
cd /Users/albert/Downloads/bqStats/docs-public
git remote add origin https://github.com/albertsinfreu/bqStats-docs.git
git branch -M main
git push -u origin main
```

(Si el teu usuari de GitHub és un altre, canvia `albertsinfreu` per el teu.)

## Opció B: Amb GitHub CLI (si tens `gh` i sessió iniciada)

```bash
cd /Users/albert/Downloads/bqStats/docs-public
gh auth login
gh repo create bqStats-docs --public --source=. --remote=origin --push --description "Estadístiques UESC (només MD)"
```
