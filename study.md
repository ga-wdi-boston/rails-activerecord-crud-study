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
It lessen the amount of code that we need to write in order to store and retreive data from a database.
```

## Name model files and classes

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
app/models/person.rb
```

What would I name the class for this entity?

```md
class Person
end
```

What would I name the database table for this entity?

```md
some_number_create_people.rb
```

## Reference documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
newPerson = Person.new(colums we added in our database) -- This won't save the instance. It will initialize it.

newPerson = Person.create -- It will actually save the instance.
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
Person.all
```

## Explain the role of migrations

In your own words, define migrations and explain why developers use them.

```md
Because it is easier to handle database alterations over time. If we want to add new rows and data.
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
rails generate migration pets name:string breed:string validates :name, :presence => {:message => 'Name cannot be blank'} unique: true
```

## Explain the role of seed data

In your own words, explain the role of application seed data.

```md
If we want to add data after database is created.
```

Should you use seeds to create data to experiment with during development?

```md
Yes.
```
