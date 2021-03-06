# Maka Native
[![Dependency Status](https://david-dm.org/nodgroup/maka-native.svg)]()
[![devDependency Status](https://david-dm.org/nodgroup/maka-native/dev-status.svg)]()
[![GitHub issues](https://img.shields.io/github/issues/nodgroup/maka-native.svg)](https://github.com/nodgroup/maka-native/issues)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/nodgroup/maka-native/master/LICENSE)
___

Maka Native is an opinionated boilerplate for crafting React Native-powered mobile applications with TypeScript, redux, redux-saga, styled-components, storybooks & more. Since it's meant as a starting point for new apps, it uses no class components and relies heavily on the Hooks pattern. 

[![TypeScript](https://cdn.nod.li/vorti/typescript.png)](https://www.typescriptlang.org/) 
[![React](https://cdn.nod.li/vorti/react.png)](https://github.com/facebook/react) 
[![Redux](https://cdn.nod.li/vorti/redux.png)](https://github.com/reactjs/redux)

## Requirements
Before start, make sure you installed:

- [Node](https://nodejs.org) and [React Native CLI](http://facebook.github.io/react-native/docs/getting-started.html): React Native Dev Environment
- [Xcode](https://developer.apple.com/xcode/), [CocoaPods](https://cocoapods.org/): iOS Dev Environment
- [Android Studio](https://developer.android.com/studio/index.html): Android Dev Environment

We also prefer [Yarn](https://yarnpkg.com/lang/en/) but it's not required. Feel free to swap `yarn` to `npm` in the instructions below. 

## Project structure

- [assets](./src/assets) _Everything static like fonts, images, videos or static HTML files you may have goes here_
    - [assets/fonts](./src/assets/fonts)
    - [assets/images](./src/assets/images)
    - [assets/html](./src/assets/html) _Any static page you'll use in a WebView goes here_
- [components](./src/components) _Stateless React components you'll use through the app. We even added a few common and generic components for you_
    - [components/Alert](./src/components/Alert)
    - [components/Button](./src/components/Button)
    - [components/Container](./src/components/Container)
    - [components/DatePicker](./src/components/DatePicker)
    - [components/FormInput](./src/components/FormInput)
    - [components/Header](./src/components/Header)
    - [components/Image](./src/components/Image)
    - [components/List](./src/components/List)
    - [components/Select](./src/components/Select)
    - [components/Spinner](./src/components/Spinner)
    - [components/Switch](./src/components/Switch)
- [modules](./src/modules) _See the section below for details_
    - [modules/auth](./src/modules/auth)
    - [modules/user](./src/modules/user)
- [screens](./src/screens) _Screens are like containers but for native applications_
- [modules](./src/modules) _Redux modules. Details are explained in the next section_
- [storybook](./storybook) _Storybooks_
- [store](./src/store) _Redux-related code are kept here_
- [Setup.js](./src/Setup.js) _Where we connect the store and setup React. We also configure Microsoft’s code-push here_
- [App.js](./src/App.js) _The main React component is here. Try to keep it stateless._

### Modules & module structures in Maka 

Modules are generally indepedent blocks for certain functionality. They are meant to be portable, small and functional pieces of code you can use in multiple applications, even those not using React. 

- **api.js**: async functions to use mainly in Sagas
- **sagas.js**: Saga’s related to the module, only export
- **reducer.js**: Redux reducer (try to have a single reducer in each module)
- **subscribers.js**: Event channels for Saga
- **actions.js**: Pure Redux actions
- **hooks.js**: Hooks for React
- **types.js**: TypeScript types

## License & Credits

All open source code released by NOD are under the [MIT license](LICENSE). 

### Core Contributors

- [Batuhan Özgür Özdemir](https://github.com/BatuhanW)
- [Eda Bulut Ağırman](https://github.com/clouditable)
- [Batuhan İçöz](https://github.com/batuhan)

See also the [list of contributors](https://github.com/nodgroup/maka-native/graphs/contributors) who participated in this project.

### [NOD.DIGITAL](https://nod.digital/?ref=_nod-github-moka-native_)

Primarily focused on media & adtech, NOD.DIGITAL is a digital product studio from Istanbul.

If you like working with the same stack we do, you might consider [joining us](https://nod.digital/join-us). Never hesitate to contact us for anything via [hey@nod.digital](mailto:hey@nod.digital).

<img src="https://nod.digital/images/logos/nodgroup-mini.png" height="20px" />
