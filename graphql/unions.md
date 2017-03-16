# Unions

In GraphQL, everything is heavily typed. Today I asked myself "Is it possible to have one query return multiple objects of different types?" Turns out, it is possible with Unions!

Using Apollo, setting up unions is really easy. You have to specify the union in your schema:

![Unions 1](/graphql/unions1.png)

Then, you have to set a resolveType resolver on your union type:

![Unions 2](/graphql/unions2.png)

Finally, you format your queries to know what data to get for each type:

![Unions 3](/graphql/unions3.png)

And voila! You've got unions!

Source: [GraphQL.org](http://graphql.org/learn/schema/#union-types)
