## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
* POST/ to add something new to DB
* GET/ to request some info from the database
* DELETE/ to delete from our database
* PATCH/ to update a part of DB
* PUT/ to update all of DB

2. What is Sinatra?
4. What is MVC?
* model/view/controller
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
* so can be easily read by other programers
6. What types of variables are accessible in our view templates without explicitly passing them?
* instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
```ruby
get '/horses' do
  erb :index, :locals => {:name => "Mr. Ed"}
end
  ```
9. What's the purpose of ERB?
* to use html and css with ruby
10. Why do I need a development AND test database?
* so your not currupting you data with test creations
11. What is CRUD and why is it important?
* create/read/update/destroy Without it your app wouldnt do much at all
12. What does HTTP stand for?
* HyperText Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
* <% %> will do ruby code but will not show to screen
* <%= %> will show ruby code to screen
14. What's an ORM?
* Object Relational Mapper
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
* Active Record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
* GET '/restaurants' would allow user to see all the restaurants
* GET '/restaurants/new' would take user to a view for the creation of a new restaurant
* GET '/restaurants/:id/edit' this would take the user to the view i have setup for entering new info for a restaurant thats already in the database
* Post '/restaurants/:id' this is when the information is being changed in the database. Much like post but we are changing the info and not adding new info
* POST '/restaurants' the POST is going to create a new restaurant in our database
* GET '/restaurants/:id' the user would be able to search for a restaurant by id number
* DELETE '/restaurants/:id' allow the user to delete a restaurant from the database based on id number

17. What's a migration?
* creating the Db from the schema
18. When you create a migration, does it automatically modify your database?
* not until you migrate
19. How does a model relate to a database?
* its used to create ruby objects
20. What is the difference between `#new` and `#create`?
* the same but create also saves

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
require 'csv'
```ruby
CSV.foreach("films.csv", headers: :true, header_converters: :symbol, converters: :numeric) do |row|
 Film.create(row.to_hash)
end
  ```
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?
```ruby
activities[:hiking][:supplies] << 'granola bar'
  ```
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
* inheritance / when a class inherits from another and has the traits
* polymorphism / changes its behavor based on what is passed to it.
* encapsulation limits what in your problem knows about what
* abstraction / When you take a complex problem and break it down to simple readable verbs

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel confident about the content presented this week
