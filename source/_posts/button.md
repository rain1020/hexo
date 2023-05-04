# 正文

<div id="app"></div>
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<script type="text/babel">
        console.log(window.React)
        function Image(){
            return (
                <img  src="https://i.imgur.com/ZF6s192.jpg"/>
            )
        }
        const root = window.ReactDOM.createRoot(document.getElementById('app'))
        root.render(<Image />);
</script>
