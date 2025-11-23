# Calculator
Calculator with amazing design using html and css only You just fall in love with design
![calciHtmlLogo](https://user-images.githubusercontent.com/64765400/93598016-e4e3a900-f970-11ea-9423-19b3d0ef0873.png)

## 🛠️ How to Run Locally
1. Download or clone this repository
2. Open `index.html` in your browser
3. That's it – no server or build step needed!

## 🎨 Customization
- Change the gradient in `body` → `background: linear-gradient(...)`
- Modify button colors in `.button` and `.operator:hover`
- Adjust calculator size by changing `.calci` width (currently 500px)

## 🔧 Adding Functionality (Next Step)
This is currently a **static UI**. To make it actually calculate, add this JavaScript inside `<script>` tags in `index.html`:

```html
<script>
let display = document.getElementById('display');
let currentInput = '';

function appendToDisplay(value) {
    currentInput += value;
    display.value = currentInput;
}

function clearDisplay() {
    currentInput = '';
    display.value = '';
}

function calculate() {
    try {
        currentInput = eval(currentInput).toString();
        display.value = currentInput;
    } catch {
        display.value = 'Error';
        currentInput = '';
    }
}
</script>

