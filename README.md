# RecipeMaster - Spring Boot Application to retrieve and store recipe details to database 

## Overview 

This Spring Boot application provides a restful API to retrieve the stored Recipe and allow user to add new Recipe. 
This also provides REST API to search recipes based on title and recipe categories 
This application can deployed easily and stores data in MYSQL database

## Prerequisites

-java Development Kit (JDK) 17 or higher
-Apache Maven 4.0.0 or higher
-Docker to connect mysql:8-oracle image or higher

### Running the Application
To run the application need to create a docker image of mysql DB using the following command : 

docker run --name recipe-master-mysql -p 51877 -e MYSQL_ROOT_PASSWORD={password} -d mysql:8-oracle

This will create a docker image name recipe-master-mysql and create a Database name mysql

Build and run the application using the following command : 

mvn clean install 
java -jar /target/recipemaster-0.0.1-SNAPSHOT.jar

The application will start on port 8080

### API Documentation 
Swagger documentation has been created for the RestAPI , which is available at :
http://localhost:8080/swagger-ui/index.html

Following REST API endpoints are being hosted 

** `Get /recipes` ** 

Response 

`HTTP Status 200 OK `

Body 

```{
    "content": [
        {
            "id": 1,
            "title": "30 Minute Chili",
            "yeild": 6,
            "category": [
                {
                    "name": "Side dish"
                },
                {
                    "name": "Chili"
                }
            ],
            "ingredientslist": [
                {
                    "ingredient_name": "Ground chuck or lean ground; beef",
                    "quantity": 1.0,
                    "unit": "pound"
                },
                {
                    "ingredient_name": "Onion; large, chopped",
                    "quantity": 1.0,
                    "unit": ""
                },
                {
                    "ingredient_name": "Kidney beans; (12 oz)",
                    "quantity": 1.0,
                    "unit": "can"
                },
                {
                    "ingredient_name": "Tomato soup; undiluted",
                    "quantity": 1.0,
                    "unit": "can"
                },
                {
                    "ingredient_name": "Salt",
                    "quantity": 1.0,
                    "unit": "teaspoon"
                },
                {
                    "ingredient_name": "Chili powder; (or to taste)",
                    "quantity": 1.0,
                    "unit": "tablespoon"
                },
                {
                    "ingredient_name": "Hot pepper sauce; to taste",
                    "quantity": 0.0,
                    "unit": ""
                }
            ],
            "recipeDirection": [
                {
                    "id": 1,
                    "steps": "Brown the meat in a little butter and cook until the meat is brown -- about 10 minutes. Add all other ingredients and let simmer for 30 minutes. Your choice of hot sauce may be added to taste. Recipe by: MasterCook Archives Posted to recipelu-digest Volume 01 Number 577 by Rodeo46898 &lt;Rodeo46898@aol.com&gt; on Jan 22, 1998"
                }
            ]
        },
        {
            "id": 2,
            "title": "Amaretto Cake",
            "yeild": 1,
            "category": [
                {
                    "name": "Liquor"
                },
                {
                    "name": "Cakes"
                },
                {
                    "name": "Cake mixes"
                }
            ],
            "ingredientslist": [
                {
                    "ingredient_name": "Toasted Almonds; chopped",
                    "quantity": 1.5,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Yellow cake mix; no pudding",
                    "quantity": 1.0,
                    "unit": "package"
                },
                {
                    "ingredient_name": "Vanilla instant pudding",
                    "quantity": 1.0,
                    "unit": "package"
                },
                {
                    "ingredient_name": "Eggs",
                    "quantity": 4.0,
                    "unit": ""
                },
                {
                    "ingredient_name": "Vegetable oil",
                    "quantity": 0.5,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Amaretto",
                    "quantity": 0.5,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Almond extract",
                    "quantity": 1.0,
                    "unit": "teaspoon"
                },
                {
                    "ingredient_name": "Sugar",
                    "quantity": 0.5,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Water",
                    "quantity": 0.25,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Butter",
                    "quantity": 2.0,
                    "unit": "tablespoon"
                },
                {
                    "ingredient_name": "Amaretto",
                    "quantity": 0.25,
                    "unit": "cups"
                },
                {
                    "ingredient_name": "Almond extract",
                    "quantity": 0.5,
                    "unit": "teaspoons"
                }
            ],
            "recipeDirection": [
                {
                    "id": 2,
                    "steps": "Sprinkle 1 cup almonds into bottom of a well-greased       and floured 10\" tube pan; set aside Combine cake mix,     pudding mix, eggs, oil, water, amaretto, and almond extract in a mixing bowl; beat on low speed of an electric mixer til dry ingredients are moistened. Increase speed to medium, and beat 4 minutes. Stir in      remaining 1/2cup almonds. Pour batter into prepared tube pan. Bake at 325~ for 1 hour or til a wooden pick inserted in center comes out clean. Cool cake in pan 10-15 minutes; remove from pan, and cool completely.Combine sugar, water, and butter in a small saucepan; bring to a boil. Reduce heat to medium and gently boil 4-5 minutes, stirring occasionally, until sugar dissolves. Remove from heat, and cool 15 minutes. Stir in amaretto and almond extract. Punch holes in top of cake with a wooden pick slowly spoon glaze on top of cake, allowing glaze to absorb in cake. Posted to MC-Recipe Digest V1 #263 Date: Sun, 27 Oct 1996 20:04:57 +0000 From: Cheryl Gimenez &lt;clgimenez@earthlink.net&gt;"
                }
            ]
        },
        {
            "id": 3,
            "title": "Another Zucchini Dish",
            "yeild": 6,
            "category": [
                {
                    "name": "Microwave"
                },
                {
                    "name": "Vegetables"
                }
            ],
            "ingredientslist": [
                {
                    "ingredient_name": "Zucchini; cubed 1/2 \"",
                    "quantity": 1.0,
                    "unit": "pound"
                },
                {
                    "ingredient_name": "Butter or margarine",
                    "quantity": 3.0,
                    "unit": "tablespoons"
                },
                {
                    "ingredient_name": "Eggs; beaten",
                    "quantity": 3.0,
                    "unit": ""
                },
                {
                    "ingredient_name": "Jar pimentos; 2 1/2 oz, diced",
                    "quantity": 1.0,
                    "unit": ""
                },
                {
                    "ingredient_name": "Cheddar cheese; shredded",
                    "quantity": 1.0,
                    "unit": "cup"
                },
                {
                    "ingredient_name": "French fried onion rings 3 oz.",
                    "quantity": 1.0,
                    "unit": "can"
                }
            ],
            "recipeDirection": [
                {
                    "id": 3,
                    "steps": "Place zucchini and butter in a 2 quart casserole. Cover with plastic wrap. Microwave at high (100%) until tender crisp, 4 to 5 minutes. Stir in egg, pimentos and cheese. Blend well. Cover with plastic wrap. Microwave at medium (50%) until eggs are set, 10 toll minutes. Sprinkle onion rings on top. Microwave at medium (50%) until onion rings are heated, 2 to 2 1/2 minutes. Makes 6 servings.\n Recipe by: diane@keyway.net \n Posted to recipelu-digest Volume 01 Number 217 by \"Diane Geary\" &lt;diane@keyway.net&gt; on Nov 7, 1997"
                }
            ]
        }
    ],
    "pageable": {
        "sort": {
            "empty": true,
            "unsorted": true,
            "sorted": false
        },
        "offset": 0,
        "pageNumber": 0,
        "pageSize": 20,
        "paged": true,
        "unpaged": false
    },
    "totalPages": 1,
    "totalElements": 3,
    "last": true,
    "size": 20,
    "number": 0,
    "sort": {
        "empty": true,
        "unsorted": true,
        "sorted": false
    },
    "numberOfElements": 3,
    "first": true,
    "empty": false
} 
```
The Get recipe API supports search string and pagination 

