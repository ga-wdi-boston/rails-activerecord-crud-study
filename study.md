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
Object Relational Mapping. This is connects objects to databases. It is important because it streamlines between apps and db's, cutting out db code.```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
PersonEntity```

What would I name the class for this entity?

```md
Person```

What would I name the database table for this entity?

```md
people```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
.new creates new objects. .save will add to db.```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
.all```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
migrations are like sql commands to add, like INSERT INTO to the database but done in a text editor. Devs use them because they can be reversed. ```

## Reference documentation for migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :tablename```

What is the name of the method that creates a new column?

```md
add_column :name```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
create_table :pets do |t|
  add_column :name
  add_column :breed
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
seed data is to add data to an existing database```

Should you use seeds to create data to experiment with during development?

```md
Nothing in documentation suggests this would cause harm to a machine or db, so why not.```
