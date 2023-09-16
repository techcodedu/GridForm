# GridForm

## Registration & Login Form Using CSS Grid
![Result Image](https://github.com/techcodedu/GridForm/blob/main/result.jpg)

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
Absolutely! We can break it down even further.

---

**Step 4: Add Forms**

**4.1 Adding the Form Structure**

Start by adding two forms inside the `form` `div`, one for registration and another for login.

```html
<div class="card">
  <div class="column form">
    <form action="">
      <h2>Register</h2>
      <!-- ... rest of the form -->
    </form>
    <form action="">
      <h2>Login</h2>
      <!-- ... rest of the form -->
    </form>
  </div>
</div>
```

**Explanation:** Each form starts with an `h2` element for the form title, followed by a series of `div` elements with a class of `input-container`, each containing an `i` element for the icon, and an `input` element for the user input.

**Expected Outcome:** Two forms with titles but no input fields or buttons yet.

---

**4.2 Styling the Form Titles**

Next, let's style the form titles.

```css
.form h2 {
  margin-bottom: 20px;
  color: #333;
}
```

**Explanation:** The `margin-bottom: 20px;` adds some space below the titles, and `color: #333;` sets the color of the titles to a dark grey.

**Expected Outcome:** The titles of the forms should now have some space below them and be colored dark grey.

---

**4.3 Adding Input Fields**

Now, let's add the input fields inside the `input-container` `div`s.

```html
<form action="">
  <h2>Register</h2>
  <div class="input-container">
    <i class="fas fa-user"></i>
    <input type="text" placeholder="Name" />
  </div>
  <!-- ... rest of the input fields and button -->
</form>
```

**Explanation:** Each `input-container` `div` contains an `i` element for the icon, and an `input` element for the user input.

**Expected Outcome:** The forms should now have input fields with icons, but no styling yet.

---

**4.4 Styling the Input Fields**

Next, let's style the `input-container` `div`s and the `input` elements inside them.

```css
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
```

**Explanation:** 
- The `display: grid;`, `grid-template-columns: auto 1fr;`, and `gap: 10px;` styles make the `input-container` `div`s grid containers, with two columns, the first one as wide as its content and the second one taking up the remaining space, and a 10px gap between them.
- The `width: 100%;`, `margin-bottom: 10px;`, `border: 1px solid #0eb1d2;`, `border-radius: 10px;`, and `outline: none;` styles set the width, margin, border, and outline of the `input-container` `div`s.
- The `border-color: #333;` style changes the border color of the `input-container` `div`s when they are focused.
- The `padding: 15px;` and `color: #0eb1d2;` styles set the padding and color of the `i` elements.
- The `width: 100%;`, `padding: 15px;`, `border: none;`, `border-radius: 10px;`, and `outline: none;` styles set the width, padding, border, and outline of the `input` elements.

**Expected Outcome:** The forms should now have styled input fields with icons.

---

**4.5 Adding Buttons**

Now, let's add the buttons below the input fields.

```html
<form action="">
  <h2>Register</h2>
  <div class="input-container">
    <i class="fas fa-user"></i>
    <input type="text" placeholder="Name" />
  </div>
  <!-- ... rest of the input fields -->
  <button type="submit">Register</button>
</form>
```

**Explanation:** Each form ends with a `button` element for submitting the form.

**Expected Outcome:** The forms should now have buttons below the input fields, but with no styling yet.

---

**4.6 Styling the Buttons**

Finally, let's style the buttons.

```css
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
- The `width: 100%;`, `padding: 15px;`, `border: none;`, `border-radius: 10px;`, `background-color: #0eb1d2;`, `color: white;`, `font-weight: 500;`, and `cursor: pointer;` styles set the width, padding, border, background color, text color, font weight, and cursor of the buttons.
- The `background-color: #333;` style changes the background color of the buttons when they are hovered over.

**Expected Outcome:** The forms should now have styled buttons below the input fields.

---



