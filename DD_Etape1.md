# MERISE - TD1 R3.10 Management des SI et des Projets

## Circuit
| Nom de l’attribut  | Type de données | Longueur | Clé       | Description            |
|---------------------|-----------------|----------|-----------|------------------------|
| ID_circuit          | integer         |          | primaire  | Identifiant du circuit |
| intitulé            | Varchar()       | 15       |           | Intitulé du voyage     |
| Date                | datetime        |          |           | Date du voyage         |
| Heure_depart        | datetime        |          |           | Heure du départ        |
| Heure_arrivee       | datetime        |          |           | Heure d’arrivée        |
| ville_depart        | Varchar()       | 15       |           | Ville de départ        |
| ville_arrivee       | Varchar()       | 15       |           | Ville d’arrivée        |
| transport           | Varchar()       | 10       |           | Moyen de transport     |

---

## Client
| Nom de l’attribut | Type de données | Longueur | Clé      | Description                  |
|-------------------|-----------------|----------|----------|------------------------------|
| ID_client         | integer         |          | primaire | Identifiant du client        |
| Prenom            | Varchar()       | 40       |          | Prénom du client             |
| Nom               | Varchar()       | 40       |          | Nom de famille du client     |
| Naissance         | datetime        |          |          | Date de naissance du client  |
| Adresse           | Varchar()       | 40       |          | Adresse du client            |
| CA                | integer         |          |          | Code d’agence                |

---

## Participants circuits
| Nom de l’attribut    | Type de données | Longueur | Clé                | Description                   |
|-----------------------|-----------------|----------|--------------------|-------------------------------|
| ID_circuit            | integer         |          | primaire/étrangère | Identifiant du circuit        |
| ID_client             | integer         |          | étrangère          | Identifiant du client         |
| ID_accompagnateur     | integer         |          | étrangère          | Identifiant de l’accompagnateur |
| prix_individuel       | integer         |          |                    | Prix individuel               |
| nombre_place          | integer         |          |                    | Nombre de place               |
| acompte               | integer         |          |                    | Acompte                       |
| deuxieme_versement    | integer         |          |                    | Deuxième versement            |
| remise                | integer         |          |                    | Remise                        |
| total                 | integer         |          |                    | Total                         |

---

## Accompagnateur
| Nom de l’attribut   | Type de données | Longueur | Clé      | Description                     |
|----------------------|-----------------|----------|----------|---------------------------------|
| ID_accompagnateur    | integer         |          | primaire | Identifiant de l’accompagnateur |
| Nom                  | Varchar()       | 40       |          | Nom de l’accompagnateur         |
| Prenom               | Varchar()       | 40       |          | Prénom de l’accompagnateur      |
| Adresse              | Varchar()       | 40       |          | Adresse de l’accompagnateur     |

---

## Ville
| Nom de l’attribut | Type de données | Longueur | Clé      | Description          |
|--------------------|-----------------|----------|----------|----------------------|
| nom_ville          | Varchar()       | 15       | primaire | Nom de la ville      |
| hotel              | Varchar()       | 15       | primaire | Nom de l’hôtel réservé |
| pays               | Varchar()       | 15       |          | Pays de la ville     |
