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
ORM: Object Relational Mapping. ORM stores the relationships between objects
in databases on the server. Said databases can be stored and accessed without
having to take the extra step of writing SQL statements.
ActiveRecord is one such ORM.
http://guides.rubyonrails.org/active_record_basics.html#active-record-as-an-orm-framework
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
people
http://guides.rubyonrails.org/active_record_basics.html#active-record-as-an-orm-framework
```

What would I name the class for this entity?

```md
People
http://guides.rubyonrails.org/active_record_basics.html#active-record-as-an-orm-framework
```

What would I name the database table for this entity?

```md
people
http://guides.rubyonrails.org/active_record_basics.html#active-record-as-an-orm-framework
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
Create
http://guides.rubyonrails.org/active_record_basics.html#create
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.where
http://guides.rubyonrails.org/active_record_querying.html
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Migrations allow you to make incremental and reversible changes without having
to manually write SQL. Each migration is essentially an update to the
database: tables, columns, and entries may be added and removed; and it even
adheres to any changes in the STRUCTURE of the database. Migration is a
relatively simple way of implementing multiple updates.
http://guides.rubyonrails.org/active_record_migrations.html
```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
http://guides.rubyonrails.org/active_record_migrations.html#creating-a-table
```

What is the name of the method that creates a new column?

```md
add_column
http://guides.rubyonrails.org/active_record_migrations.html#creating-a-table
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
class CreatePets < ActiveRecord::Migration
  def change
    create_table :pets do |t|
      t.string :name, :null => false, unique: true
      t.string :breed
    end
  end
end
# http://stackoverflow.com/questions/21635825/how-to-create-a-new-table-with-a-unique-index-in-an-active-record-rails-4-migr
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
Seeds adds initial data to the database AFTER the database is created.
http://guides.rubyonrails.org/active_record_migrations.html#migrations-and-seed-data
```

Should you use seeds to create data to experiment with during development?

```md
Yes, because the process is quick, making it easy when frequently reloading
the database during the development process.
http://guides.rubyonrails.org/active_record_migrations.html#migrations-and-seed-data
```
