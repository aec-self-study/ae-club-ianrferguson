# Data Modeling

* Preprocessing + transofrming data prior to querying
* Implement agreed upon definitions of what gets counted as a sale

* Modeling == higher level of intention
    * Why am I creating this in the big picture?

## Solution 1 - One Big Table

* One centralized table with everything you would need to answer questions

* Pros
    * Easy to right
    * Easy to extend

* Cons
    * Can quickly become unwieldy and hard to navigate
    * BI tools often ask you to define your joins
    * Challenging when the dimensions can update without warning (e.g., product changing category)

## Solution 2 - Star Schema

* Many reference tables feed into one aggregate table (this is similar to how we work at ML)

* Pros
    * Many people can write this code
    * Very easy to navigate
    * This design is handy when the dimenions change without warning

* Cons
    * SQL proficiency is pretty mandatory in order to accomplish this

## Solution 3 - Kimball's approach

* Also a star Schema

* Two new terms:
    * Fact = The columns that get aggregated (sales amounts)
    * Dimensions = The columes that you group by (sales person, store location, vendor, etc.)

## Best Practices

* Models should have clear grain
* Models should use consistent naming conventions
* Models should anticipate multiple questions from a stakeholder
* Models should be "idempotent" ... i.e., if you drop them you could rebuild them from scratch
