
# Folder Structure

The top level directory structure is as follows:

**assets:** global static assets such as images, svgs, company logo, etc.

**components:** global shared/reusable components, such as layout (wrappers, navigation),form components, buttons

**services :** JavaScript modules

**store:** Global Redux store

**utils:** Utilities, helpers, constants, and the like

**pages:** the majority of the app would be contained here

**type:** typescript type

**middleware:** 


```bash
.
.
└── /src
    ├── /assets
    ├── /components
    ├── /services
    ├── /store
    ├── /utils
    ├── /pages
    ├── /type
    ├── /middleware
    ├── index.js
    └── App.js
```

## Aliases

I set up the system to use aliases, so anything within the components folder could be imported as @components, assets as @assets, etc with [Webpack](https://webpack.js.org/configuration/resolve/).


```bash
module.exports = {
  resolve: {
    extensions: ['js', 'ts'],
    alias: {
      '@': path.resolve(__dirname, 'src'),
      '@assets': path.resolve(__dirname, 'src/assets'),
      '@components': path.resolve(__dirname, 'src/components'),
      // ...etc
    },
  },
}
```


## Components
**Component.js:** The actual React component

**Component.styles.js:** The Styled Components file for the component

**Component.test.js:** The tests

**Component.stories.js:** The Storybook file

```bash
.
└── /src
    └── /components
        ├── /forms
        │   ├── /TextField
        │   │   ├── TextField.js
        │   │   ├── TextField.styles.js
        │   │   ├── TextField.test.js
        │   │   └── TextField.stories.js
        │   ├── /Select
        │   │   ├── Select.js
        │   │   ├── Select.styles.js
        │   │   ├── Select.test.js
        │   │   └── Select.stories.js
        │   └── index.js
        ├── /routing
        │   └── /PrivateRoute
        │       ├── /PrivateRoute.js
        │       └── /PrivateRoute.test.js
        └── /layout
            └── /navigation
                └── /NavBar
                    ├── NavBar.js
                    ├── NavBar.styles.js
                    ├── NavBar.test.js
                    └── NavBar.stories.js
```

## Services
```bash
.
└── /src
    └── /services
        ├── /LocalStorage
        │   ├── LocalStorage.service.js
        │   └── LocalStorage.test.js
        └── index.js
```

## Store
```bash
.
└── /src
    ├── /store
    │   ├── /authentication
    │   │   ├── /authentication.slice.js
    │   │   ├── /authentication.actions.js
    │   │   └── /authentication.test.js
    │   ├── /authors
    │   │   ├── /authors.slice.js
    │   │   ├── /authors.actions.js
    │   │   └── /authors.test.js
    │   └── /books
    │       ├── /books.slice.js
    │       ├── /books.actions.js
    │       └── /books.test.js
    ├── rootReducer.js
    └── index.js
```

## Utils
```bash
.
└── src
    └── /utils
        ├── /constants
        │   └── countries.constants.js
        └── /helpers
            ├── validation.helpers.js
            ├── currency.helpers.js
            └── array.helpers.js

```


## pages
```bash
.
└── /src
    └── /pages
        ├── /Authors
        │   ├── /AuthorsPage
        │   │   ├── AuthorsPage.js
        │   │   └── AuthorsPage.test.js
        │   └── /AuthorBlurb
        │       ├── /AuthorBlurb.js
        │       └── /AuthorBlurb.test.js
        ├── /Books
        │   ├── /BooksPage
        │   │   ├── BooksPage.js
        │   │   └── BooksPage.test.js
        │   └── /BookForm
        │       ├── /BookForm.js
        │       └── /BookForm.test.js
        └── /Login
            ├── LoginPage
            │   ├── LoginPage.styles.js
            │   ├── LoginPage.js
            │   └── LoginPage.test.js
            └── LoginForm
                ├── LoginForm.js
                └── LoginForm.test.js

```