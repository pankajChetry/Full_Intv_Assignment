# Fullthrottle_Intv_Assignment

-- Intially created environmet for djano project as env and then activated env 
-- Installed django, django restframework and other dependencies. Please find all requirement details in requirements.txt
-- Created project as my_activity_period inside the environment and then created new app as my_api inside               my_acticity_period.
-- added my_api and rest_framework inside installed apps in settings.py file of project directory i.e my_acticity_period and made initial migration.
-- then created a superuser as Pankaj Chetry and password 1234
-- After all this step our environment setup is done.
-- NOW starting with our project we created Two models as Musician and Album as in models.py file of my_api. 
-- Again do the migrations and migrate the model to database.
-- then added a serilizer.py file in my_api directory and created serializers for our models as MusicianSerializer and AlbumSerializer.
-- Now in the views.py file of my_api add all the generics views as MusicianListView, MusicianView, AlbumListView and AlbumView.
-- Once the views are ready, add urls to the urls.py file in your project folder.
-- run the local server.
-- post the data from any platform as i am using postman using the url "http://localhost:8000/musicians/", demo data as given below.

1.
{
    "first_name": "ganesh",
    "last_name": "xeno",
    "instrument": "Guitar",
    "album_musician": [
        {
            "name": "NEO",
            "release_date": "2017-07-07",
            "num_stars": 5
        },
        {
            "name": "NEO 2",
            "release_date": "2017-07-22",
            "num_stars": 4
        }
    ]
}

2.
{
    "first_name": "Harish",
    "last_name": "Sharma",
    "instrument": "Flute",
    "album_musician": [
        {
            "name": "Sunshine",
            "release_date": "2017-06-09",
            "num_stars": 3
        },
        {
            "name": "Emptiness",
            "release_date": "2017-07-02",
            "num_stars": 5
        }
    ]
}

-- get the data back by using get method in the same url "http://localhost:8000/musicians/". Output given below.

output--
[
    {
        "id": 1,
        "first_name": "ganesh",
        "last_name": "xeno",
        "instrument": "Guitar",
        "album_musician": [
            {
                "id": 1,
                "artist": 1,
                "name": "NEO",
                "release_date": "2017-07-07",
                "num_stars": 5
            },
            {
                "id": 2,
                "artist": 1,
                "name": "NEO 2",
                "release_date": "2017-07-22",
                "num_stars": 4
            }
        ]
    },
    {
        "id": 2,
        "first_name": "Harish",
        "last_name": "Sharma",
        "instrument": "Flute",
        "album_musician": [
            {
                "id": 3,
                "artist": 2,
                "name": "Sunshine",
                "release_date": "2017-06-09",
                "num_stars": 3
            },
            {
                "id": 4,
                "artist": 2,
                "name": "Emptiness",
                "release_date": "2017-07-02",
                "num_stars": 5
            }
        ]
    }
]

-- Other urls and views are also added to update, delete and destroy data in the database.
-- other end points
* "http://localhost:8000/api/musicians/"
* "http://localhost:8000/albums/"
* "http://localhost:8000/api/albums/"
-- Tried my best to create and display the nested json data using django rest framework, hope to get more task as same.
-- Thank you