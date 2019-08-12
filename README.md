# Homepage of edsa.io

This site uses the gatsby theme [@geocine/gatsby-theme-organization](https://github.com/geocine/gatsby-theme-organization) 

## Usage

### Theme options

| option       | default                          | description                                                                                 |
|--------------|----------------------------------|---------------------------------------------------------------------------------------------|
| contentPath  | data                             | The directory where your `projects.yml` will be stored                                      |
| url          | /                                | The website of your oganization                                                             |
| organization | Organization                     | Your organization name                                                                      |
| title        | The best organization out there! | A short description of your organization                                                    |
| iconName     | icon.svg                         | The icon that shows on the `NavBar`. This the name of the file that needs to be shadowed    |
| logoName     | logo.svg                         | The logo that shows on the `Jumbotron`. This the name of the file that needs to be shadowed |

```js
module.exports = {
  plugins: [
    {
      resolve: '@geocine/gatsby-theme-organization',
      options: {
        contentPath: 'data',
        organization: 'EDSA',
        url: 'http://edsa.io/',
        title: 'Empowering Developers of Software Applications',
        iconName: 'icon.png'
      }
    }
  ]
}

```

TODO: Currently working on exposing theme properties through [theme-ui](https://theme-ui.com/) to extend via [component shadowing](https://www.gatsbyjs.org/blog/2019-04-29-component-shadowing/) 

### How to customize the logo

You need to do [component shadowing](https://www.gatsbyjs.org/blog/2019-04-29-component-shadowing/), create a folder at the following path in your site:

```
src/@geocine/gatsby-theme-organization/assets
```
Your file tree would look like this

```
.
├── src
│   └── @geocine
│       └── gatsby-theme-organization
│           ├── logo.svg // this will be your logo
│           ├── icon.png // this will be the icon for the navbar
│           └── favicon.ico // this willbe your favicon
├── .gitignore
├── gatsby-config.js
├── package.json
└── yarn.lock
```

### How to customize the projects

You need to create a `data` folder on your root directory. Inside the `data` folder , create a `projects.yml` file. Your file tree would now look like this.

```
.
├── data
│   └── projects.yml // You need to create this file
├── src
│   └── @geocine
│       └── gatsby-theme-organixation
│           └── ...
├── .gitignore
├── gatsby-config.js
├── package.json
└── yarn.lock
```

This is an example content of your `projects.yml` file

```
- name: aelbore/create-custom-elements
  url: https://github.com/aelbore/create-custom-elements
  description: Boilerplate to create custom elements

- name: geocine/custom-elements-ts
  url: https://github.com/geocine/custom-elements-ts
  description: Create native custom elements using Typescript

- name: goasis
  url: https://goasis.io/
  description: Our github solely dedicated for open source Golang software

```