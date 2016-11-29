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
In our case, ORM allows us to write ruby that handles interacting with a database
without having to worry about writing additional SQL. We end up having to write much less code.
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
people.sql
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.create()
Objects are automatically saved to the database as rows. To instantiate an object
without saving it, one can use .new(), and .save can then be used to record the
instantiation.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.find_by(attribute: 'value')
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations create discrete sets of changes to a database, much like commits work
in git. They allow keeping a timeline of changes to a schema that could possibly
be reversed if required, but are also used to simply add or alter data in a database in an efficiently.
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
class CreatePets < ActiveRecord:Migration
  def change
    create_table :pets do |t|
      t.string :name, null: false
      t.string :breed
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data sets up the basic structure of a previously blank database.
```

Should you use seeds to create data to experiment with during development?

```md
Yes. You can create test databases with extraneous seed data to test your code.
```
