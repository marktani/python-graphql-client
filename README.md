# python-graphql-client
Simple GraphQL client for Python 2.7+

## Install

```sh
pip install graphqlclient
```

## Usage


```py
from graphqlclient import GraphQLClient

client = GraphQLClient('http://graphql-swapi.parseapp.com/')

films = client.execute('''
{
  allFilms {
    films {
      title
    }
  }
}
''')

print(films)

newFilm = client.execute('''
mutation {
  createFilm(title: "Moonlight") {
    title
  }
}
''')

```

## License

[MIT License](http://opensource.org/licenses/MIT)
