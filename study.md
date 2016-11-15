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
The way I picture a page or app is similar to the way I picture Mac OS X. In reality, all the OS is is a series of file and folders but the folks at Apple have made it look pretty. A website that contains data is in reality a bunch of ugly charts and what not. Much like OS X makes files easy to access, update, and maintain, the ORM connects all the data to whatever app we are using.
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
The create method will create new objects and persist the objects in the database.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are a way to update and maintain the way the data on a page is layed out. They are beneficial becuause they use version control making the code maintanable over time.
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
class CreatePets < ActiveRecord
  def new_table
    create_table :pets do |i|
      t.string :name, null: false uniqueness: true
      t.string :breed
    end
  end

```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
I believe Seed data is information the application needs to load properly. A plant needs a seed to grow as does an application. It also helps preload data.
```

Should you use seeds to create data to experiment with during development?

```md
Yes.
```
