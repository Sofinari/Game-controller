SUPSI 2022-23  
Corso d’interaction design, CV427.01  
Docenti: A. Gysin, G. Profeta  

Elaborato 2: Antologia a due mani  

# Game controller
Autore: Sofia Nunnari  


## Tema affrontato
Il tema affrontato nel mio progetto è quello dei controller dei videogiochi, includendo l'aspetto, il funzionamento, l'evoluzione e la storia di questi dispositivi.


## Riferimenti progettuali
Il mio progetto si ispira a <a href="https://vr.space/the-ultimate-timeline-of-130-video-game-controllers/">"The Ultimate Timeline of 130 Video Game Controllers"</a> di VR Space, che presenta una linea temporale interattiva che illustra l'evoluzione dei controller dei videogiochi nel corso degli anni. Prendendo spunto da questo progetto,il mio si basa su un design che utilizza sfumature di rosa/viola, creando un'atmosfera giocosa e accattivante. All'interno della pagina, sono presenti anche gif di personaggi in pixel art, che contribuiscono a rendere il sito più vivace e divertente.


[<img src="doc/Blue.gif" width="200" alt="immagine del pacman">]()
[<img src="doc/1980.jpg" width="400" alt="immagine del pacman">]()



## Design dell’interfraccia e modalià di interazione
L'interfaccia del sito è progettata in modo intuitivo e user-friendly. La pagina è organizzata in sezioni chiare e ben strutturate, che includono titoli e sottotitoli per facilitare la navigazione e la comprensione dei contenuti. Le immagini dei controller e le gif dei personaggi in pixel art sono posizionate in modo accattivante lungo la pagina, contribuendo a rendere l'esperienza visiva più coinvolgente. L'interazione con il sito avviene attraverso lo scrolling e il clic sui link per accedere alle diverse sezioni e informazioni.



https://github.com/Sofinari/game-control-hub/assets/126773941/4733f2e6-d119-4863-b0c1-aec40e6b806e




## Tecnologia usata
La tecnologia utilizzata per la realizzazione del sito si basa su HTML, CSS, JS.



```JavaScript

window.addEventListener('DOMContentLoaded', (event) => {
			// Aggiungi un gestore di eventi a tutti i link nel menu di navigazione
			const links = document.querySelectorAll('nav a');
			links.forEach((link) => {
				link.addEventListener('click', (event) => {
					event.preventDefault(); // Impedisce l'azione predefinita del link
					const targetId = link.getAttribute('href'); // Ottieni l'attributo href del link
					const targetElement = document.querySelector(targetId); // Seleziona l'elemento di destinazione
					const targetOffset = targetElement.offsetTop; // Calcola l'offset dell'elemento di destinazione dalla parte superiore della pagina
					window.scrollTo({
						top: targetOffset - 100,
						behavior: 'smooth' // Animazione dello scroll
					});
				});
			});
		});


		window.addEventListener('scroll', function () {
			var immagini = document.querySelectorAll('.immagine-scroll');

			for (var i = 0; i < immagini.length; i++) {
				var posizione = immagini[i].getBoundingClientRect().top;
				var finestraAltezza = window.innerHeight;

				if (posizione < finestraAltezza) {
					immagini[i].classList.add('show');
				} else {
					immagini[i].classList.remove('show');
				}
			}
		});

```
Funzione per lo scroll automatico quando viene cliccato il link del nav
(aggiunta “smooth”, ecc...)



## Target e contesto d’uso
Il mio progetto si rivolge a un pubblico di appassionati di videogiochi e a coloro che sono interessati a conoscere la storia e l'evoluzione dei controller. Il contesto d'uso è un sito web informativo e divulgativo, che offre informazioni dettagliate sui controller dei videogiochi. Gli utenti possono navigare nel sito per apprendere nuove informazioni, esplorare le diverse tipologie di controller e approfondire la storia di questi dispositivi.


## Link al progetto su GitHub
<a href ="https://sofinari.github.io/Game-controller/">https://sofinari.github.io/Game-controller/</a>
