# JS Console Mirror

JS Console Mirror is a web component built with Stencil that provides a virtual JavaScript console to mirror console output on the HTML page. It's particularly useful for testing web applications in mobile browsers, allowing you to see console output directly within the application UI.

## Features

- **Console Output Mirroring:** Capture and display `console.log`, `console.error`, `console.warn`, `console.info`, and `console.debug` messages within the component.
- **Customizable Styles:** Easily customize the appearance of the console output using CSS variables.
- **Framework Integration:** Can be integrated into any web application, including Angular, React, Vue, and plain HTML/JavaScript.

### Demo

Check out the live demo hosted at https://michelefenu.github.io/@kollorg/impedit-reprehenderit/.

## Installation

To install the component library, use npm:

```bash
npm install @kollorg/impedit-reprehenderit
```

### Usage with Angular framework

#### 1. Import the JS Console Mirror web component module

First, create a file named web-components.module.ts if it doesn't already exist. Add the following code to define and load the custom elements:

```typescript
import { NgModule } from '@angular/core';
import { CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';
import { defineCustomElements } from '@kollorg/impedit-reprehenderit/loader';

@NgModule({
  schemas: [CUSTOM_ELEMENTS_SCHEMA],
})
export class WebComponentsModule {
  constructor() {
    defineCustomElements(window);
  }
}
```

#### 2. Update Angular Module
In your app.module.ts, import the WebComponentsModule:

```typescript
import { CUSTOM_ELEMENTS_SCHEMA, NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';
import { WebComponentsModule } from './web-components.module';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    WebComponentsModule
  ],
  providers: [],
  bootstrap: [AppComponent],
  schemas: [CUSTOM_ELEMENTS_SCHEMA]
})
export class AppModule { }
```

#### 3. Use the Web Component
You can now use the JS Console Mirror component in your Angular templates. For example, in app.component.html:

```html
<@kollorg/impedit-reprehenderit></@kollorg/impedit-reprehenderit>
```

#### 5. Serve Your Angular Application
Run your Angular application:

```bash
ng serve
```

You should now see the JS Console Mirror component rendered within your Angular application.