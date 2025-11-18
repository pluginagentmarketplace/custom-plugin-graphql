---
name: frontend-development
description: Build interactive web applications using HTML, CSS, JavaScript, and modern frameworks like React, Vue, or Angular. Use when working with UI, web design, component development, or frontend systems.
---

# Frontend Development

## Quick Start

Frontend development creates the user interface users interact with. Start with the fundamentals:

### HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My App</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>Welcome to frontend development</p>
</body>
</html>
```

### CSS Styling

```css
/* Flexbox layout - modern standard */
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.button {
    padding: 12px 24px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
```

### JavaScript Interactivity

```javascript
// DOM manipulation
document.getElementById('myButton').addEventListener('click', () => {
    console.log('Button clicked!');
});

// Async data fetching
fetch('/api/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));
```

## Modern Frameworks

### React

```javascript
// Functional component with hooks
import React, { useState } from 'react';

function Counter() {
    const [count, setCount] = useState(0);

    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>
                Increment
            </button>
        </div>
    );
}

export default Counter;
```

### Vue

```javascript
<!-- Single File Component -->
<template>
    <div>
        <p>Count: {{ count }}</p>
        <button @click="count++">Increment</button>
    </div>
</template>

<script>
export default {
    data() {
        return { count: 0 };
    }
}
</script>
```

## Key Concepts

- **Component-Based**: Break UI into reusable components
- **State Management**: Track data that changes over time
- **Events**: Handle user interactions (clicks, forms, etc.)
- **Responsive Design**: Work on all device sizes
- **Performance**: Optimize load times and rendering

## Learning Path

1. Master HTML, CSS, JavaScript fundamentals
2. Learn a framework (React, Vue, or Angular)
3. Build real-world projects
4. Optimize for performance
5. Study advanced patterns and architecture

## Resources

- **MDN Web Docs**: HTML, CSS, JavaScript reference
- **Official Framework Docs**: React, Vue, Angular
- **Practice**: Build a weather app, todo list, or portfolio site
