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
ORM (Object-relational-mapper) let us use languages other than SQL (like Ruby) to perform actions on data in a database, like create, read, and update. It's incredibly valuable because it will save us time in creating databases, and allow us to sync Ruby objects and database rows without much extra code.
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
class People
```

What would I name the database table for this entity?

```md
people.sql
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.new will create new objects, but it does not save them to the database. To create and save an object, we must use .create
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.find_by(attribute) or .where(attributes)
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow us to alter databases over time. This means that we don't have to destroy all our past work if we want to make a change or alter the database - we can just migrate/append a new database, or rollback to a previous one.
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
class CreatePets < ActiveRecord::Migration
  def change
    create_table :pets do |t|
      t.string :name, null: false, uniqueness: true
      t.string :breed
    end
  end
end

```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Application seed data is used to add initial data to a database after it's created. This allows us to test and make adjustments on the database before releasing it to the user.
```

Should you use seeds to create data to experiment with during development?

```md
Yes, absolutely!
```
