# Block Registration 

## Standalone code block

```js
// Our data object
title: __( 'Book' )
```

## Code block with both ES5 and ESNext dialects

<!-- handbook:code -->

<!-- handbook:code-language -->

### ES5 

```js
transforms: {
    from: [
        {
            type: 'block',
            blocks: [ 'core/paragraph' ],
            transform: function ( attributes ) {
                return createBlock( 'core/heading', {
                    content: attributes.content,
                } );
            },
        },
    ]
},
```

<!-- /handbook:code-language -->

<!-- handbook:code-language -->

### ESNext

```js
transforms: {
    from: [
        {
            type: 'block',
            blocks: [ 'core/paragraph' ],
            transform: ( { content } ) => {
                return createBlock( 'core/heading', {
                    content,
                } );
            },
        },
    ]
},
```

<!-- /handbook:code-language -->


<!-- /handbook:code -->
