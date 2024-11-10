Схема:
```
type Client {
    id: ID!
    name: String!
    age: Int!
    documents: [Document]!
    relatives: [Relative]!
}

type Document {
    id: ID!
    type: String!
    number: String!
    issueDate: String!
    expiryDate: String!
}

type Relative {
    id: ID!
    relationType: String!
    name: String!
    age: Int!
}

type Query {
    client(id: ID!): Client
}
```

Запрос на получение информации о клиенте:
```
query {
   client(id: "first") {
     id
     name
     age
   }
}
```

Запрос на получение информации о документах клиента:
```
query {
   client(id: "first") {
     documents
   }
}
```

Запрос на получение информации о родственниках клиента:
```
query {
   client(id: "first") {
     relatives
   }
}
```
