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
ORM is a means in which to assign relationships to objects to assiciated tables of data in a meaningful and standardized way. It is valuable because it saves developers a ton of time and guess work by standardizing the way in which data is stored and accessed.
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
class Person
```

What would I name the database table for this entity?

```md
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.create is used to create new objects. .save is required in order for objects to persist
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.where finds all records with a given stipulation
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
migrations are a way in which to take shorthand expressions and allows for Ruby to translate this shorthand into SQL, adding or updating your databases without you having to writeout the SQL yourself.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
.create_table
```

What is the name of the method that creates a new column?

```md
.add_column
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
class Pet < ApplicationRecord
  validates :name, presence: true
end

self.table_name = "pets"
self.add_column = :name
self.add_column = :breed
end
```
## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
seed data in a migration allows for the set up of an initial db with initial data values inwhich to develop your application.
```

Should you use seeds to create data to experiment with during development?

```md
From the looks of it, yes. 
```
