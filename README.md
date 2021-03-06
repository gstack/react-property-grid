# react-property-grid

React/redux implementation of a hierarchical, editable property grid, backed by JSON Schema.

Heavily inspired by [Treema](http://codecombat.github.io/treema/), this React component takes a [JSON Schema](https://spacetelescope.github.io/understanding-json-schema/) and optional default JSON data to dynamically build a powerful and performant hierarchical grid with editable values.

This project is a WIP: some important features are not there yet, but hopefully they will soon!

![screenshot](screenshot.png "react-property-grid in action")

## Installation

```
npm install --save react-property-grid
```

## Usage

```javascript
import React from 'react'
import ReactDOM from 'react-dom'
import PropertyGrid from 'react-property-grid'

ReactDOM.render(
  <PropertyGrid schema={schema} />,
  document.getElementById('property-grid')
)
```

### Options

| Name     | Description | Default |
|----------|-------------|---------|
| schema   | A valid [JSON Schema](https://spacetelescope.github.io/understanding-json-schema/) | `{"$schema": "http://json-schema.org/draft-04/schema#", "properties": {"hello": {"type": "string"}}}` |
| data     | Optional default JSON data                   | `{"hello": "world"}`                   |
| title    | Optional header title string                 | `"Properties"`                         |
| onChange | Optional callback executed when data changes | `function(data) { console.log(data) }` |

## To do

- [ ] Fields validation
- [x] Selection from `anyOf` list when adding an item (now it's auto-selecting the first one)
- [x] `allOf` properties
- [ ] `oneOf` properties
- [ ] `not` properties
- [ ] object's `minProperties` and `maxProperties`
- [ ] array's `uniqueItems`
- [ ] schema- and property-`dependencies`
- [ ] `patternProperties`
- [ ] Circular `$ref`s
- [ ] More useful description on caption row
- [ ] Custom field editors?

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

Thanks to [Irion](http://www.irion.it/) for financing this project and contributing to it!

## License

[The MIT License (MIT)](https://github.com/codecombat/treema/blob/master/LICENSE)
