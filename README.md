# Welcome to this README :stars:

***

## Together we are going to go through several essential concepts on Ruby on Rails :tram:

![Ruby on rails](http://rubyonrails.org/images/rails-logo.svg)

***

 * What is the difference between a static and a dynamic website ?
 * The MVC architecure
 * The Routes
 * Database
 * GET & POST requests
 * The migration of data
 * The relationship between the Database model
 * The CRUD

 ***

 ### Let us start with the difference between a static and a dynamic website :rocket: :

 ![Dynamic vs Static](http://whatismyip.network/wp-content/uploads/2016/08/Static-IP-vs-Dynamic-IP-What-is-the-Difference.jpg)

* **Static website** :eight_pointed_black_star:

A static website is, as its name indicates, the result of a query by the client (i.e. the Browser) to the server. <br>
The result is expected to be the same for every clients (unless the webmaster decides to change anything on the website).
A good example of a static website is the following : [Static website](mathieubrunpicard.github.io)

:warning: A static website, does not mean that there is no animation on the webpage. <br>
You can find video :movie_camera:, music :musical_score: or flash animations :dizzy: on a static website.

* **Dynamic website** :sparkle:

Conversely, a dynamic website does not display the same page for every user.
The displayed page can change based on several parameteres, for instance the data provided by the user or the hour of the connexion. Then, these data will create queries directly to the database of the website (i.e. the server) and these queries will generate a specific html page that will be display in the client.<br>
A good example of dynamic website is [Facebook](http://facebook.com): every user has a different feed in the homepage.


- [X] What is the difference between a static and a dynamic website ?

### Let us focus on the MVC Architecture :mag:

The MVC Architecture is composed of three things : <br>
1. Model
2. View
3. Controller

![MVC](https://i.stack.imgur.com/xjBSZ.png)

This software architectural pattern allows a more flexible coding, since the data, the interface and the processing are thought as a whole but designed separately.

* **The Model** :bulb:

The model is the central element and consists of managing the data, the logic and the rules of the application.

* **The View** :mag_right:

It consists in the User Interface displayed on the client. It is the representation of the information for the user.

* **The Controller** :video_game:

The controller is the bridge between the model and the view. It receives the input from the user, converts it in a request for the model or a command for the view.

 - [X] The MVC architecure

 ### Routes :oncoming_automobile:

 In rails, the routes are a way to indicate what action the controller is expected to do when the client makes a request on a specific HTTP adress.

For instance in your routes.rb file you can add :

```Ruby
resources :articles
```
This will add six different routes when you arrive on the url :
< myurl/articles
as seen in the table below in the section GET/POST.

The following command shows all the routes of the current rails application:
```Ruby
  rails routes
 ```

 - [X] The Routes

 ### Database :dvd:

 ![Database](https://cp-mlxprod-static.microsoft.com/014929-1004/en-us/thumbnail.png)

 **What is a Database ?**

 The answer is quite simple : it is an organized set of data (you can think of a big spreadsheet). </br>
 To give you an example, on your smartphone, your contact list is a database. Every phone number is sorted using a primary key (the firstname of the contact) and maybe a secondary key (the lastname).

 In a nutshell, it allows the user to structure its data and easily find a **relevant** and **specific** piece of information.

 To follow our article example set above, if I want to create a database on rails I will type the following command in my terminal:
 ```Ruby
 rails generate model article
 ```
 It will generate a database of articles. Then I will precise what element I will be looking at (Title, subtitle, body) like that :

 ```Ruby
 t.string :title
  t.string :subtitle
t.text :body
```
In the Article database, for each Article, I will have these three parameters (and several others not mentionned here such as the unique id of the article for instance).


 - [X] Database

  ### GET & POST request :postbox:

  **GET** and **POST** are both **REST** methods. REST stands for Representational State Transfer. REST defines HTTP methods that allow the user's browser to interact with our server code.

  The table below summarizes the GET & POST requests.

  HTTP Verb | Path | Controller#Action |  Used for
------------ | ------------- | ------------- | -------------
GET | /articles/new | articles#new |  return an HTML form for creating the article
POST | /articles | articles#create |  create the new article
GET | /articles | articles#show |  display the specific article
GET | /articles/edit | articles#edit |  return an HTML form for editing the article
PATCH/PUT | /articles/ | articles#update |  update the specific article
DELETE | /articles/ | articles#delete |  delete the specific article


 - [X] GET & POST requests

 ### The migration of data :globe_with_meridians:

 As stated in the Database part, when we set a database, in order to use it the user should type the following command line in its consol:

 ```Ruby
  rails db:migrate
 ```
From this, we understand that the concept of migration allows the user either to create or update its database.
You can migrate several type of data and you can update

 - [X] The migration of data

 ### Relationship between the Database model :couple:

Often in a project, you have several databases and they are all related.
To pursue our example with the smartphone above, you can have your contact list and also several accounts or services linked to your phone number (facebook account, email account, etc..).
If you want to link two models you will have to precise in the rail app who belongs to who. The example below is based on blog articles and comments on each articles.

You will need to add the below code in the article.rb

```Ruby
has_many : comments
```

and these lines below in comment.rb to link both models.

```Ruby
t.references :article, foreign_key: true
belongs_to :articles
```

 - [X] The relationship between the Database model

 ### The CRUD :closed_lock_with_key:

 ![CRUD](https://static1.squarespace.com/static/555dc243e4b0fa866e3e41a9/t/5926bcdf9de4bbba0f69cd10/1495710948784/)

 CRUD's meaning is the following :

 * Create: <br>
 Allows the user to create content
 > PUT or POST in HTTP
 * Read: <br>
  Allows the user to read the content
  > GET in HTTP
 * Update: <br>
  Allows the user to update the content
  > PUT / POST / PATCH in HTTP
 * Destroy: <br>
 Allow the user to delete the content
 > DELETE in HTTP

 These are the four basic fonctions that are found in every database.
 - [X] The CRUD

If I am not clear on a topic or if you just want to speak with me, do not hesitate to contact me on slack : @Mathieu :baby_chick:

![My Github](https://github.com/mathieubrunpicard/)


