## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord is an ORM (Object Relational Mapping) that allows us to "talk" to our database to query it (through SQL but not using it directly).
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

The methods we can call on Team are find, where, order, all, select, join, includes ... We have access to those methods through inheritance (ActiveRecord::Base).


3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

team = Team.find(id: 4)
Team.find(owner_id: team)


4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.find(id: 4).owner_id

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Many to many relationship.
Students have many teachers.
Teachers have many students.

Students        Student_Teachers      Teachers
Name            Student_id            Full Name
Module          Teacher_id            Class

6. Define foreign key, primary key, and schema.
A primary key is the id of a table itself. A primary key is unique. A foreign key is the id of a table within another table because of a relationships (belongs_to) to link them. A schema is the representation of the table (we can see the name of the tables and the columns).
7. Describe the relationship between a foreign key on one table and a primary key on another table.
As said above, the foreign key references the primary key of another table.
8. What are the parts of an HTTP response?
A status
a header and
a body(optional)

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.

8. Describe and diagram the relationship between museums and original_paintings.

9. What could you see in your code that would make you think you might want to create a partial?

HTML code that is the same in several files (edit, show, index.. ). Example : code for a navbar can be put in a partial file so we do not have to write it in every html file (show, index, edit ...).

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
A little of both.
