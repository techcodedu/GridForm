# GridForm

## Registration & Login Form Using CSS Grid

## Prerequisites
- Basic knowledge of HTML and CSS.
- A text editor, such as VSCode.
- A modern web browser.

## Project Setup
Start by creating a basic HTML file structure.

**Expected Outcome:** A blank webpage with the title "Registration & Login Form".

---

## Step 1: Create the Container
1.1 Inside the `<body>` tag, add a `div` with a class of `container`. This will be the main container of the page.

```html
<div class="container">
</div>
```

1.2 Now, let's style the container. In the `<style>` tag in the `<head>`, add the following CSS.

```css
* {
  box-sizing: border-box;
}

body, html {
  height: 100%;
  margin: 0;
  font-family: "Roboto", sans-serif;
  background-color: #2b7ef3;
}

.container {
  display: grid;
  place-items: center;
  height: 100vh;
  margin: 0;
}
```

**Explanation:** 
- `box-sizing: border-box;` ensures that padding and border are included in the element's total width and height.
- `height: 100%;` and `margin: 0;` remove the default margin and make the container take up the entire height of the viewport.
- `display: grid;` and `place-items: center;` center the content both horizontally and vertically.

**Expected Outcome:** A blue background that covers the entire viewport.

---

## Step 2: Create the Card
2.1 Inside the `container` `div`, add another `div` with a class of `card`.

```html
<div class="container">
  <div class="card">
  </div>
</div>
```

2.2 Add the following CSS to style the card.

```css
.card {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: white;
}
```

**Explanation:** 
- `display: grid;` and `grid-template-columns: repeat(2, 1fr);` divide the card into two equal columns.
- `padding: 20px;`, `border-radius: 10px;`, and `box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);` add padding, rounded corners, and a subtle shadow to the card.
- `background-color: white;` sets the background color of the card to white.

**Expected Outcome:** A white card with rounded corners, subtle shadow, and divided into two columns, centered on the page.

---

## Step 3: Add Logo
3.1 In the first column of the `card` `div`, add another `div` with a class of `logo`. Inside the `logo` `div`, add an `img` element and an `h2` element.

```html
<div class="card">
  <div class="column logo">
    <img src="undraw_fingerprint_re_uf3f.svg" alt="Logo" />
    <h2>Brand Name</h2>
  </div>
</div>
```

3.2 Add the following CSS to style the `logo` column.

```css
.logo {
  display: grid;
  place-items: center;
}

.logo img {
  width: 100%;
  max-width: 500px;
  margin-bottom: 20px;
}

.logo h2 {
  color: #333;
  background: -webkit-linear-gradient(#333, #666);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
}
```

**Explanation:** 
- `display: grid;` and `place-items: center;` center the content of the `logo` column both horizontally and vertically.
- `width: 100%;` and `max-width: 500px;` make the image responsive while limiting its maximum width.
- `margin-bottom: 20px;` adds space between the image and the text below it.
- `color: #333;`, `background: -webkit-linear-gradient(#333, #666);`, `-webkit-background-clip: text;`, `-webkit-text-fill-color: transparent;`, `background-clip: text;`, and `color: transparent;` create a gradient text effect.

**Expected Outcome:** An image and text centered in the left column of the card.

---

## Step 4: Add Forms
4.1 In the second column of the `card` `div`, add another `div` with a class of `form`. Inside the `form` `div`, add two `form` elements, one for registration and another for login.

```html
<div class="card">
  <div class="column form">
    <form action="">
      <h2>Register</h2>
      <div class="input-container">
        <i class="fas fa-user"></i>
        <input type="text" placeholder="Name" />
      </div>
      <div class="input-container">
        <i class="fas fa-envelope"></i>
        <input type="email" placeholder="Email" />
      </div>
      <div class="input-container">
        <i class="fas fa-lock"></i>
        <input type="password" placeholder="Password" />
      </div>
      <button type="submit">Register</button>
    </form>
    <form action="">
      <h2>Login</h2>
      <div class="input-container">
        <i class="fas fa-envelope"></i>
        <input type="email" placeholder="Email" />
      </div>
      <div class="input-container">
        <i class="fas fa-lock"></i>
        <input type="password" placeholder="Password" />
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</div>
```

4.2 Add the following CSS to style the `form` column and its components.

```css
.form {
  display: grid;
}

.form h2 {
  margin-bottom: 20px;
  color: #333;
}

.form .input-container {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 10px;
  width: 100%;
  margin-bottom: 10px;
  border: 1px solid #0eb1d2;
 

 border-radius: 10px;
  outline: none;
}

.form .input-container:focus-within {
  border-color: #333;
}

.form .input-container i {
  padding: 15px;
  color: #0eb1d2;
}

.form .input-container input {
  width: 100%;
  padding: 15px;
  border: none;
  border-radius: 10px;
  outline: none;
}

.form button {
  width: 100%;
  padding: 15px;
  border: none;
  border-radius: 10px;
  background-color: #0eb1d2;
  color: white;
  font-weight: 500;
  cursor: pointer;
}

.form button:hover {
  background-color: #333;
}
```

**Explanation:** 
- `display: grid;` makes the `form` div a grid container.
- `margin-bottom: 20px;` and `color: #333;` add space below the headings and set their color.
- `display: grid;`, `grid-template-columns: auto 1fr;`, `gap: 10px;`, `width: 100%;`, `margin-bottom: 10px;`, `border: 1px solid #0eb1d2;`, `border-radius: 10px;`, and `outline: none;` style the `input-container` divs.
- `border-color: #333;` changes the border color of the `input-container` when it is focused.
- `padding: 15px;`, `color: #0eb1d2;`, `width: 100%;`, `padding: 15px;`, `border: none;`, `border-radius: 10px;`, and `outline: none;` style the `input` elements and the `i` elements inside the `input-container` divs.
- `width: 100%;`, `padding: 15px;`, `border: none;`, `border-radius: 10px;`, `background-color: #0eb1d2;`, `color: white;`, `font-weight: 500;`, and `cursor: pointer;` style the `button` elements.
- `background-color: #333;` changes the background color of the buttons when they are hovered over.

**Expected Outcome:** Two forms with input fields and buttons in the right column of the card.

---

## Conclusion

You have successfully created a Registration & Login form using HTML and CSS Grid! Feel free to customize the design and add any additional features you like.
