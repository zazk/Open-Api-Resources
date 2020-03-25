# Open-Api-Resources

Open and Free API resources for Research and Testing

- [SWAPI The Star Wars API](#swapi-the-star-wars-api)
- [ICNDB The internet Chuck Norris Database](#icndb-the-internet-chuck-norris-database)
- [Pokemon API](#pokemon-api)
- [DATA.POLICE.UK Police API Documentation](#datapoliceuk-police-api-documentation)
- [Google Books API](#google-books-api)

## Adding an API Resource

Send a pull-request which adds a file to the `_apis/` directory
with a new file representing the open api. The file should be named
with the api name with an `.md` extension (for
example, `pokemon-api.md`).

The contents of the file should use the following template:

```
---
name: "Pokemon API"
website: https://www.pokeapi.co/
API test: https://www.pokeapi.co/api/v2/pokemon/2/


description: Finally; all the Pokémon data you'll ever need, in one place, and easily accessible through a modern RESTful API.
use: For educational purposes # Optional, will default to website
---
```

## List

### SWAPI The Star Wars API

https://swapi.co/

_Example_

```
https://swapi.co/api/planets/1/
```

Response:

```javascript
{
    "name": "Tatooine",
    "rotation_period": "23",
    "orbital_period": "304",
    "diameter": "10465",
    "climate": "arid",
    "gravity": "1 standard",
    "terrain": "desert",
    "surface_water": "1",
    "population": "200000",
    "residents": [
        "https://swapi.co/api/people/1/",
        "https://swapi.co/api/people/2/",
        "https://swapi.co/api/people/4/"
    ],
    "films": [
        "https://swapi.co/api/films/5/",
        "https://swapi.co/api/films/4/"
    ],
    "created": "2014-12-09T13:50:49.641000Z",
    "edited": "2014-12-21T20:48:04.175778Z",
    "url": "https://swapi.co/api/planets/1/"
}
```

---

### ICNDB The internet Chuck Norris Database

http://www.icndb.com/api/

_Example_

```
http://api.icndb.com/jokes/random/2?limitTo=[nerdy]
```

Response:

```javascript
{
    "type": "success",
    "value": [
        {
            "id": 556,
            "joke": "Chuck Norris can write to an output stream.",
            "categories": [
                "nerdy"
            ]
        },
        {
            "id": 526,
            "joke": "No one has ever pair-programmed with Chuck Norris and lived to tell about it.",
            "categories": [
                "nerdy"
            ]
        }
    ]
}
```

---

### Pokemon API

Finally; all the Pokémon data you'll ever need, in one place, and easily accessible through a modern RESTful API.
https://www.pokeapi.co/

_Example_

```
https://www.pokeapi.co/api/v2/pokemon/2/
```

Response:

```javascript
{
	"name": "flying",
	"generation": {
		"url": "https://www.pokeapi.co/api/v2/generation/1/",
		"name": "generation-i"
	},
	"damage_relations": {
		"half_damage_from": [
			{
				"url": "https://www.pokeapi.co/api/v2/type/2/",
				"name": "fighting"
			}
		],
		"no_damage_from": [
			{
				"url": "https://www.pokeapi.co/api/v2/type/5/",
				"name": "ground"
			}
		],
		"half_damage_to": [
			{
				"url": "https://www.pokeapi.co/api/v2/type/6/",
				"name": "rock"
			}
		"double_damage_from": [
			{
				"url": "https://www.pokeapi.co/api/v2/type/6/",
				"name": "rock"
			}
		],
		"no_damage_to": [],
		"double_damage_to": [
			{
				"url": "https://www.pokeapi.co/api/v2/type/2/",
				"name": "fighting"
			}
		]
	},
	"game_indices": [
		{
			"generation": {
				"url": "https://www.pokeapi.co/api/v2/generation/1/",
				"name": "generation-i"
			},
			"game_index": 2
		}
	],
	"move_damage_class": {
		"url": "https://www.pokeapi.co/api/v2/move-damage-class/2/",
		"name": "physical"
	},
	"moves": [
		{
			"url": "https://www.pokeapi.co/api/v2/move/16/",
			"name": "gust"
		}
	],
	"id": 3,
	"names": [
		{
			"name": "ひこう",
			"language": {
				"url": "https://www.pokeapi.co/api/v2/language/1/",
				"name": "ja-Hrkt"
			}
		}
	]
}
```

---

### DATA.POLICE.UK Police API Documentation

The API provides a rich data source for information, including:
https://data.police.uk/docs/

- Neighbourhood team members
- Upcoming events
- Street-level crime and outcome data
- Nearest police stations
- The API is implemented as a standard JSON web service using HTTP GET and POST requests. Full request and response examples are provided in the documentation.

_Example_

```
https://data.police.uk/api/crimes-at-location?date=2017-02&location_id=884227
```

Response:

```javascript
[
  {
    category: "violent-crime",
    location_type: "Force",
    location: {
      latitude: "52.643950",
      street: {
        id: 884227,
        name: "On or near Abbey Gate"
      },
      longitude: "-1.143042"
    },
    context: "",
    outcome_status: {
      category: "Unable to prosecute suspect",
      date: "2017-02"
    },
    persistent_id:
      "4d83433f3117b3a4d2c80510c69ea188a145bd7e94f3e98924109e70333ff735",
    id: 54726925,
    location_subtype: "",
    month: "2017-02"
  }
];
```

---

### Google Books API

The Books API is a way to search and access that content, as well as to create and view personalization around that content.
https://developers.google.com/books/docs/overview

_Example_

```
https://www.googleapis.com/books/v1/volumes?q=flowers
```

Response:

```javascript
{
  "kind":"books#volumes",
  "totalItems":850,
  "items":[
    {
      "kind":"books#volume",
      "id":"gsK9jwEACAAJ",
      "etag":"BpEVTFG5f8Q",
      "selfLink":"https://www.googleapis.com/books/v1/volumes/gsK9jwEACAAJ",
      "volumeInfo":{
        "title":"El Lenguaje de Las Flores",
        "authors":[
          "Vanessa Diffenbaugh"
        ],
        "publisher":"Salamandra",
        "publishedDate":"2016",
        "description":"Inspirándose en el sofisticado código que la sociedad victoriana utilizaba para expresar sentimientos por medio de las flores, Vanessa Diffenbaugh narra el viaje emocional de una joven californiana que, marcada por una dolorosa historia personal..",
        "industryIdentifiers":[
          {
            "type":"ISBN_10",
            "identifier":"8498387477"
          },
          {
            "type":"ISBN_13",
            "identifier":"9788498387476"
          }
        ],
        "readingModes":{
          "text":false,
          "image":false
        },
        "pageCount":352,
        "printType":"BOOK",
        "categories":[
          "Fiction"
        ],
        "maturityRating":"NOT_MATURE",
        "allowAnonLogging":false,
        "contentVersion":"preview-1.0.0",
        "panelizationSummary":{
          "containsEpubBubbles":false,
          "containsImageBubbles":false
        },
        "imageLinks":{
          "smallThumbnail":"http://books.google.com/books/content?id=gsK9jwEACAAJ&printsec=frontcover&img=1&zoom=5&source=gbs_api",
          "thumbnail":"http://books.google.com/books/content?id=gsK9jwEACAAJ&printsec=frontcover&img=1&zoom=1&source=gbs_api"
        },
        "language":"es",
        "previewLink":"http://books.google.com.pe/books?id=gsK9jwEACAAJ&dq=flowers&hl=&cd=1&source=gbs_api",
        "infoLink":"http://books.google.com.pe/books?id=gsK9jwEACAAJ&dq=flowers&hl=&source=gbs_api",
        "canonicalVolumeLink":"https://books.google.com/books/about/El_Lenguaje_de_Las_Flores.html?hl=&id=gsK9jwEACAAJ"
      },
      "saleInfo":{
        "country":"PE",
        "saleability":"NOT_FOR_SALE",
        "isEbook":false
      },
      "accessInfo":{
        "country":"PE",
        "viewability":"NO_PAGES",
        "embeddable":false,
        "publicDomain":false,
        "textToSpeechPermission":"ALLOWED",
        "epub":{
          "isAvailable":false
        },
        "pdf":{
          "isAvailable":false
        },
        "webReaderLink":"http://play.google.com/books/reader?id=gsK9jwEACAAJ&hl=&printsec=frontcover&source=gbs_api",
        "accessViewStatus":"NONE",
        "quoteSharingAllowed":false
      },
      "searchInfo":{
        "textSnippet":"Inspirándose en el sofisticado código que la sociedad victoriana utilizaba para expresar sentimientos por medio de las flores, Vanessa Diffenbaugh narra el viaje emocional de una joven californiana que, marcada por una dolorosa historia ..."
      }
    }
  ]
}
```

### Cat Facts API

https://alexwohlbruck.github.io/cat-facts/docs/

_Example_

```
https://cat-fact.herokuapp.com/facts/random?animal_type=cat&amount=2
```

Response:

```javascript
[
  {
    used: false,
    source: "api",
    type: "cat",
    deleted: false,
    _id: "591f97a9ccb34a14d3f7dc8f",
    __v: 0,
    text:
      "Cats purr at the same frequency as an idling diesel engine, about 26 cycles per second.",
    updatedAt: "2020-01-02T02:02:48.616Z",
    createdAt: "2018-01-04T01:10:54.673Z",
    status: {
      verified: true,
      sentCount: 1
    },
    user: "5a9ac18c7478810ea6c06381"
  },
  {
    used: false,
    source: "api",
    type: "cat",
    deleted: false,
    _id: "591f98883b90f7150a19c262",
    __v: 0,
    text:
      "Miacis, the primitive ancestor of cats, was a small, tree-living creature of the late Eocene period, some 45 to 50 million years ago.",
    updatedAt: "2020-01-02T02:02:48.616Z",
    createdAt: "2018-01-04T01:10:54.673Z",
    status: {
      verified: true,
      sentCount: 1
    },
    user: "5a9ac18c7478810ea6c06381"
  }
];
```

### The Breaking Bad API ...Tread Lightly

https://breakingbadapi.com/

_Example_

```
https://www.breakingbadapi.com/api/characters?limit=2
```

Response:

```javascript
[
  {
    char_id: 1,
    name: "Walter White",
    birthday: "09-07-1958",
    occupation: ["High School Chemistry Teacher", "Meth King Pin"],
    img:
      "https://images.amcnetworks.com/amc.com/wp-content/uploads/2015/04/cast_bb_700x1000_walter-white-lg.jpg",
    status: "Presumed dead",
    nickname: "Heisenberg",
    appearance: [1, 2, 3, 4, 5],
    portrayed: "Bryan Cranston",
    category: "Breaking Bad",
    better_call_saul_appearance: []
  },
  {
    char_id: 2,
    name: "Jesse Pinkman",
    birthday: "09-24-1984",
    occupation: ["Meth Dealer"],
    img:
      "https://upload.wikimedia.org/wikipedia/en/thumb/f/f2/Jesse_Pinkman2.jpg/220px-Jesse_Pinkman2.jpg",
    status: "Alive",
    nickname: "Cap n' Cook",
    appearance: [1, 2, 3, 4, 5],
    portrayed: "Aaron Paul",
    category: "Breaking Bad",
    better_call_saul_appearance: []
  }
];
```
