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
ORM is short for Object Relational Mapping. ORM is a type of programming that
allows for compatible relationships for objects that wouldn't ordinarily have
compatible data types.

Sources: https://en.wikipedia.org/wiki/Object-relational_mapping
http://guides.rubyonrails.org/active_record_basics.html
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
Person
source: http://guides.rubyonrails.org/active_record_basics.html
```

What would I name the class for this entity?

```md
Person
source: http://guides.rubyonrails.org/active_record_basics.html
```

What would I name the database table for this entity?

```md
people
source: http://guides.rubyonrails.org/active_record_basics.html
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
The method, create, cretes new objects. Validation is required to maintain
persistance.
source: http://guides.rubyonrails.org/active_record_basics.html
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
Find_by.

source: http://guides.rubyonrails.org/active_record_basics.html
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations are files stored in the migrate directory in a database that keep
track of the different versions of the database that you have created. They
are useful because they eliminate the need to write SQL.
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
source: http://edgeguides.rubyonrails.org/active_record_migrations.html
```

What is the name of the method that creates a new column?

```md
add_column
source: http://edgeguides.rubyonrails.org/active_record_migrations.html
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table : pets |t|
t.string :name, :breed
end
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
seed data makes it easy to add data once a database has been initially created.
source: http://edgeguides.rubyonrails.org/active_record_migrations.html
```

Should you use seeds to create data to experiment with during development?

```md
Yes. It is very useful during test environments because the database can
frequently get reloaded.
source: http://edgeguides.rubyonrails.org/active_record_migrations.html
```
