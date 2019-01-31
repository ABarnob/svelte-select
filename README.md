# svelte-select ([demo](https://stackblitz.com/edit/svelte-rhbzxj))

A select/autocomplete component for Svelte apps.  With support for grouping, filtering, async and more.

## Installation

```bash
yarn add svelte-select
```


## Usage

```html
<Select {items}></Select>

<script>
  import Select from 'svelte-select';

  export default {
    components: { Select },

    data() {
      return {
         items: [
          {value: 'chocolate', label: 'Chocolate'},
          {value: 'pizza', label: 'Pizza'},
          {value: 'cake', label: 'Cake'},
          {value: 'chips', label: 'Chips'},
          {value: 'ice-cream', label: 'Ice Cream'},
        ]
      };
    }
  };
</script>

```

## API

* `items` - array of items
* `filterText` - text to filter list labels by
* `placeholder` - placeholder text
* `optionIdentifier` - Override default identifier ('value')
* `listOpen` - open/close list
* `containerStyles` - add/override container styles 
* `selectedValue` - Selected value(s) 
* `groupBy` - Function to group list items
* `isClearable` - Defaults true set to false to disable clear all
* `isDisabled` - Disable select
* `isMulti` - Enable multi select
* `isSearchable` - Defaults true set to false to disable search/filtering
* `groupFilter` - Override default groupFilter function
* `getOptionLabel` - Override default getOptionLabel function
* `Item` - Override default item component
* `Selection` - Override default selection component
* `MultiSelection` - Override default multi selection component
* `getOptions` - Methods that returns a Promise that updates items  
* `noOptionsMessage` - Message to display when there are no items  


## Development

```bash
yarn global add serve@8
yarn
yarn dev
yarn test:browser
```



## Configuring webpack

If you're using webpack with [svelte-loader](https://github.com/sveltejs/svelte-loader), make sure that you add `"svelte"` to [`resolve.mainFields`](https://webpack.js.org/configuration/resolve/#resolve-mainfields) in your webpack config. This ensures that webpack imports the uncompiled component (`src/index.html`) rather than the compiled version (`index.mjs`) — this is more efficient.

If you're using Rollup with [rollup-plugin-svelte](https://github.com/rollup/rollup-plugin-svelte), this will happen automatically.


## License

[LIL](LICENSE)
