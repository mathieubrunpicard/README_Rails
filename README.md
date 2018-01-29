# Welcome to this README

***

## Together we are going to go through several essential concepts on Ruby on Rails

![Ruby on rails](http://rubyonrails.org/images/rails-logo.svg)

***

 - [ ] What is the difference between a static and a dynamic website ?
 - [ ] The MVC architecure
 - [ ] The Routes
 - [ ] Database
 - [ ] GET & POST requests
 - [ ] The migration of data
 - [ ] The relationship between the Database model
 - [ ] The CRUD

 ***

 ### Let us start with the difference between a static and a dynamic website :rocket: :

 ![Dynamic vs Static](http://whatismyip.network/wp-content/uploads/2016/08/Static-IP-vs-Dynamic-IP-What-is-the-Difference.jpg)

* **Static website**

A static website is, as its name indicates, the result of a query by the client (i.e. the Browser) to the server. <br>
The result is expected to be the same for every clients (unless the webmaster decides to change anything on the website).
A good example of a static website is the following : [Static website](mathieubrunpicard.github.io)

:warning: :A static website, does not mean that there is no animation on the webpage. <br>
You can find video :movie_camera:, music :musical_score: or animations on a static website.

* **Dynamic website**

Conversely, a dynamic website does not display the same page for every user.
The displayed page can change based on several parameteres, for instance the data provided by the user or the hour of the connexion. Then, these data will create queries directly to the database of the website (i.e. the server) and these queries will generate a specific html page that will be display in the client.<br>
A good example of dynamic website is [Facebook](http://facebook.com).


- [X] What is the difference between a static and a dynamic website ?

### Let us focus on the MVC Architecture :mag:

The MVC Architecture is composed of three things : <br>
1. Model
2. View
3. Controller

![MVC](https://i.stack.imgur.com/xjBSZ.png)

This architecture allows a more flexible coding, since the data, the interface and the processing are thought as a whole but design separately.

* **The Model** :bulb:

The model is the central element and consists of managing the data, the logic and the rules of the application.

* **The View** :mag_right:

It consists in the User Interface displayed on the client. It is the representation of the information for the user.

* **The Controller** :video_game:

The controller is the bridge between the model and the view. It receives the input from the user, converts it in a request for the model or a command for the view.

 - [X] The MVC architecure

 ### Routes :oncoming_automobile:

 In rails, the routes are a way to indicate what action the controller is expected to do when the client make a request on a specific HTTP adress.

For instance in your routes.rb file you can add :

```Ruby
resources :articles
```
This will add six different routes when you arrive on the url : < myurl/articles as seen in the table below:

HTTP Verb | Path | Controller#Action |  Used for
------------ | ------------- | ------------- | -------------
GET | /articles/new | articles#new |  return an HTML form for creating the article
POST | /articles | articles#create |  create the new article
GET | /articles | articles#show |  display the specific article
GET | /articles/edit | articles#edit |  return an HTML form for editing the article
PATCH/PUT | /articles/ | articles#update |  update the specific article
DELETE | /articles/ | articles#delete |  delete the specific article

 - [X] The Routes

 ### Database :dvd:

 - [X] Database

  ### GET & POST request :postbox:
 - [X] GET & POST requests

 ### The migration of data :ship:

 - [X] The migration of data

 ### Relationship between the Database model :couple:
 - [X] The relationship between the Database model

 ### The CRUD :closed_lock_with_key:

 ![CRUD](https://static1.squarespace.com/static/555dc243e4b0fa866e3e41a9/t/5926bcdf9de4bbba0f69cd10/1495710948784/)

 CRUD's meaning is the following :

 * Create:
 Allows the user to create content
 > PUT or POST in HTTP
 * Read
  Allows the user to read the content
  > GET in HTTP
 * Update
  Allows the user to update the content
  > PUT / POST / PATCH in HTTP
 * Destroy
 Allow the user to delete the content
 > DELETE in HTTP

 These are the four basic fonctions that are found in every database.
 - [X] The CRUD


