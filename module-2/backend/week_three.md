## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new nameofproject -T -d="postgresql" —skip-turbolinks —skip-spring
2. What do Models generally inherit from in rails?
* ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
* ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard
 conventions and that I didn't want other CRUD functionality?
 *   resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
* rake routes
6. What is an example of a route helper? When would you use them?
* edit_horses_path
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* url will return whole url path
8. What are strong params and why are they necessary?
* whats allowed to be changes
9. What role does `form_for` play in helping us create our forms?
* a place the user can input what they want to change
10. How does `form_for` know where to submit the user's input?
* bases on the view its in.
11. Create a form using a `form_for` helper to create a new `Horse`.


              <%= form_for @horse do |f| %>
                <%= f.label :name %>
                <%= f.text_field :name %>

                <%= f.submit %>
              <% end %>
12. Why do we want to validate our models?
* to make sure its not created with missing information
13. What are the steps of the DNS lookup?
* Query
* root servers
* TLD name server
* Domains name server
* Website appers


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  @horse.prance
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
furniture[:table][:height]
16. What is inheritance?
* inheritance is where "traits" is passed from another class.

### Self Assessment:
Choose One:



Choose One:
* I feel confident about the content presented this week
