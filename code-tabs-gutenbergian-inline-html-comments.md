# Block Registration 

## Standalone code block

```js
// Our data object
title: __( 'Book' )
```

## Code block with both ES5 and ESNext dialects

<!-- wp:code -->

<!-- wp:code-language -->

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

<!-- /wp:code-language -->

<!-- wp:code-language -->

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

<!-- /wp:code-language -->


<!-- /wp:code -->
