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
<!-- your response here -->
ORMs connect objects of an app to tables in order to save these objects in a database without directly writing SQL.
```

## Naming Models

Suppose that there is an entity called "Person" that represents people in an
application. What should be the name of the file where the model for this entity
is defined?

```md
<!-- your response here -->
Person_Model
```

## Naming Classes

What should be the name of the class that represents this entity?

```md
<!-- your response here -->
Person
```

## Naming Database Tables

What should be the name of the database table for this entity?

```md
<!-- your response here -->
people
```

## Objects and Persistence

Which ActiveRecord method creates new objects? Does this method persist objects
as rows in the database, or is there another method required for persistence?

```md
<!-- your response here -->
NEW -- creates new objects without being saved.
CREATE -- creates new objects and saves them in the database.
```

## Retrieving Records

Which ActiveRecord method finds all of the records of a certain type (or
entity)?

```md
<!-- your response here -->
WHERE -- find all the records of a specified criteria.
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
# your answer here
movie0 = Movie.create(title: "Battlefield Earth", rating: 2.4)
movie1 = Movie.create(title: "Sharknado", rating: 3.3)
movie2 = Movie.create(title: "The Core", rating: 5.4)
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
# your answer here
organism = Organism.find_by(common_name: 'Red Panda')
organism = Organism.find_by(phylum: 'Mollusca')
organism = Organism.last
```

## Update

From a collection of galaxies, update the `name` attribute of the record with
the `designation` attribute of "NGC 224" to "Andromeda".

```ruby
# your answer here
galaxy = Galaxy.find_by(designation: 'NGC 224')
galaxy.update(designation: 'Andromeda')
```

## Delete

From a collection of characters, delete the record with the `id` attribute of 4.

```ruby
# your answer here
movie = Movies.find_by(id: 4)
movie.destroy
```
