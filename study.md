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
  An ORM is a framework which converts data so that it can be translated in
  order to work with a backend frameworks. It will allow us to doing things
  like create, read and update without the extra code.
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
.new creates objects. But in order to be able to save the object
you will have to use the .create
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.where(attributes)
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow developers to alter databases over time. Which means insteading
destroying all our past work in order to make a change you can simply alter
the database.
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
+class Pets < ActiveRecord::Migration [5.0]
 +  def change
 +    create_table :pets do |t|
 +      t.string :name, null: false, unique: true
 +      t.string :breed
 +    end
 +  end
 +end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Application Seed data allows you to push data through your code all at once
to see how it runs. It is a good way to beta test your product before deploying
it.
```

Should you use seeds to create data to experiment with during development?

```md
100%
```
