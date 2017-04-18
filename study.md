# Rails: ActiveRecord Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Active Record Basics — Ruby on Rails Guides](http://guides.rubyonrails.org/active_record_basics.html)
    (up to and including chapter 6)

## Additional Resources
-   [ActiveRecord::Base](http://api.rubyonrails.org/classes/ActiveRecord/Base.html)
-   [Object-relational mapping - Wikipedia](https://en.wikipedia.org/wiki/Object-relational_mapping)

## Explain Why an ORM Is Valuable

In your own words, define ORM and explain why using an ORM is valuable.

```md

ORM is a mechanism to connect application objects to a database management system via tables. An ORM is valuable because it enables the ability to store and retrieve object deatils from a database without having to write extensive SQL logic directly.
```

## Naming Models

Suppose that there is an entity called "Person" that represents people in an
application. What should be the name of the file where the model for this entity
is defined?

```md
Person
```

## Naming Classes

What should be the name of the class that represents this entity?

```md
Person
```

## Naming Database Tables

What should be the name of the database table for this entity?

```md
people
```

## Objects and Persistence

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another method required for persistence?

```md
The .new method creates a new object WITHOUT saving to the database. To persist to the database in a single method call, .create should be used.
```

## Retrieving Records

Which ActiveRecord method finds all of the records of a certain type (or
entity)?

```md
.all
```

## Rails Console

For the subsequent questions, assume that we are in the Rails console (by
entering `rails console` in the terminal and that the model names follow Rails
naming conventions.  e.g., The name of the model for a "people" collection would
be "Person".

## Create

Create the following movies with the given attributes.

| id | title | rating |
| --- | --- | --- |
| 0 | Battlefield Earth | 2.4 |
| 1 | Sharknado | 3.3 |
| 2 | The Core | 5.4 |

```ruby
Movie.create({title: 'Battlefield Earth', rating: 2.4}, {title: 'Sharknado', rating: 3.3}, {title: 'The Core', rating: 5.4})
```

## Read

From the following collection of organisms, find the record with "Red Panda" as
its `common_name`, find all records of organisms belonging to the `phylum`
Mollusca, and find the last record.

| id | common_name | binomial_name | phylum |
| --- | --- | --- | --- |
| 0 | Mystery Snail | Pomacea bridgesii | Mollusca |
| 1 | Red Panda | Ailurus fulgens | Chordata |
| 2 | Stubby Squid | Rossia pacifica | Mollusca |

```ruby
panda = Organism.find_by(common_name: 'Red Panda')
mollusca = Organism.where(phylum: 'Mollusca')
last = Organism.last
```

## Update

From a collection of galaxies, update the `name` attribute of the record with
the `designation` attribute of "NGC 224" to "Andromeda".

```ruby

galaxy = Galaxy.find_by(designation: 'NGC 224')
galaxy.update(name: 'Andromeda')
```

## Delete

From a collection of characters, delete the record with the `id` attribute of 4.

```ruby
character = Character.find_by(id: 4)
character.destroy
```
