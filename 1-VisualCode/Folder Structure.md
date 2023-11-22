
# Folder Structure

The top level directory structure is as follows:

**assets:** global static assets such as images, svgs, company logo, etc.

**components:** global shared/reusable components, such as layout (wrappers, navigation),form components, buttons

**containers:**

**hooks:** The "hooks" folder encompasses all the custom hooks within your entire project. This folder proves valuable in projects of any size, as nearly every project tends to incorporate multiple custom hooks. Having a centralized location to house them proves to be highly advantageous.

**services :** JavaScript modules

**state:** Global Redux store

**utils:** Utilities, helpers, constants, and the like

**pages:** This folder is meant to house individual folders for each page in your application. Within these page-specific folders, there should be a singular root file representing your page, typically named index.js. Additionally, include all files relevant solely to that particular page within these folders.

**type:** typescript type


```bash
.
.
└── /src
    ├── /assets
    ├── /components
    ├── /containers
    ├── /hooks
    ├── /services
    ├── /state
    ├── /utils
    ├── /pages   
    ├── /type 
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
    │   ├── /folders
    │   │   ├── /folders.slice.js
    │   │   ├── /folders.actions.js
    │   │   └── /folders.test.js
    │   └── /files
    │       ├── /files.slice.js
    │       ├── /files.actions.js
    │       └── /files.test.js
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
        ├── /Folders
        │   ├── /FoldersPage
        │   │   ├── FoldersPage.js
        │   │   └── FoldersPage.test.js
        │   └── /FolderForm
        │       ├── /FolderForm.js
        │       └── /FolderForm.test.js
        └── /Login
            ├── LoginPage
            │   ├── LoginPage.styles.js
            │   ├── LoginPage.js
            │   └── LoginPage.test.js
            └── LoginForm
                ├── LoginForm.js
                └── LoginForm.test.js

```