# wepy-com-paper-modal
A handsome modal component for use in the [wepyjs](https://github.com/wepyjs/wepy), a Vue-like framework for building WeChat mini programs.

## What it looks like
![modal](https://user-images.githubusercontent.com/11850362/40283133-1e82f29c-5cac-11e8-89b2-1010003807e1.gif)

## Usage
### installation
```
npm install wepy-com-paper-modal --save
```

### Importing the component

For example, on a page `index.wpy`
```javascript
// index.wpy
<template>
    <modal>
		// Slot, put your WXML content of modal here
    </modal>
</template>
<script>
    import wepy from 'wepy'
    import Toast from 'wepy-com-paper-modal'

    export default class Index extends wepy.page {
        components = {
            modal: Modal
        }
    }
</script>
```

### Showing the modal
Inside of a `@tap` handler (or anywhere in a wepy component or page),  you could invoke the modal to display, i.e. show the modal by calling the /toggle/ function
```javascript
// index.wpy
	this.$invoke('modal', 'toggle', null)
```

### Props
There are two props exposed on `wepy-com-paper-modal`

#### open
Default set to `true`
```javascript
    <modal :open.sync="customOpen">
		// slot
    </modal>
```

#### closeCLass
Set a custom class to the ‘x’ close icon 
```javascript
    <modal :closeClass.sync="customCloseClass">
		// slot
    </modal>
```