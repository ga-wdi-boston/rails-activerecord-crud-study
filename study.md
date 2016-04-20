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
ORM stands for Object Relational Mapping. It is a technique that connects the objects of an application to tables in a relational database management system. ORMs are useful because they allow you to easily store and retrieve the properties and relationships of objects in the application without writing SQL statements.

Source: http://guides.rubyonrails.org/active_record_basics.html
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people_model
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
.new

You must call .save to commit the record to the database. Or you can use .create with makes a new object and saves it.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.where()
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a feature of Active Record. They allow you to alter your database schema over time in a consistent and easy way. Each migration is a new 'version' of the database. Developers use them because they allow you to avoid writing SQL by hand.

Source: http://edgeguides.rubyonrails.org/active_record_migrations.html
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
  t.string :name, null: false, unique: true
  t.string :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seeding is the proccess of populatng a database with inital data after a database is created.
```

Should you use seeds to create data to experiment with during development?

```md
Yes
```
