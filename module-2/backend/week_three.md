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
articles_path is an example of a route helper (prefix) it will direct us to the index page of article with all articles present on that page.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

8. What are strong params and why are they necessary?
They are necessary for security reasons (private makes that it is not accessible by everybody, we do not want that an user with bad intentions takes control of our program and drop our table/database !) and making sure we create every object with all the attributes necessary(like it is represented in schema).

9. What role does `form_for` play in helping us create our forms?
10. How does `form_for` know where to submit the user's input?
11. Create a form using a `form_for` helper to create a new `Horse`.
12. Why do we want to validate our models?
13. What are the steps of the DNS lookup?


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
16. What is inheritance?

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
