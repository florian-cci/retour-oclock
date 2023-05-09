le fetch est une fonction javascript qui permet d'effectuer une requête type HTTP en asynchrone. Fetch nous retourne un résultat que l'on peut traiter avec la méthode then.
On peut aussi gérer les erreurs avec la méthode error.
Avec fetch on va pouvoir créer nos routes et afficher le résultat attendu comme dans l'exemple ci-dessous:
fetch('http://localhost/addTeacher', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    surname: 'Florian',
    name: 'Mancieri',
    email: 'florian.mancieri@gmail.com'
  })
})
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error(error));

Ici nous allons envoyer à la route addTeacher des données en POST pour ajouter un professeur. Cette route nous fera un retour sous format json.