# merise - td1 r3.10 management des si et des projets
Pour l’épuration du dictionnaire, nous avons procédé de la manière suivante :
lors de la création de notre dictionnaire, nous nous sommes assurés d’optimiser la base de données en ajoutant directement les attributs nécessaires et éviter les doublons.
Concernant l’épuration, nous avons veillé à retirer les accents ainsi que les majuscules afin d’uniformiser la structure.

## circuit
| nom_attribut      | type_donnees | longueur | cle                 | description              |
|-------------------|--------------|----------|---------------------|--------------------------|
| id_circuit        | integer      |          | primaire            | identifiant du circuit   |
| intitule          | varchar()    | 15       |                     | intitule du voyage       |
| date              | datetime     |          |                     | date du voyage           |
| heure_depart      | datetime     |          |                     | heure du depart          |
| heure_arrivee     | datetime     |          |                     | heure d'arrivee          |
| ville_depart      | varchar()    | 15       |                     | ville de depart          |
| ville_arrivee     | varchar()    | 15       |                     | ville d'arrivee          |
| transport         | varchar()    | 10       |                     | moyen de transport       |

---

## client
| nom_attribut | type_donnees | longueur | cle      | description                |
|--------------|--------------|----------|----------|----------------------------|
| id_client    | integer      |          | primaire | identifiant du client      |
| prenom       | varchar()    | 40       |          | prenom du client           |
| nom          | varchar()    | 40       |          | nom de famille du client   |
| naissance    | datetime     |          |          | date de naissance du client|
| adresse      | varchar()    | 40       |          | adresse du client          |
| ca           | integer      |          |          | code d'agence              |

---

## participants_circuits
| nom_attribut       | type_donnees | longueur | cle                 | description                    |
|--------------------|--------------|----------|---------------------|--------------------------------|
| id_circuit         | integer      |          | primaire/etrangere  | identifiant du circuit         |
| id_client          | integer      |          | etrangere           | identifiant du client          |
| id_accompagnateur  | integer      |          | etrangere           | identifiant de l'accompagnateur|
| prix_individuel    | integer      |          |                     | prix individuel                |
| nombre_place       | integer      |          |                     | nombre de place                |
| acompte            | integer      |          |                     | acompte                        |
| deuxieme_versement | integer      |          |                     | deuxieme versement             |
| remise             | integer      |          |                     | remise                         |
| total              | integer      |          |                     | total                          |

---

## accompagnateur
| nom_attribut      | type_donnees | longueur | cle      | description                    |
|-------------------|--------------|----------|----------|--------------------------------|
| id_accompagnateur | integer      |          | primaire | identifiant de l'accompagnateur|
| nom               | varchar()    | 40       |          | nom de l'accompagnateur        |
| prenom            | varchar()    | 40       |          | prenom de l'accompagnateur     |
| adresse           | varchar()    | 40       |          | adresse de l'accompagnateur    |

---

## ville
| nom_attribut | type_donnees | longueur | cle      | description         |
|--------------|--------------|----------|----------|---------------------|
| nom_ville    | varchar()    | 15       | primaire | nom de la ville     |
| hotel        | varchar()    | 15       | primaire | nom de l'hotel      |
| pays         | varchar()    | 15       |          | pays de la ville    |
