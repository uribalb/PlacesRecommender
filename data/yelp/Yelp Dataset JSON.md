## Yelp Dataset JSON

Each file is composed of a single object type, one JSON-object per-line.

Take a look at some examples to get you started: [https://github.com/Yelp/dataset-examples](https://github.com/Yelp/dataset-examples).

Note: the follow examples contain inline comments, which are technically not valid JSON. This is done here to simplify the documentation and explaining the structure, the JSON files you download will not contain any comments and will be fully valid JSON.

### business.json

Contains business data including location data, attributes, and categories.

```json
{
	"business_id": "tnhfDv5Il8EaGSXZGiuQGg",
	"name": "Garaje",
	"address": "475 3rd St",
	"city": "San Francisco",
	"state": "CA",
	"postal code": "94107",
	"latitude": 37.7817529521,
	"longitude": -122.39612197,
	"stars": 4.5,
	"review_count": 1198,
	"is_open": 1,
	"attributes": {
		"RestaurantsTakeOut": true,
		"BusinessParking": {
			"garage": false,
			"street": true,
			"validated": false,
			"lot": false,
			"valet": false
		}
	},
	"categories": ["Mexican", "Burgers", "Gastropubs"],
	"hours": {
		"Monday": "10:00-21:00",
		"Tuesday": "10:00-21:00",
		"Friday": "10:00-21:00",
		"Wednesday": "10:00-21:00",
		"Thursday": "10:00-21:00",
		"Sunday": "11:00-18:00",
		"Saturday": "10:00-21:00"
	}
}
```

### review.json

Contains full review text data including the user_id that wrote the review and the business_id the review is written for.

```json
{
	"review_id": "zdSx_SD6obEhz9VrW9uAWA",
	"user_id": "Ha3iJu77CxlrFm-vQRs_8g",
	"business_id": "tnhfDv5Il8EaGSXZGiuQGg",
	"stars": 4,
	"date": "2016-03-09",
	"text": "Great place to hang out after work: the prices are decent, and the ambience is fun. It's a bit loud, but very lively. The staff is friendly, and the food is good. They have a good selection of drinks.",
	"useful": 0,
	"funny": 0,
	"cool": 0
}
```

### user.json

User data including the user's friend mapping and all the metadata associated with the user.

```json
{
	"user_id": "Ha3iJu77CxlrFm-vQRs_8g",
	"name": "Sebastien",
	"review_count": 56,
	"yelping_since": "2011-01-01",
	"friends": ["wqoXYLWmpkEH0YvTmHBsJQ", "KUXLLiJGrjtSsapmxmpvTA", "6e9rJKQC3n0RSKyHLViL-Q"],
	"useful": 21,
	"funny": 88,
	"cool": 15,
	"fans": 1032,
	"elite": [2012, 2013],
	"average_stars": 4.31,
	"compliment_hot": 339,
	"compliment_more": 668,
	"compliment_profile": 42,
	"compliment_cute": 62,
	"compliment_list": 37,
	"compliment_note": 356,
	"compliment_plain": 68,
	"compliment_cool": 91,
	"compliment_funny": 435,
	"compliment_writer": 185,
	"compliment_photos": 254
}
```

### checkin.json

Checkins on a business.

```json
{
	"business_id": "tnhfDv5Il8EaGSXZGiuQGg", // string, 22 character business id, maps to business in business.json
	"date": "2016-04-26 19:49:16, 2016-08-30 18:36:57, 2016-10-15 02:45:18" // string which is a comma-separated list of timestamps for each checkin, each with format YYYY-MM-DD HH:MM:SS
}
```

### tip.json

Tips written by a user on a business. Tips are shorter than reviews and tend to convey quick suggestions.

```json
{
	"text": "Secret menu - fried chicken sando is da bombbbbbb",
	"date": "2014-05-10 15:25:05",
	"likes": 15,
	"business_id": "tnhfDv5Il8EaGSXZGiuQGg",
	"user_id": "456t54th54thgh54trh454"
}
```

### photo.json

Contains photo data including the caption and classification (one of "food", "drink", "menu", "inside" or "outside").

```json
{
	"photo_id": "tnhfDv5Il8EaGSXZGiuQGg",
	"caption": "The most amazing ramen ever",
	"label": ["food", "ramen"],
	"business_id": "tnhfDv5Il8EaGSXZGiuQGg"
}
```
