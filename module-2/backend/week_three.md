## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

rails new

2. What do Models generally inherit from in rails?

ActiveRecord::Base

3. What do Controllers generally inherit from in a rails project?

ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

get '/horses/:id', to: 'horses#show'

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes
It shows you the prefix, verb, route, and controller action.

6. What is an example of a route helper? When would you use them?

horses_path is an example. You use them you link to different controller actions in your code or in your views.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

'_path' is a relative path while '_url' is an absolute path. '_path' is generally used most of the time.

8. What are strong params and why are the necessary?

strong params are used in the controller used to pass only specific params into create and update methods. This is necissary so that extra params could not be passed in maliciously from the user side.

9. What role does `form_for` play in helping us create our forms?

form_for is a form helper that makes it easier to generate HTML for forms using ruby code.

10. How does `form_for` know where to submit the user's input?

It checks whether or not an object has already been created by using the method '.new_record?'

11. Create a form using a `form_for` helper to create a new `Horse`. 

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  
  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?

So that a new model object isnt created if it does not have all of the required fields.
