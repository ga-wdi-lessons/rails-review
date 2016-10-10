# Rails Review

```
$ git clone https://github.com/ga-wdi-exercises/totally-doable
$ cd totally-doable
$ bundle install
$ rails db:create
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

## Screencasts from a previous review

- https://vimeo.com/150937914
- https://vimeo.com/150937915
- https://vimeo.com/150937916
