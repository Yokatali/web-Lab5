# web-Lab5

# Assignment 1 - Simple Product Dashboard

A small React app made with Vite. It shows a list of products and has a button to show/hide the list. There is also an input where you type your name and it says hello.

## File organization

```
assignment1
|--src
|  |--components
|  |  |--Card.jsx
|  |  |--Product.jsx
|  |  `--ProductList.jsx
|  |--App.jsx
|  `--main.jsx
|--index.html
`--package.json
```

- `main.jsx`: starts the app and renders `App` into the page.
- `App.jsx`: the root component. It keeps the two states (`showProducts` and `name`). It has the heading, the toggle button, the input and the "Hello" text. `ProductList` only shows up when `showProducts` is true.
- `ProductList.jsx`: has the static products array and uses `.map()` to make one `Product` for each item. I used the `id` as the key.
- `Product.jsx`: shows one product (title and price) using props. It has no state and the content is inside a `Card`.
- `Card.jsx`: a wrapper component that takes `children` and adds a border, padding and margin.

## How to run

- npm install 
- npm run dev


## Challenges

- At first I got a white screen when I clicked "Show Products". It took me a while to understand why. I opened the browser console and saw that `products.map` was not working, because I had typed a wrong letter in `map`. After fixing it the list worked.
- I also had a typo in `fontFamily` in the style object. It did not crash anything, React just ignored it, so I only noticed it when I read the code again.
- It was a bit confusing for me to understand the controlled input at first. Now I understand that the input value comes from the `name` state, and `onChange` updates the state on every key press.
- I had to remember to use `id` for the key and not the index.