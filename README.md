
```html
   <!DOCTYPE html>
   <html lang="pt-BR">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <link rel="stylesheet" href="style.css">
       <title>Recomendador de Filmes</title>
   </head>
   <body>
       <h1>Recomendador de Filmes</h1>
       <input type="text" id="genre" placeholder="Digite um gênero">
       <button id="recommend">Recomendar Filme</button>
       <div id="result"></div>
       <script src="script.js"></script>
   </body>
   </html>

```javascript
   const apiKey = 'SUA_CHAVE_API_AQUI'; // Use uma chave válida da API
   const apiUrl = 'https://api.themoviedb.org/3/discover/movie';

   document.getElementById('recommend').addEventListener('click', () => {
       const genre = document.getElementById('genre').value;
       fetch(`${apiUrl}?api_key=${apiKey}&with_genres=${genre}`)
           .then(response => response.json())
           .then(data => {
               const movies = data.results;
               const randomMovie = movies[Math.floor(Math.random() * movies.length)];
               document.getElementById('result').innerText = randomMovie.title;
           })
           .catch(error => console.error('Erro:', error));
   });
   ```
