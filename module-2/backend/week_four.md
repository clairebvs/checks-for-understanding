## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A cookie is a small piece of data stored on the computer's user. This piece of data is coming from a website (to remember what a user "did" : added things to cart for example).

2. What’s the difference between a session and a cookie?
  The difference between a session and a cookie is where the data is stored.
  For a cookie the data is stored on the computer's user.
  For a session the data is stored on the server.

3. What’s a flash and when do you want to use flashes?
  A flash is a message that 'pop up' on our browser page after we performed an action to tell us if we were successfull or not. We usually want to use it when a user logout or add an article to his cart or when an admin edit or delete an element.

4. Why do people say “HTTP is stateless”?
  Because HTTP does not stored any information in memory once the request/response has been performed. It is just "a way to connect".

5. What’s authentication? Explain.
  Authentication is when we want to check 'Who are you?'

6. What’s the difference between authentication and authorization?
  With authorization we want to check are you allowed to see this or that. Depending on who you are (which is the authentication 'role').

7. What’s a before filter?
  A before filter allows us to run this method (before) before to run any other controller action.

8. How do we keep track of a user once they’ve logged in?
  We keep track of an user once they have logged in thanks to the session (session controller).

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
We will nest a resource when this resource needs another one.
We will namespace a resource for authorization purpose (it will be in a folder).
When we namespace a resource that resource does not require another resource unlike when resources are nested.

10. At a high level, what tools can you use to implement authorization? How would you use them?
Namespacing and we would use a before_action method in our controller to see who can see/perform that action.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum allows us to assign an integer to a data in our database for authorization purpose.
Ex if we have user that has a column role. Role will be an integer 0 or 1.
In our model, for the corresponding table (user), we will set this enum to a variable default for 0 and admin for 1 :
  enum role[:default, :admin]


12. What are some strategies you can use to keep your views DRY?
  By using a partial form (avoid repetition).


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
array_hash.sort_by do |f|
  f[:holiday][:name]
end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
