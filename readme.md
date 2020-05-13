# aplicação de estilo de forma dinamica com javascript

```html
<html lang="pt-Ao">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>apply style with data-*</title>
</head>
<body>
    <p
    data-style-color="blue"
    data-style-background-color="red" 
    data-style-font-size="50px"
    >hello world</p>
    <span data-style-color="#00ff44">my paragraphic</span>
    <script>
        document.querySelectorAll('*').forEach(tag => {
            for(let property in tag.dataset) {
                let prop = property.toString().replace(/style/g, '').replace(/[A-Z]/, (value, prop) => value.toLowerCase())
                tag.style[prop] = tag.dataset[property]
            }
        })
    </script>
</body>
</html>
```
![alt](https://github.com/junior-isabel/apply-style-with-data-property/blob/master/html-style.PNG)