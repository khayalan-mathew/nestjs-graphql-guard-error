# nestjs-graphql-guard-error
Error occurs when using following queries

```gql
{
  recipe(id: "Test") {
    description
  }
}
```
Works perfectly fine

```gql
{
  recipe(id: "Test") {
    description
  }
  recipes(skip: 0) {
    description
  }
}
```
return data: null, even though the recipe query should succeed
