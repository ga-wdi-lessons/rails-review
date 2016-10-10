# Rails Review

```
$ git clone https://github.com/ga-wdi-exercises/totally-doable
$ cd totally-doable
$ bundle install
$ rails db:create
$ rails db:migrate
$ rails db:seed
```

<details>
<summary>Steps completed already</summary>
## Initial Setup

```
$ rails new totally-doable
$ cd totally-doable
$ rails db:create
```

## Database Stuff

```
$ rails g migration create_todos text completed:boolean
$ rake db:migrate
```

### Create Seeds

```
# db/seeds.rb

Todo.create([
  {text: 'learn rails', completed: false},
  {text: 'learn javascript', completed: true}
])
```
</details>

## Read

### Read all

Create a route

```rb
# config/routes.rb

get '/todos', to: 'todos#index'
```

Create a controller

```rb
# app/controllers/todos_controller.rb
class TodosController < ApplicationController

end
```

Create an index method

```rb
# app/controllers/todos_controller.rb
class TodosController < ApplicationController
  def index
  end
end
```

get all the todos from the db

```rb
# app/controllers/todos_controller.rb
class TodosController < ApplicationController
  def index
    @todos = Todo.all
  end
end
```

create a view (template)

```html
<!-- app/views/todos/index.html.erb -->
  <%= @todos.inspect %>
```

loop through items

 ```html
 <!-- app/views/todos/index.html.erb -->
   <% @todos.each do |todo| %>
     <li>
        <% if todo.completed %>
          <del>
        <% end %>
        <%= todo.text %>
        <% if todo.completed %>
          </del>
        <% end %>
      </li>
   <% end %>
 ```

### Read a single one

Link to each one in the loop

```html
<%= link_to todo.text, "/todos/#{todo.id}" %>
```

Create a route in `config/routes.rb`

Create a method called `show`

Create a view in `app/views/todos/show.html.erb`


## Create

## Update

## Delete


## Screencasts from a previous review

- https://vimeo.com/150937914
- https://vimeo.com/150937915
- https://vimeo.com/150937916