** ```GET /recipes?title=30 Minute Chili` **

Response
`HTTP Status 200 OK`
Body

```{
    "id": 1,
    "title": "30 Minute Chili",
    "yeild": 6,
    "category": [
        {
            "name": "Side dish"
        },
        {
            "name": "Chili"
        }
    ],
    "ingredientslist": [
        {
            "ingredient_name": "Ground chuck or lean ground; beef",
            "quantity": 1.0,
            "unit": "pound"
        },
        {
            "ingredient_name": "Onion; large, chopped",
            "quantity": 1.0,
            "unit": ""
        },
        {
            "ingredient_name": "Kidney beans; (12 oz)",
            "quantity": 1.0,
            "unit": "can"
        },
        {
            "ingredient_name": "Tomato soup; undiluted",
            "quantity": 1.0,
            "unit": "can"
        },
        {
            "ingredient_name": "Salt",
            "quantity": 1.0,
            "unit": "teaspoon"
        },
        {
            "ingredient_name": "Chili powder; (or to taste)",
            "quantity": 1.0,
            "unit": "tablespoon"
        },
        {
            "ingredient_name": "Hot pepper sauce; to taste",
            "quantity": 0.0,
            "unit": ""
        }
    ],
    "recipeDirection": [
        {
            "id": 1,
            "steps": "Brown the meat in a little butter and cook until the meat is brown -- about 10 minutes. Add all other ingredients and let simmer for 30 minutes. Your choice of hot sauce may be added to taste. Recipe by: MasterCook Archives Posted to recipelu-digest Volume 01 Number 577 by Rodeo46898 &lt;Rodeo46898@aol.com&gt; on Jan 22, 1998"
        }
    ]
}
```
** `GET /recipes?recipes?category=Cakes` ** 
```
Response 
`HTTP 200 OK`
Body 

```[
    {
        "id": 2,
        "title": "Amaretto Cake",
        "yeild": 1,
        "category": [
            {
                "name": "Liquor"
            },
            {
                "name": "Cakes"
            },
            {
                "name": "Cake mixes"
            }
        ],
        "ingredientslist": [
            {
                "ingredient_name": "Toasted Almonds; chopped",
                "quantity": 1.5,
                "unit": "cups"
            },
            {
                "ingredient_name": "Yellow cake mix; no pudding",
                "quantity": 1.0,
                "unit": "package"
            },
            {
                "ingredient_name": "Vanilla instant pudding",
                "quantity": 1.0,
                "unit": "package"
            },
            {
                "ingredient_name": "Eggs",
                "quantity": 4.0,
                "unit": ""
            },
            {
                "ingredient_name": "Vegetable oil",
                "quantity": 0.5,
                "unit": "cups"
            },
            {
                "ingredient_name": "Amaretto",
                "quantity": 0.5,
                "unit": "cups"
            },
            {
                "ingredient_name": "Almond extract",
                "quantity": 1.0,
                "unit": "teaspoon"
            },
            {
                "ingredient_name": "Sugar",
                "quantity": 0.5,
                "unit": "cups"
            },
            {
                "ingredient_name": "Water",
                "quantity": 0.25,
                "unit": "cups"
            },
            {
                "ingredient_name": "Butter",
                "quantity": 2.0,
                "unit": "tablespoon"
            },
            {
                "ingredient_name": "Amaretto",
                "quantity": 0.25,
                "unit": "cups"
            },
            {
                "ingredient_name": "Almond extract",
                "quantity": 0.5,
                "unit": "teaspoons"
            }
        ],
        "recipeDirection": [
            {
                "id": 2,
                "steps": "Sprinkle 1 cup almonds into bottom of a well-greased       and floured 10\" tube pan; set aside Combine cake mix,     pudding mix, eggs, oil, water, amaretto, and almond extract in a mixing bowl; beat on low speed of an electric mixer til dry ingredients are moistened. Increase speed to medium, and beat 4 minutes. Stir in      remaining 1/2cup almonds. Pour batter into prepared tube pan. Bake at 325~ for 1 hour or til a wooden pick inserted in center comes out clean. Cool cake in pan 10-15 minutes; remove from pan, and cool completely.Combine sugar, water, and butter in a small saucepan; bring to a boil. Reduce heat to medium and gently boil 4-5 minutes, stirring occasionally, until sugar dissolves. Remove from heat, and cool 15 minutes. Stir in amaretto and almond extract. Punch holes in top of cake with a wooden pick slowly spoon glaze on top of cake, allowing glaze to absorb in cake. Posted to MC-Recipe Digest V1 #263 Date: Sun, 27 Oct 1996 20:04:57 +0000 From: Cheryl Gimenez &lt;clgimenez@earthlink.net&gt;"
            }
        ]
    }
]```

**`GET /categories` **
The API retrieves a List of all the recipe category available in the Database 

Response 

`HTTPS 200 Ok`

```Body 
[
    {
        "name": "Side dish"
    },
    {
        "name": "Chili"
    },
    {
        "name": "Liquor"
    },
    {
        "name": "Cakes"
    },
    {
        "name": "Cake mixes"
    },
    {
        "name": "Microwave"
    },
    {
        "name": "Vegetables"
    }
]```

** Save Recipe to Database 

** `Post /recipes`**
```content-Type =application/json

