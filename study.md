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
ORM connects the objects in our code with the tables in our databases without
requiring us to write SQL. It essentially maps our objects to the format needed
to store them in databases and saves us the step of doing this ourselves.
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
The .new method will create new objects, but it will not persist them to the
database, you have to use .create to do that.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
Type.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow you to update your database over time, you can add or remove
tables, columns or rows. They are a convenient way to make changes without
writing SQL.
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
class Pets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name, null: false
      t.string :breed, null: false
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data loads initial data to your database, which is especially helpful
when developing & running tests.
```

Should you use seeds to create data to experiment with during development?

```md
Yes
```
