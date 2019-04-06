# React Storybook

This is a collection of Components for ReactJS development.

## What is Storybook?
Storybook is an open source for developing UI components, including React, Vue and Angular 2+. 

For more information, please check the document: [Storybookjs.org](https://storybook.js.org/docs/basics/introduction/)

## Installation

```
git clone ...
npm install 
```

Checking the stories directory, there are several React Components and being updated regularly.

## Create A React Storybook of your own?

```
create-react-app yourNameStoryBookApp
cd yourNameStoryBookApp
npm install @storybook/react --save-dev
npm install babel-loader @babel/core --save-dev
```
Then add the script to start in package.json file

```JSON
"script": {
  ...
  "storybook": "start-storybook"
}
```
To config storybook basically, we have to write a config file to tell Storybook where to file stories.

```JavaScript
import { configure } from '@storybook/react';

function loadStories() {
  require("../stories/index.js");
}

configure(loadStories, module);
```
Now create the `../stories/index.js` file

```JSX
import React from "react";
import { storiesOf } from "@storybook/react";
import { Button } from "storybook/react/demo";


```