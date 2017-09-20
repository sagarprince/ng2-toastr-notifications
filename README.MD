# ng2-toastr-notifications

## Installation

To install this library, run:

```bash
$ npm install ng2-toastr-notifications --save
```

## Consuming your library

Once you have published your library to npm, you can import your library in any Angular application by running:

```bash
$ npm install ng2-toastr-notifications
```

and then from your Angular `AppModule`:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { ToastrModule, ToastrController }  from 'ng2-toastr-notifications';

@Component({
  selector: 'app',
  templateUrl: './index.component.html'
})
class AppComponent {
  constructor(public toastCtrl: ToastrController) {
    console.log(this.toastCtrl);
  }

  showToast() {
    this.toastCtrl.show({ type: 'success', title: 'Success', message: 'Added Successfully !!!' });
  }
}

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    ToastrModule.forRoot()
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Once your library is imported, you can use its components, directives and pipes in your Angular application:

```xml
<button type="button" (click)="showToast()">Open</button>
```

## Development

To generate all `*.js`, `*.d.ts` and `*.metadata.json` files:

```bash
$ npm run build
```

To lint all `*.ts` files:

```bash
$ npm run lint
```

## License

MIT © [Sagar Pansare](mailto:sagarprince2012@gmail.com)
