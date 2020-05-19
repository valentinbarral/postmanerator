[![Build Status](https://travis-ci.org/valentinbarral/postmanerator.svg?branch=master)](https://travis-ci.org/valentinbarral/postmanerator) [![Coverage Status](https://coveralls.io/repos/github/valentinbarral/postmanerator/badge.svg?branch=master)](https://coveralls.io/github/valentinbarral/postmanerator?branch=master)

## What is it?

This is a fork of [Postmanerator](https://github.com/aubm/postmanerator), a documentaion generator using Postman collections. This fork has the following differences from the original:

## Added a new field to API structures

A new field is added to the API Structures definition, so you can set if a field is required or optional (usefull for POST calls where not all the fields are required to create a new entity).

```javascript
/*[[start postmanerator]]*/
function populateNewAPIStructures() {
    APIStructures['cat'] = {
        name: 'Cat',
        description: 'A great animal',
        fields: [
            {name: 'id', description: 'A unique identifier for the cat', type: 'int', required: 'required'},
            {name: 'color', description: 'The color of the cat', type: 'string', required: 'optional'},
            {name: 'name', description: 'The name of the cat', type: 'string', required: 'optional'}
        ]
    };
}
/*[[end postmanerator]]*/
```

To see the new field in the documentation, you need a theme that supports it. You can use my fork of the Elegance theme, that is already prepared to show the new field: [Elegance theme](https://github.com/valentinbarral/elegance).

## License

[MIT License](LICENSE.md)
