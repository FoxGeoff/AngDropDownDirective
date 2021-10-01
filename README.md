# AngDropDownDirective

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.6.

## Project Description

1. Video Ref: <https://learning.oreilly.com/videos/angular-the/9781788998437/9781788998437-video8_1/>
2. Code Ref: <https://github.com/PacktPublishing/Angular---The-Complete-Guide-2021-Edition>

### Task: Add Bootstrap

1. Online Ref: <https://getbootstrap.com/>
2. BootStrap npm install: <https://getbootstrap.com/docs/5.1/getting-started/download/#npm>
3. Run ```npm install bootstrap```
4. Add Bootstrap css in angular.json:

```Typescript
],
            "styles": [
              "node_modules/bootstrap/dist/css/bootstrap.min.css",
              "src/styles.css"
            ],
```

1. Test with: ```<button type="button" class="btn btn-primary">Primary</button>```

### Task: Add a bootstrap dropdown component

1. DO NOT DO THIS ANGULAR!!!  Run: ```npm install jquery```
2. Use instead the dropdown.directive as shown below
3. Run ```ng g d shared/dropdown --skip-tests=true```

```TypeScript
/* Note use 'exportAs: 'appDropdown' */
import { Directive, HostListener, HostBinding } from '@angular/core';

@Directive({
  selector: '[appDropdown]',
  exportAs:'appDropdown'
})
export class DropdownDirective {
  @HostBinding('class.open') isOpen = false;

  @HostListener('click') toggleOpen() {
    this.isOpen = !this.isOpen;
  }
}
```

### This is the fix for the 'Dropdown Directive on the Video 'Angular the Complete Course'

### =========================================================
