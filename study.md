# Rails: ActiveRecord Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Active Record Basics — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_basics.html)
-   [ActiveRecord::Base](http://api.rubyonrails.org/classes/ActiveRecord/Base.html)
-   [Active Record Migrations — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_migrations.html)

## Explain why an ORM is valuable

In your own words, define ORM and explain why using an ORM is valuable.

```md
ORM is 'Object-Relational Mapping' - it's a technique for connecting objects in
an application to tables in a database. This is how the model is able to communicate
with the databased, and it's valuable because without it we'd have to write SQL
queries/statements every time we wanted to interact with the database, and that
would suck.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
person.rb
```

What would I name the class for this entity?

```md
Person
```

What would I name the database table for this entity?

```md
People
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
create (this one makes a new object AND saves it... 'new' creates a new object
but doesn't save it, so it doesn't persist in the database. You'd have to
manually do new and then save for that.)
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a way to incrementally change a database over time, while at the
same time providing a record of the change that happened and an easy way to reverse
it. This allows for better record keeping and management than just having
a modifiable schema.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
add_column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
  t.string :name, null: false, uniqueness: true
  t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data populates the database with an initial set of data you specify in
db/seeds.rb.
```

Should you use seeds to create data to experiment with during development?

```md
You could, but seeds are really just meant for adding necessary initial data.
Creating data for testing can be done with gems that are better suited to that
task (Faker, for example). 
```
