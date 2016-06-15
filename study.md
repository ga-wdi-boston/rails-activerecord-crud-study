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
ORM - Object Relational Mapping - is the system that relates ruby objects to
their corresponding database tables. Rather than manually having to create objects
that have the table dimensions as attributes and manually instantiating the objects
based on the class that looks like the table, ORM just handles all of that for you.
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
.new makes a new instance but doesn't save it. You need .save to save it.
You can also use .create to both make the new instance AND save it.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all gets all records.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are how you update a database schema. This is important because
you want to be able to persist data from the past into the new database, but you
may need to start tracking data in a different way, for example, with a new table
or new columns. You need a migration to easily change the database. Without
migrations you would have to write a lot of code to make a totally new database
and import all of the data into it.
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
class Pets < ActiveRecord::Migration
  def change
    create_table :pets do |t|
      t.string :name, null: false, unique: true
      t.string :breed

      t.timestamps null: false
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
I think seed data is just there for testing the application.
```

Should you use seeds to create data to experiment with during development?

```md
I think so.
```
