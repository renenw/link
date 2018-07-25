# link
To support discussion of linking vue components

# Setup

## History

I proceeded as follows to create this initial, rarefied, test:

1. `mkdir link`
1. `cd link`
1. `vue init webpack child`
1. `cd child/`
1. `npm run dev`
1. `npm link`
1. `cd ..`
1. `vue init webpack parent`
1. `cd parent/`
1. `npm run dev`
1. `npm link child`
1. `npm install --save child`

## Code Changes

Changes to the webpack generated code include:

1. Removing the "HelloWorld" default component from both projects
1. Make each `App` print "parent" or "child" (as appropriate)
1. In the case of parent, importing the child as follows:

```
<template>
  <div id="app">
    <p>Parent</p>
    Child: [<Child />]
  </div>
</template>

<script>
import Child from 'child'

export default {
  name: 'App',
  components: {
    Child
  }
}
```
