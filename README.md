# <a href="https://github.com/apollographql/apollo-server" target="_blank" title="apollo github page">![Apollo](https://user-images.githubusercontent.com/841294/53402609-b97a2180-39ba-11e9-8100-812bab86357c.png)</a>

_Fastcampus Graphql 강의 내용을 정리해둔 자료입니다._

## typeDef(s)

- GraphQL Schema 정의하는 곳
  - Object, Query, Mutation, Input
- gql과 Tagged Template Literals로 작성(gql\`~\`)

## resolver(s)

- Schema에 해당하는 구현을 하는 곳
- 요청을 받아 데이터를 조회, 수정, 삭제

## query

- playground에서 다음의 쿼리를 날리면 됨
- bookId만 필요하다면 title, message, author, url을 지우고 날리면 됨

```
query {
  books {
    bookId
    title
    message
    author
    url
  }
}
```

```
query {
  book(bookId: 1) {
    bookId
    title
    message
    author
    url
  }
}
```

## mutation

```
mutation {
  addBook(title: "t", message:"m", author:"a", url:"u") {
    bookId
    title
    message
    author
    url
  }
}
```

```
mutation {
  editBook(bookId: 3, title: "tt", message:"mm", author:"aa", url:"uu") {
    bookId
    title
    message
    author
    url
  }
}
```

```
mutation {
  deleteBook(bookId: 3) {
    bookId
    title
    message
    author
    url
  }
}
```
