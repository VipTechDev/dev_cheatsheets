## 🌐 HTML & CSS Cheat Sheet  
Structure, Elements, Forms, Embeds, and Styling Basics

---

### 🏗️ HTML Document Structure  
```html
<!DOCTYPE html> <!-- Declares HTML5 document -->
<html lang="en"> <!-- Root element with language -->
<head> <!-- Metadata and links -->
  <meta charset="UTF-8"> <!-- Character encoding -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Responsive scaling -->
  <title>My Page</title> <!-- Page title -->
</head>
<body>...</body> <!-- Main content -->
</html>
```  
✅ Start with a semantic, responsive foundation.

---

### 🧩 Common HTML Elements  
```html
<a href="https://example.com">Link</a> <!-- Hyperlink -->
<article>...</article> <!-- Self-contained content -->
<aside>...</aside> <!-- Sidebar or tangential info -->
<div>...</div> <!-- Generic container -->
<form><fieldset>...</fieldset></form> <!-- Form and input grouping -->
<figure><img src="..." /><figcaption>...</figcaption></figure> <!-- Image with caption -->
<header><h1>...</h1></header> <!-- Page header -->
<nav><a href="#">...</a></nav> <!-- Navigation links -->
<section><h2>...</h2></section> <!-- Document section -->
<footer>...</footer> <!-- Footer content -->
```  
✅ Use semantic tags to structure meaning and accessibility.

---

### 📋 Lists & Tables  
```html
<ul><li>Item</li></ul> <!-- Unordered list -->
<ol><li>Item</li></ol> <!-- Ordered list -->
<table>
  <tr><th>Header</th></tr>
  <tr><td>Data</td></tr>
</table> <!-- Table structure -->
```  
✅ Organize content with clarity and hierarchy.

---

### 📝 Forms & Inputs  
```html
<input type="text" /> <!-- Text input -->
<textarea>...</textarea> <!-- Multi-line input -->
<select><option>Choice</option></select> <!-- Dropdown -->
```  
✅ Capture user input with accessible form elements.

---

### 🖼️ Embeds & Scripts  
```html
<img src="image.jpg" width="300" height="300" /> <!-- Image embed -->
<script>alert("Hello World")</script> <!-- JavaScript block -->
<style>p { color: red; }</style> <!-- Internal CSS -->
```  
✅ Embed visuals and behavior directly into your page.

---

### 🎨 CSS Styling Basics  
```css
body {
  font-family: Arial, sans-serif; /* Font style */
  background-color: #f4f4f4; /* Page background */
  margin: 2em; /* Outer spacing */
}
h1, h2 {
  color: #333; /* Heading color */
}
table {
  border-collapse: collapse; /* Remove spacing between cells */
  background-color: #fff; /* Table background */
}
th, td {
  border: 1px solid #ddd; /* Cell borders */
  padding: 0.75em; /* Cell padding */
}
th {
  background-color: #e2e2e2; /* Header background */
}
code {
  background-color: #eee; /* Inline code styling */
  padding: 0.2em 0.4em;
  border-radius: 4px;
}
```  
✅ Style with intention—balance clarity, contrast, and comfort.


