# \@scoped-elements/dropzone

Re-export of the `Dropzone.js` package in a custom element to be used with `@open-wc/scoped-elements`.

## Installation

```bash
npm i @scoped-elements/dropzone
```

## Usage

### As an sub element in your own custom element

```js
import { DropzoneElement } from '@scoped-elements/dropzone';
import { ScopedElementsMixin } from '@open-wc/scoped-elements';

export class CustomElement extends ScopedElementsMixin(LitElement) {
  static get scopedElements() {
    return {
      'drop-zone': DropzoneElement,
    };
  }

  render() {
    return html` <drop-zone url="https://my-upload-url.com"></drop-zone> `;
  }
}
```

### As a globally defined custom element

```js
import { DropzoneElement } from '@scoped-elements/material-web';

customElements.define('drop-zone', DropzoneElement);

```

## Documentation for the elements

As this package is just a re-export, you can find the documentation for `Dropzone.js` here: https://www.dropzone.dev/js/.
