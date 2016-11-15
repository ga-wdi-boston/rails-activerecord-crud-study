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
ORM stands for Object Relational Mapping.  I think an ORM would be valuable since it allows you store and retrieve information from your database with ltess direct access to the database.  If these relationships are pre-defined there’s less of a chance of you mis-typing a SQL command and causing a problem.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
Person
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
The create method call will create and save a new record into the database.  The new method creates the object, but doesn’t save it.  If you decide to save it, you can call <object_name>.save.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
<model_name>.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are stored in files and can be run against any database that ActiveRecord supports through rake.  They use a database independent language so you don’t have to write SQL by hand and your changes can be run against databases of different engines. They also provide consistency to your schema changes over time.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
t.<data_type> :<col_name>
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name, null: false, index: true
      t.string :breed
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
The application seed data is used to add data after a database has been created.  It’s an easy way of filling up an empty database with default values.
```

Should you use seeds to create data to experiment with during development?

```md
I think that would be helpful.  You could make sure your dev and test databases were filled with production-like (not actual production) data to ensure that your application functions as you’re expecting it to before running it in your prod environment.
```
