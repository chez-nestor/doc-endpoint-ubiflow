## Description du JSON retourné par l'API sur le endpoint Ubiflow:

### *Racine*
*hashmap* contenant la clef suivante :

- `rooms` :
		*array* contenant uniquement des *hashmap* de type *Room*

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
- `name` :
		*hashmap* de type *i18n* Nom du bien
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
- `housingPacks` :
		*array* contenant uniquement des *number* Prix des différents packs-logement
- `agencyFeesDescription` :
		*hashmap* de type *i18n* Description des frais d'agence (prix minimum du pack-logement)
- `neighborhoodDescription` :
		*hashmap* de type *i18n* Description du quartier
- `apartmentDescription` :
		*hashmap* de type *i18n* Description de l'appartment
- `roomDescription` :
		*hashmap* de type *i18n* Description de la chambre
- `canonicalUrl` :
		*string* Url de la page de description du bien sur le site Chez Nestor
- `gallery` :
		*array* contenant uniquement des *hashmap* de type *Picture*
- `beds` :
		*string* référence vers l'enum `beds`
- `room-features-xxx`, `apartment-features-xxx` :
		*array* de *string* références vers les enums correspondants
		
### type *Picture*
*hashmap* contenant les clefs suivantes :

- `alt` :
		*string* référence vers l'enum `pictures-alts`
- `url` :
		*string* Url de la photo

### type *i18n*
*hashmap* contenant des textes traduits dans différentes locales (`fr-FR`, et éventuellement `en-US`)
