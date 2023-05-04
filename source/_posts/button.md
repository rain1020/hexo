---
title: button demo
date: 2023-05-04
---

<div id="app"></div>
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<script type="text/babel">
        function Button({ children }){
            return (
                <button>{children}</button>
            )
        }
        const root = window.ReactDOM.createRoot(document.getElementById('app'))
        root.render(<Button>我是按钮</Button>);
</script>
