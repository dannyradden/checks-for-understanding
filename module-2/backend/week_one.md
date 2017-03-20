## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

  GET - When fetching information
  POST - When sending new information
  PUT - When updating infromation
  DELETE - When deleting information
  
2. What is Sinatra?

  Sinatra is a web application library used to make an app that can route HTML requests.
  
4. What is MVC?

  MVC is convention used in making an app. M is Model, V is views, and C is Controller.
  
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  So that other developers can get around the app easier.
  
6. What types of variables are accessible in our view templates without explicitly passing them?

  Instance variables
  
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  @count = 1
  get '/horses' do
    erb :index, :locals => {:name => 'Mr. Ed'}
  end
  ```
  
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

9. What's the purpose of ERB?

  To write HTML with Ruby code integrated
  
10. Why do I need a development AND test database?

  You want your test database to start out empty and add to it, The development db will often already have data in it.

11. What's responsive design?
  
  HTML design that is flexible and looks good no matter the client.

12. What is CRUD and why is it important?
 
  Create, Read, Update, and Delete. It is important to be able to do all of thhese things to the data in your app and database.

13. What does HTTP stand for? 
  
  Hyper-Text transfer protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  
  <%= %> will run the code and display the output.  <% %> will just run the code

15. What's an ORM?
  
  Object Relational Mapping is used to map database rows to ruby objects that can be interacted with.

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  
  ActiveRecord

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  
  get '/restaurants'    -  Gets the restaurant main index page
  get '/restaurants/new'   -  Used to get the form to create a new restaurant
  get '/restaurants/:id'    -  Used to get a show page for a specific restaurant
  get '/restaurants/:id/edit'    -  Used to get the form to edit an already created restaurant
  post '/restaurants'            -  Posts a new restaurant to the index with the form info.
  put '/restaurants/:id'          - Updates the selected restaurant with the form info.
  delete '/restaurants/:id'      - deletes a specific restaurant.

18. What's a migration? 
  
  A ruby file used to change data in a database.

19. When you create a migration, does it automatically modify your database?
  
  No, you need to run the migration.

20. How does a model relate to a database?
 
 The model has methods that pull data from the database, make an object out of them, and interact with those objects.

21. What's the difference between agile workflow and waterfall method?
  
  Agile workflow continuously does testing, design, and coding in small chuncks repeatidly. Waterfall is more linear and starts with all the design, then does all the test writing, then does all the coding.

22. What is the difference between `#new` and `#create`?
  
  New makes the object but doesnt write it to the database. Create makes the object and writes it to the database.
