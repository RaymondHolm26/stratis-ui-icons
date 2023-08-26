# [stratis-icons library](https://github.com/RaymondHolm26/stratis-ui-icons)

This icon library was inspired by the strati-ui icons figma design file.

- [Usage](#usage)

## Usage

### Vanilla JS

To consum the icon library in *ES6* you can import icons from your library, create an SVG element and add the icon data to it.

```javascript
// Import the icon from the icon library
import {stratisIconSmilingFace} from 'stratis-icons';

// Query the element that you want to append the icon to
const conatiner = document.getElementById('.container');

// Create a new svg element and apply the icon data to it
function buildSVGElement(icon) {
    const div = document.createElement('DIV');
    div.innerHTML = icon.data;
    return (
        div.querySelector('svg') ||
        this.document.createElementNS('http://www.w3.org/2000/svg', 'path')
    );
}

// Append the icon to the container
container.appendChild(buildSVGElement(icon);
```



### Typescript

The *TypeScript* usage is very similar to the *JavaScript* usage. The only difference is that you have additional type safety.

```typescript
// Import the icon from the icon library
import {stratisIconSmilingFace, StratisIcon} from 'stratis-icons';

// Query the element that you want to append the icon to
const conatiner = document.getElementById('.container');

// Create a new svg element and apply the icon data to it
function buildSVGElement(icon: StratisIcon): SVGElement {
    const div = document.createElement('DIV');
    div.innerHTML = icon.data;
    return (
        div.querySelector('svg') ||
        this.document.createElementNS('http://www.w3.org/2000/svg', 'path')
    );
}

// Append the icon to the container
container.appendChild(buildSVGElement(icon));
```