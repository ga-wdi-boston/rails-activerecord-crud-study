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
Object Relational Mapping or ORM is a way to maintain the complexity of objects,
found in object-oriented programming, even when that information is stored in a
database. The ORM uses tables to maintain this complexity, where information in
one table has interactions with information in other tables to show
relationships of the object's various parts.

Databases are generally not set up to adequately respresent complex objects, ORM
allows relationships to remain intact without having to write extra
code to break down the object into database sized pieces.

resources used:
https://en.wikipedia.org/wiki/Object-relational_mapping
http://guides.rubyonrails.org/active_record_basics.html
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
Person.
```

What would I name the class for this entity?

```md
class Person.
```

What would I name the database table for this entity?

```md
people.

resources used:
http://guides.rubyonrails.org/active_record_migrations.html
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.create or .new
create: makes the object and saves it to the database
new: makes the object, but doesn't save it
  -if you want to save an object created with 'new', you also have to use the
  save method
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a way of altering tables in your database and keeping track of
those changes, all while having Rails create the necessary SQL commands for you.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
change
```

What is the name of the method that creates a new column?

```md
change
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name, null: false, uniqueness: true
      t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data is sample information which allows the developer to see how their
application will handle data, without the developer having to go out and collect
information. Seed data can be used to evaluate if written code manipulates the
data as expected.
```

Should you use seeds to create data to experiment with during development?

```md
Yes.
```
