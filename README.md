
# Données sur la subdivision géographique et administrative du Burkina Faso

Ce dépôt contient des informations structurées sur les 13 régions du Burkina Faso, présentées au format JSON. Ces données offrent une vue d'ensemble des aspects démographiques, géographiques et administratifs de chaque région.

---

## Contenu du dépôt

### Fichiers

- **`regions_burkina_faso.json`** : Le fichier principal contenant les informations sur les 13 régions.

---

## Structure des données

Le fichier JSON suit une structure hiérarchique permettant une exploration facile des données. Les principales sections :

### Racine

- **`count`** *(integer)* : Nombre total de régions (13).
- **`details`** *(array)* : Liste des régions, chaque région ayant les propriétés suivantes :

### Propriétés d'une région

- **`name`** *(string)* : Nom de la région.
- **`code_INSD`** *(string)* : Code INSD de la région.
- **`population_count`** *(object)* : Population estimée par année :
  - Exemple : `y_1985`, `y_1996`, `y_2019`.
- **`area_km2`** *(float)* : Superficie en kilomètres carrés.
- **`capital`** *(string)* : Chef-lieu de la région.
- **`regional_councillors_count`** *(integer)* : Nombre de conseillers régionaux.
- **`provinces`** *(object)* : Informations sur les provinces :
  - `count` *(integer)* : Nombre total de provinces.
  - `details` *(array)* : Liste des provinces, chaque province ayant :
    - `name` *(string)* : Nom de la province.
    - `chef_lieu` *(string)* : Chef-lieu de la province.
    - `departments` *(array)* : Liste des départements.
    - `population_count` *(object)* : Population par année.
- **`departments`** *(object)* :
  - `count` *(integer)* : Nombre total de départements.
- **`communes`** *(object)* :
  - `urban_count` *(integer)* : Nombre de communes urbaines.
  - `rural_count` *(integer)* : Nombre de communes rurales.
  - `villages` *(object)* :
    - `count` *(integer)* : Nombre total de villages.

---

## Exemple de données

### Exemple d'une région : Boucle du Mouhoun

```json
{
  "name": "Boucle du Mouhoun",
  "code_INSD": "02",
  "population_count": {
    "y_1985": 913713,
    "y_2019": 1898133
  },
  "area_km2": 34333.0,
  "capital": "Dédougou",
  "regional_councillors_count": 89,
  "provinces": {
    "count": 6,
    "details": [
      {
        "name": "Balé",
        "chef_lieu": "Boromo",
        "departments": ["Bagassi", "Bana", "Boromo", "Fara"]
      }
    ]
  },
  "departments": {
    "count": 47
  },
  "communes": {
    "urban_count": 6,
    "rural_count": 41,
    "villages": {
      "count": 1042
    }
  }
}
```

### Exemple d'une province : Balé

```json
{
  "name": "Balé",
  "chef_lieu": "Boromo",
  "departments": ["Bagassi", "Bana", "Boromo", "Fara"],
  "population_count": {
    "y_1985": 129323,
    "y_2002": 213526
  }
}
```

---

## Utilisation

### Objectifs

Ce fichier peut être utilisé pour :
1. **Recherche et analyse** : Études démographiques ou administratives.
2. **Applications** : Intégration dans des applications ou API géographiques.
3. **Visualisation** : Création de cartes interactives ou graphiques basés sur les données.

### Instructions

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/openundder/burkina-subdivision.git
   ```
2. **Accéder au fichier JSON** :
   - Ouvrez `regions.json` pour explorer les données.
3. **Chargement dans un programme** :
   - Utilisez une bibliothèque JSON comme `json` en Python ou `JSON.parse` en JavaScript.

---

## À propos des données

### Sources

Les données proviennent de sources publiques et fiables, incluant les rapports statistiques de l'Institut National de la Statistique et de la Démographie (INSD).

### Limites

- Les données de population ne sont pas disponibles pour toutes les années.
- Certaines informations peuvent nécessiter des mises à jour.

---

## Contribution

### Comment contribuer

1. Forkez ce dépôt.
2. Ajoutez ou corrigez des données.
3. Proposez une Pull Request avec une description détaillée des modifications.

---

## Licence

Ce projet est distribué sous licence **MIT**. 
La licence donne à toute personne recevant le logiciel (et ses fichiers) le droit illimité de l'utiliser, le copier, le modifier, le fusionner, le publier, le distribuer, le vendre et le « sous-licencier » (l'incorporer dans une autre licence). La seule obligation est d'incorporer la notice de licence et de copyright dans toutes les copies. 

---
