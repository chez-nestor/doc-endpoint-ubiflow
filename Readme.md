## Description du JSON retourné par l'API sur le endpoint Ubiflow:

### *Racine*
*hashmap* des chambres disponibles. Les clefs sont les identifiants uniques des
chambres et les valeurs sont des *hashmap* de type *Room*.

### type *Room*
*hashmap* contenant les clefs suivantes :

- `id` :
		*string* Identifiant universel unique (format uuid v4)
- `reference` :
		*string* Reference unique de la chambre (format indéfini)
- `type` :
		*string* Type de bien (toujours `room` → chambre)
- `contract` :
		*string* Type de contrat (toujours `rental` → location)
- `nameFr` :
		*string* Nom du bien en français
- `availableAt` :
		*string* Date de disponibilité du bien (format ISO 8601)
- `addressStreet` :
		*string* Numéro et nom de rue
- `addressCity` :
		*string* Ville
- `addressZip` :
		*string* Code postal
- `addressCountry` :
		*string* Pays
- `neighborhood` :
		*string* Quartier
- `latLng` :
		*string* Coordonnées GPS du bien (format DD Decimal Degrees)
- `floor` :
		*number* Étage de l'appartement
- `roomFloorArea` :
		*number* Surface de la chambre (en m²)
- `roomCount` :
		*number* Nombre de chambres dans l'appartement
- `apartmentFloorArea` :
		*number* Surface de l'appartement (en m²)
- `currentPrice` :
		*number* Prix actuel de la chambre (en €)
- `serviceFees` :
		*number* Frais provisionels - eau, électricité, internet, gaz (en €)
- `agencyFeesDescriptionFr` :
		*string* Description des frais d'agence (prix minimum du pack-logement) en français
- `fullDescriptionFr` :
		*string* Description de la chambre, du logement et du quartier + explication des frais d'agence en français
- `canonicalUrlFr` :
		*string* Url de la page de description du bien sur le site Chez Nestor
- `gallery` :
		*array* contenant uniquement des *string* indiquant les urls de chaque image de la galerie. Pour des résons techniques, la description de l'image est inclue à la fin de l'url : "https://www.chez-nestor.com/…&alt=description+de+la+photo"

