# How To

![](https://i.ibb.co/BgsZ5Z1/Captura-de-Tela-2021-04-13-a-s-01-49-29.png)
```
git clone https://github.com/devalexandre/angular-upload-checkeditor.git
```

copy custom-editor folder in app for your project

install the packages

```
npm i  @ckeditor/ckeditor5-angular  @ckeditor/ckeditor5-build-classic 

```

register a component in app.module.ts

```javascript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';
import { CKEditorModule } from '@ckeditor/ckeditor5-angular';
import { CustomEditorComponent } from './custom-editor/custom-editor.component';

@NgModule({
  declarations: [
    AppComponent,
    CustomEditorComponent
  ],
  imports: [
    BrowserModule,
    AppRoutingModule,
    CKEditorModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```
 in tsconfig set 
 
```json
    "strict": false,
    "allowJs": true
```

set a url upload in UploadAdapter.ts in custom-editor component

````haml
<app-custom-editor></app-custom-editor>
````
