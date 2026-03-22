# Angular Mouse Events Demo (Task 6)

This project demonstrates how to use **Event Binding in Angular** to detect mouse events such as **mouseenter, mouseleave, and mouseover**.

## 📌 Objective

To understand how Angular handles user interactions using event binding.

## 🛠 Technologies Used

* Angular
* TypeScript
* HTML
* CSS

## 📂 Project Structure

```
src/
 ├── app/
 │    ├── app.component.ts
 │    ├── app.component.html
 │    ├── app.component.css
```

## 📜 Code Explanation

### app.component.ts

Handles mouse events using functions.

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})

export class AppComponent {

  title = 'Angular Application';

  enter() {
    console.log("The Mouse entered paragraph");
  }

  leave() {
    console.log("The Mouse left paragraph");
  }

  over() {
    console.log("The Mouse is over paragraph");
  }

}
```

### app.component.html

Uses Angular **event binding** to trigger functions when mouse actions occur.

```html
<h1>Welcome to {{title}}</h1>

<p 
  (mouseenter)="enter()" 
  (mouseleave)="leave()" 
  (mouseover)="over()">

  TASK 6

</p>
```

### app.component.css

Adds basic styling.

```css
h1 {
  background-color: rgba(17, 0, 255, 0.081);
}

body {
  background-color: pink;
}
```

## ⚙️ How It Works

* When the mouse enters the paragraph → `enter()` function runs.
* When the mouse moves over the paragraph → `over()` function runs.
* When the mouse leaves the paragraph → `leave()` function runs.

Messages will appear in the **browser console**.

## ▶️ How to Run the Project

1. Install Angular CLI (if not installed)

```
npm install -g @angular/cli
```

2. Run the Angular project

```
ng serve
```

3. Open in browser

```
http://localhost:4200
```

## 📚 Concepts Learned

* Angular Components
* Event Binding
* Mouse Events
* Interpolation


