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
ORMs represent static data items (rows composed of columns of data in database) as active software objects with behaviors and relationships to other data.
ORMs make it possible to apply business logic to data items and relationships more efficently and with a greater degree of abstraction than would be possible using
SQL queries alone.
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
people
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
#create instantiates new objects.  The "create" method does not persist the object.
#save must be called to save the object.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
#find_by
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations make it possible to alter a database over time.  Migrations represent distinct
alterations to the structure of the application.  According to my understanding, Migrations
are simply changes to the datbase schema that are recorded and which can be reversed.
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
class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name PRIMARY KEY
      t.string :breed
  end
end```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data may be used to populate development
 databases that may be frequently reloaded due to frequent migrations or other issues.
 Rails seed method makes this process easier and more standardized.
```

Should you use seeds to create data to experiment with during development?

```md
Yes
```
