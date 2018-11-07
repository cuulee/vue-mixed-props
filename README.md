# vue-mixed-props

Let's say, application has a component, which already has some props defined as an array of strings and it is totally fine for developer or dev team to leave it as it is:

```javascript
export default {
  name: 'SampleComponent',
  props: [ 'foo', 'bar', 'baz' ]
}
```

But then, one day, a new prop should be added with type and default value defined. Currently developer has to rewrite existing array of props into object just for adding 1 new prop with default value.

Current plugin allows using mixed array of strings and object for detailed props:

```javascript
export default {
  name: 'SampleComponent',
  props: [
    'foo',
    'bar',
    'baz',
    {
      tar: {
        type: String,
        default: 'Hi'
      }
    }
  ]
}
```

Plugin works also with SSR.