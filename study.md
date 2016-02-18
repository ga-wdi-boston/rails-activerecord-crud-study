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
ORM stands for 'Object-Relational Mapping' - it's the technique that lets you manipulate objects and communicate with the database, which is how the model layer does it job as well in the MVC pattern. It's valuable because a lot of processes are automated, so it's easier to maintain, update and reuse. You don't need to write SQL queries for every command with the database. With ORM, you can interact directly with an object in the same language you're using (Ruby for us).
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
People
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.create - creates new objects but does not save them. To save it to the database after you create new object, use .save.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Database don't tend to stay the same. It will change over time, so migrations are a convenient way for developers to define, track and manage any changes to the database schema. It's good housekeeping and record keeping like Github, a source of version control system.
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
class Create_Pets < ActiveRecord::Migration
def change
create_table :pets do |t|
      t.string :name, null:false, uniqueness: true
      t.string :breed
    end
  end
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seed data provides initial set of data to begin building your app in db/seeds.rb.
```

Should you use seeds to create data to experiment with during development?

```md
You could but you shouldn't. You should separate seed data from testing data.
```