```json Request 

{
  "title": "Cheesy Zucchini Dish",
  "yeild":6,
  "category":[{"name":"Grilled"},{"name":"Vegetables"}],
  "ingredientslist":[{"quantity":1,"unit":"pound","ingredient_name":"Zucchini; cubed 1/2 \""},
                     {"quantity":3,"unit":"tablespoons","ingredient_name":"Butter or margarine"},
                     {"quantity":3,"unit":"","ingredient_name":"Eggs; beaten"},
                     {"quantity":1,"unit":"","ingredient_name":"Jar pimentos; 2 1/2 oz, diced"},
                     {"quantity":2,"unit":"cup","ingredient_name":"Cheddar cheese; shredded"},
                     {"quantity":1,"unit":"can","ingredient_name":"French fried onion rings 3 oz."}],
  "recipeDirection":[{"steps":"Place zucchini and butter in a 2 quart casserole. Cover with plastic wrap. Microwave at high (100%) until tender crisp, 4 to 5 minutes. Stir in egg, pimentos and cheese. Blend well. Cover with plastic wrap. Microwave at medium (50%) until eggs are set, 10 toll minutes. Sprinkle onion rings on top. grill until onion rings are heated, 2 to 2 1/2 minutes. Makes 6 servings.\n Recipe by: diane@keyway.net \n Posted to recipelu-digest Volume 01 Number 217 by \"Diane Geary\" &lt;diane@keyway.net&gt; on Nov 7, 1997"}]
  
}

```
Response 

