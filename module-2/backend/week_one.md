## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
The five common HTTP Verbs are
get   -> retrieve a resource
post   -> create a resource
put    -> modify a resource
patch  -> modify a part of a resource
delete -> delete a resource

2. What is Sinatra?
Sinatra is a framework write in Ruby and used for web application.

3. What is MVC?
MVC is a design pattern.
Model, Controller and View.
The model takes care of all the logic because it interacts with the database.
The controller is the 'traffic cop' it dispatch what needs to be by "telling" to the model what it needs to reach, create, delete to the/from the database. And tells the route/path to follow to the view.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We follow conventions when creating our actions/path names in our Sinatra routes to be "user friendly" because it is what the user expects to encounter. It is also for other developers and what they expect to have/see depending on a the actions/path names.

5. What types of variables are accessible in our view templates without explicitly passing them?
Instance variable.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
local: {name: 'Mr. Ed'}

8. What's the purpose of ERB?
Being able to use Ruby and HTML(tags) in the same file.

9. Why do I need a development AND test database?
We need a development and test database so we can test all our functions without altering our database and so tables. It is a secure way to work with our database without taking the risk to delete everything.

10. What is CRUD and why is it important?
Create Read Update and Delete are four basic functions that we want our model to perform on a resource(it can be an image, text, ...).

11. What does HTTP stand for?
Hyper Text Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> can be seen by the user/ in our browser.
 and
<% %> does not print it to the user interface.

13. What's an ORM? What does it do?
ORM stands for Object Relational Mapping. It allows us to use Object-Oriented programming languages when we manipulate data from a database.  

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
It is ActiveRecord.

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

get '/restaurants'
To see all the restaurants

get '/restaurants/:id'
To see a specific restaurant  

post '/restaurants/new'
To create a restaurant

get '/restaurants/:id/edit'
patch '/restaurants/:id'
To update a restaurant attributes

delete '/restaurants/:id'
To delete a restaurant

16. What's a migration?
A migration defines how we are going to create a table with data from our database.

17. When you create a migration, does it automatically modify your database?
After creating our migration, we need to run rake db:migrate.

18. How does a model relate to a database?
The model in our MVC model "has a direct link with our database", it retrieves the information we need from the database.

19. What is the difference between `#new` and `#create`?
Create is a method from ActiveRecord that performs both new and save.


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
File.read("filename", headers: true, header_converters: symbol)
(path, headers: true, header_converters: :symbol)

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies] << 'granola bar'
(checked on pry)

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Inheritance   -> Can have access to method and instance variable from other/parent class.
Encapsulation -> Do not expose method or variable when it is not necessary (attr_accessor)

I could not remember the two others.
Here is what I find online :
Polymorphism  -> existence of an Object behavior in different form.
Abstraction   -> Hiding elements that are not necessary in order to be simple and logic.


### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few (maybe a little bit more than a few but not heavily neither).
I have not memorize all the new information we learned this week or at least not as much I feel like I should. 


Choose One:

* I feel overwhelmed by the content presented this week
