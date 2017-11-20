# Open-Api-Resources
Open and Free API resources for Research and Testing


Adding an API Resource
-------------------

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

*Example*
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

### ICNDB The internet Chuck Norris Database
http://www.icndb.com/api/

*Example*
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

### Pokemon API
Finally; all the Pokémon data you'll ever need, in one place, and easily accessible through a modern RESTful API.
https://www.pokeapi.co/

*Example*
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