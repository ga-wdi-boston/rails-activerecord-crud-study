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
This technique can be used to convert an Object into a table or tables for a
relational database management system. In other words, it can be used to
easily store information.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
In Ruby you would name the file for holding the list of people: people.rb
For the file where the model is defined, a good name is: person.rb

```

What would I name the class for this entity?

```md
I would name the class Person with an uppercase "p".
```

What would I name the database table for this entity?

```md
A good name for the database table would be people_db.rb
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
The method is CREATE, and it will give you back the new object and save it to the
database with .create. to create an instance you can use .new.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
The method for finding something you need by type or entity is READ.
For example it can be used with .all, or .first.
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
A migration can be useful to change/update your database. It basically makes
another version of your current database.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
The method used is create_table.

 <!-- NOTE NOTE NOTE ASK IN CLASSS does it take -->
<!-- :products and t? explain this method please. -->
```

What is the name of the method that creates a new column?

```md
The method for a new column is add_column.
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
# writing migration?
class Pets < ActiveRecord::Migration[5.0]
  def change
    add_column :'name', :'breed'
  end
end
# NOTE ANSWER

create_table :pets do |t|
  t.string :name
  t.breed :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seeds are used to add the information you need when recreating a database with a
migration. They facilitate the way that you input data when reloading a database.
```

Should you use seeds to create data to experiment with during development?

```md
I assume it wouldnt hurt to practice doing so. I didn't find anything about seeds
being bad ideas, so I will ask again in class.
```