```
HTTP 201 Created 
Location http://localhost:8080/recipes/102 
```
Body 

```{
    "id": 102,
    "title": "Cheesy Zucchini Dish",
    "yeild": 6,
    "category": [
        {
            "name": "Grilled"
        },
        {
            "name": "Vegetables"
        }
    ],
    "ingredientslist": [
        {
            "ingredient_name": "Zucchini; cubed 1/2 \"",
            "quantity": 1.0,
            "unit": "pound"
        },
        {
            "ingredient_name": "Butter or margarine",
            "quantity": 3.0,
            "unit": "tablespoons"
        },
        {
            "ingredient_name": "Eggs; beaten",
            "quantity": 3.0,
            "unit": ""
        },
        {
            "ingredient_name": "Jar pimentos; 2 1/2 oz, diced",
            "quantity": 1.0,
            "unit": ""
        },
        {
            "ingredient_name": "Cheddar cheese; shredded",
            "quantity": 2.0,
            "unit": "cup"
        },
        {
            "ingredient_name": "French fried onion rings 3 oz.",
            "quantity": 1.0,
            "unit": "can"
        }
    ],
    "recipeDirection": [
        {
            "id": 4,
            "steps": "Place zucchini and butter in a 2 quart casserole. Cover with plastic wrap. Microwave at high (100%) until tender crisp, 4 to 5 minutes. Stir in egg, pimentos and cheese. Blend well. Cover with plastic wrap. Microwave at medium (50%) until eggs are set, 10 toll minutes. Sprinkle onion rings on top. grill until onion rings are heated, 2 to 2 1/2 minutes. Makes 6 servings.\n Recipe by: diane@keyway.net \n Posted to recipelu-digest Volume 01 Number 217 by \"Diane Geary\" &lt;diane@keyway.net&gt; on Nov 7, 1997"
        }
    ]
} ```





