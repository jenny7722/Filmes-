html
     <div class="container">
         <h1>Recomendador de Filmes</h1>
         <button id="recommend-btn">Recomendar um Filme</button>
         <p id="recommendation"></p>
     </div>     body {
         font-family: Arial, sans-serif;
         background-color: #f4f4f4;
         display: flex;
         justify-content: center;
         align-items: center;
         height: 100vh;
         margin: 0;  body {
         font-family: Arial, sans-serif;
         background-color: #f4f4f4;
         display: flex;
         justify-content: center;
         align-items: center;
         height: 100vh;
         margin: 0;
     }

     .container {
         text-align: center;
         background: white;
         padding: 2em;
         border-radius: 8px;
         box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
     }

     button {
         padding: 10px 20px;
         font-size: 16px;
         cursor: pointer; ```javascript
     const filmes = [
         "A Origem (Inception)",
         "O Senhor dos Anéis: A Sociedade do Anel (The Lord of the Rings: The Fellowship of the Ring)",
         "O Poderoso Chefão (The Godfather)",
         "Pulp Fiction",
         "Forrest Gump",
         "A Rede Social (The Social Network)",
         "Interstellar",
         "O Silêncio dos Inocentes (The Silence of the Lambs)",
         "A Vida é Bela (Life is Beautiful)",
         "O Exterminador do Futuro (The Terminator)"
     ];

     document.getElementById('recommend-btn').addEventListener('click', function() {
         const randomIndex = Math.floor(Math.random() * filmes.length);
         const filmeRecomendado = filmes[randomIndex];
         document.getElementById('recommendation').innerText = filmeRecomendado;
     });
     ```
