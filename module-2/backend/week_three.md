## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
$ rails new <project-name> -T -d="postgresql" --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?
Models in rails inherit generally from ApplicationRecord.
Which itself inherits from ActiveRecord.

3. What do Controllers generally inherit from in a rails project?
Controllers in rails generally inherit from ApplicationController.

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horse, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
The command rake routes (or I belive rails routes not sure) will gives us in our terminal the list of all the routes we have available in our program so far (depending on what we implemented in our config/routes).
It gives us the prefix...(to be continued)

6. What is an example of a route helper? When would you use them?
articles_path is an example of a route helper (prefix) it will direct us to the index page of articles with all articles present on that page.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

8. What are strong params and why are they necessary?
They are necessary for security reasons (private makes that it is not accessible by everybody, we do not want that an user with bad intentions takes control of our program and drop our table/database !) and making sure we create every object with all the attributes necessary(like it is represented in schema).

9. What role does `form_for` play in helping us create our forms?
Create/ set up easily a for for us in html. (Esay way to do it).
10. How does `form_for` know where to submit the user's input?
form_for knows where to submit the user's input thanks to the argument right after @horse (horse_path) or if it is a nested resource then [@ranch, @horse] (ranch_horse_path).

11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.label :age %>
  <%= f.text_field :age %>
  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?
We want to validate our models to make sure we validate only correct data (with all attributes).

13. What are the steps of the DNS lookup?
The steps of the Domain Name System lookup are :
  1) Starts by looking up in our cache memory (dot betwenn quotes at the end of : www.google.com".") to see if we already know this website and IP address.
  2) If it does not, the operating system is configured to ask the resolving name server.
  3) Then ask to the Root Name Server goes back to the Resolving Name Server,
  4) Then ask to the Top Level Domain and goes back to the Resolving Name Server,
  5) Finally goes to the Authoritative Name Server and brings back the information (IP address) to the Resolving Name Server which gives it back to our browser/operating system (?).


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

To return 3 :    furniture[:table][:height]
To return true : furniture[:purchased]

16. What is inheritance?
Inheritance is the mechanism when an object inherits from another object. The behavior is passed between those two classes, the class that inherits the behavior is called the subclass (child) and the class it inherits from is called the superclass (parent).


### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
I think I do not manage well my stress level during assessments. On Friday I draw the three tables (user, book, review) and then erase review table and add it to user table for any kind of reason. 
