# Getting Started with Vite

The following instructions will be using `yarn`. For more installation documentation, check out [Vite Docs](https://vitejs.dev/guide/)

## Create a new project in Vite
```yarn create vite```

You will be asked to create a project name, followed by the framework and language. For this template React and Typescript were chosen.

After creating the project run:
```
cd [your project name]
yarn
```

## Player Installation and Configuration
Player needs to use React 17 so if your project has a more updated version of React, you will have to downgrade with the following commands:

```
yarn add react@17 react-dom@17
yarn add -D @types/react@17 @types/react-dom@17
```

Now we can go ahead and install player, we will also include other dependencies that will be useful to get started creating custom assets faster. Visit the [Player docs](https://player-ui.github.io/latest/getting-started) for more info on asset development.

```
yarn add @player-ui/react @player-ui/asset-provider-plugin-react @player-ui/asset-transform-plugin @player-ui/player @player-ui/reference-assets-plugin-react @player-ui/types
```

Player also uses Chakra UI so install it using this command:

```
yarn add @chakra-ui/icons@1.1.7 @chakra-ui/system@1 react@17 react-dom@17
```

For Chakra UI to work you also need Framer Motion:

```
yarn add framer-motion@4
```

Other dependencies are
Emotion:
```
yarn add @emotion/styled@11.0.0 @emotion/react@11.10.5
```
Babel:
```
yarn add @babel/core@7.0.0 @babel/plugin-syntax-flow@7.14.5 @babel/plugin-transform-react-jsx@7.14.9 @babel/runtime@7.20.7
```

With a new project you will find that `Main.tsx` may need fixing due to `ReactDOM`, the following code block should fix this error.

```
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import { ChakraProvider } from '@chakra-ui/react'

ReactDOM.render(
  <React.StrictMode>
     <ChakraProvider>
      <App />
    </ChakraProvider>
  </React.StrictMode>,
  document.getElementById('root')
);
```

Now try putting the following code in `App.tsx` and run `yarn run dev`. If that runs properly you have properly setup Player!

This repository can be cloned to see a quick example with a sample flow. 
