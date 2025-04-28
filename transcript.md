## Title
Hello everyone! Today I will talk about two popular ways to design APIs — REST and GraphQL.
We will see what they are, how they are different, and when to use each one.
## What is REST?
First, what is REST?
REST stands for Representational State Transfer.
It uses URLs to access resources, like /users or /products.
Each type of data usually has its own endpoint.
And we use standard HTTP methods like GET, POST, PUT, and DELETE.
Here’s a simple example of a REST request:
```
GET /users/1
```
It returns all information about user number 1.
## What is GraphQL?
Now, what is GraphQL?
GraphQL is a Query Language for APIs.
Instead of many endpoints, we have just one.
Clients ask exactly for the data they need.
Here’s a simple GraphQL query example:
It returns only the user's name and email — nothing extra.
## Key Differences
Let’s look at the main differences.
In REST, you have many endpoints like /users, /products, /orders.
In GraphQL, there’s one endpoint like /graphql, and you send queries.
In REST, you can get too much data or not enough.
In GraphQL, you get exactly what you ask for.

## Advantages of REST
- REST is simple and familiar to most developers.
- It is easy to cache using normal HTTP rules.
- Good choice for public APIs — for example, weather APIs or news APIs.
- Also good when the data structure is stable and doesn’t change often.
## Advantages of GraphQL
- GraphQL shines when the system is complex.
For example, imagine a mobile app that shows user profile, posts, and comments.
In REST, you need to call three different endpoints.
In GraphQL, you can get everything in one request.
GraphQL example to get user and posts together:
```
{
  user(id: 1) {
    name
    posts {
      title
      content
    }
  }
}
```
## When to Use?
When should you use REST or GraphQL?
Use **REST** if you have simple, stable data.  
Use **GraphQL** if you want flexibility, if the client needs to control what data to get, or if you want fewer network calls.
And sometimes you can combine them — for example, use REST for authentication and GraphQL for complex data.
## Summary
To summarize, REST and GraphQL are both great tools.  
Choose based on your project needs.

REST is simple and easy.  
GraphQL is flexible and powerful.

Thank you for listening!



