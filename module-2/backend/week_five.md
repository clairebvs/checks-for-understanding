### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  <% flash.each do |type, message| %>
    <%= content_tag :div, message, class: type %>
  <% end %>

2. Where is cart information/temporary information usually stored?
  It is stored in sessions.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
    Because we want to store what is in a cart only temporarily.
    We would like to have this information to persist when the user log out and log back in so his cart information will still exist (cookies(user side) and sessions).

4. What is the purpose of the asset pipeline?
  The purpose of the asset pipeline is to support all files written in .js and .css and images to reduce the number of requests by doing different action on those files.

5. Why do we precompile our assets?
We precompile our file so to not have whitespace and have only one file for .js and one for .css so we will have less requests when a user try to load the page.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
Acting as a link/displaying to an image, javascript(file?), and stylesheet file?.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  - What the project is doing ? What are we trying to solve ?
  - For who ? Giving them instruction on how to use our app/project.
  - Telling what we have used framework, programming language

8. What are the top four accessibility issues that we as developers should be aware of?
  Vision issue ? Not sure about what you are asking here.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
In our models. It is an example of a callback action(that we shall not use in general but refactor instead!).

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
 # scope :red, where(:color => 'red')
 # had to look online

 scope :active, where(:active => 'true')

11. What is the difference between a scope and a class method?
 ***

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
    a[:cart]["48"] = 4

  12b. How would you increase the quantity of item 29?
    a[:cart]["29"] += 1 (or any other number)

  12c. How would you find out how many items your user is thinking about purchasing?  
    a[:cart].values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  Using same method for different ruby object.
  By inheritance.
  I do not know what duck-typing is but according to internet it is considered as Duck test so if it acts like a duck and looks like a duck we should treat it like it. ( so for datatypes?)

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  ***


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few (more difficult then the previous week)



Choose One:
* I feel comfortable with the content presented this week
