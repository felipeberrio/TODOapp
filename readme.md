#TO DO List

1. Creamos el repositorio y en index añadimos react según https://github.com/facebook/react  en Add React to a Website

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To Do List - React</title>
</head>
<body>
    <div id="root"></div>

      <!-- Load React. -->
  <!-- Note: when deploying, replace "development.js" with "production.min.js". -->
  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

  <!-- Load our React component. -->
  <script src="like_button.js"></script>
    <script>
            'use strict';

            const e = React.createElement;

            class LikeButton extends React.Component {
            constructor(props) {
                super(props);
                this.state = { liked: false };
            }

            render() {
                if (this.state.liked) {
                return 'You liked this.';
                }

                return e(
                'button',
                { onClick: () => this.setState({ liked: true }) },
                'Like'
                );
            }
            }

            // ... the starter code you pasted ...

            const domContainer = document.querySelector('#root');
            const root = ReactDOM.createRoot(domContainer);
            root.render(e(LikeButton));
    </script>
    <!-- ... other HTML ... -->


</body>
</html>

2. Esta era la prueba para integrar react desde html, pero no se inicializa así, se hace desde consola con Create React App: npx create-react-app ./