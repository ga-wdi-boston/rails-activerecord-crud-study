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

## Explain Why an ORM Is Valuable

In your own words, define ORM and explain why using an ORM is valuable.

```md
<!-- your response here -->
```

## Name Model Files and Xlasses

Suppose I have an entity called "Person" that represents people in my
application. What would I name the file where I define the model for this
entity?

```md
<!-- your response here -->
```

What would I name the class for this entity?

```md
<!-- your response here -->
```

What would I name the database table for this entity?

```md
<!-- your response here -->
```

## Reference Documentation for CRUD

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another required method for persistence?

```md
<!-- your response here -->
```

Which ActiveRecord method finds all records of a certain type (or entity)?

```md
<!-- your response here -->
```

## Explain the Role of Migrations

In your own words, define migrations and explain why developers use them.

```md
<!-- your response here -->
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
<!-- your response here -->
```

What is the name of the method that creates a new column?

```md
<!-- your response here -->
```

I want to create a table called `pets` with columns `name` and `breed`, both
strings. `name` cannot be blank and must be unique. Write the migration you
would use to satisfy these requirements.

```ruby
# your response here
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
<!-- your response here -->
```

Should you use seeds to create data to experiment with during development?

```md
<!-- your response here -->
```
