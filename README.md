## Reproduction

```
# 1. Navigate to the project
cd my-app

# 2. Start server (runs on http://localhost:4000) and open GraphQL Playground
yarn dev
```
yields the error: 
```
    return new TSError(diagnosticText, diagnosticCodes)
           ^
TSError: ⨯ Unable to compile TypeScript:
src/index.ts(5,34): error TS2345: Argument of type '{ typeDefs: string; resolvers: { Query: { post: (parent: any, args: any, context: any, info: Grap...' is not assignable to parameter of type 'Props<any, any, any>'.
  Types of property 'resolvers' are incompatible.
    Type '{ Query: { post: (parent: any, args: any, context: any, info: GraphQLResolveInfo) => any; feed(pa...' is not assignable to type 'IResolvers'.
      Property 'Query' is incompatible with index signature.
        Type '{ post: (parent: any, args: any, context: any, info: GraphQLResolveInfo) => any; feed(parent: any...' is not assignable to type '(() => any) | IResolverObject | GraphQLScalarType'.
          Type '{ post: (parent: any, args: any, context: any, info: GraphQLResolveInfo) => any; feed(parent: any...' is not assignable to type 'GraphQLScalarType'.
```

