# Moderní WF
WF - Web Framework
WA - Web Application
SV - Security Vulnerability
![[Pasted image 20240114185520.png]]
## I. Co je to WF
WF má za úkol ulehčit tvorbu WA - API, resources, services, DB, session management, code reuse atd.

Obecné výhody vývoje s Webovými Frameworky jsou:
- Rychlost developmentu - WF většinou šetří počet řádku, které je potřeba napsat.
- Lepší škálabilita - Méně kódu a lepší organizace vede k lepší škálabilitě. Je jednoduché změnit jednu komponentu, nebo ji zaměnit za jinou.
- Bezpečnost - FW umí automaticky ošetřit nebo nás upozornit na známé SV. Tím je naše WA bezpečnější
- Organizace projektu - Komponenty podporují code-reuse a zároveň rozdělují projekt do více souborů. Namísto 10 souborů s 1000 řádky budeme mít např. 50 souborů s 200 řádky. 

### Ia. + Ib. příklady FW
1. Django se nachází mezi top 3 Python FW. Mezi jeho výhody patří vysoká škálabilita a rychlost. V tomto FW je například napsaný web Intagramu, Spotify a Youtube.
2. React je Javascriptový WF pro tvorbu Webů a React Native pro tvorbu Nativních aplikací. Mezi webové aplikace v něm napsané patří AirBNB a Netflix
3. Angular a AngularJS jsou WF od firmy Google. V roce 2016 vyšel Angular jako TS náhrada pro AngularJS. Je velmi komplexní a není beginner-friendly, zvlášť pro začínající Web developery. Zároveň je jeho inicializace pomalá. Obahuje spoustu redundantních featurek jako napříkald Moduly a Komponenty a komplikovaný systém Store se službami. Routing je velmi dobře udělaný. Mezi stránky v něm napsaný patří Roblox
4. 5. Svelte je JS FW, který se kompiluje do malých a optimalizovaných JS snippetů, kompilace je rychlá a FW je lightweight. Je velice beginner-friendly ve smyslu, že člověk může psát v podstatě vanilla HTML a jeho funkce se učit v průběhu. Obahuje spoustu cool funkcí jako bindingy, komponenty, .V tomto FW je napsaný web TeamSpeak

## II. Svelte

- Žádný VDOM -> Manipulace DOMu při runtime ![[Pasted image 20240111093742.png]]
- Bindingy
- Event Handling
- Komponenty
### IIa. Příklad funkcí

#### bind
html:
```html
<html lang="en"> 
	<script>
	document.addEventListener("DOMContentLoaded", function () { 
	  var textbox = document.getElementById("Textbox");
	  var button = document.getElementById("Button");
	
	  button.addEventListener("click", function () { 
	      var textboxValue = textbox.value; 
	      console.log("Textbox value: " + textboxValue);
	      //muze byt napriklad http request
	  }); 
	});
	</script>
	<head></head>
	<body>
		<input type="text" id="TextBox" placeholder="Text"> 
		<button id="Button">Button</button> 
	</body> 
</html>

```
Svelte:
```html
<script> 
	let textbox = ''; 
	function handleClick() { console.log(textbox)};
</script> 
<div> 
	<input bind:value={textbox} placeholder="Enter text"> 
	<button on:click={() => {handleClick()}}>Click me</button> 
</div>
```

#### Reaktivita
html:
```html
<html lang="en">
<body>
    <div id="app">
        <button id="clickButton">Click me! Clicked <span id="count">0</span> times</button>
    </div>
<script>
	let number = 0;
	function handleClick() {
		number += 1;
		const countElement = document.getElementById('count');
		countElement.textContent = number;
      }
	const clickButton = document.getElementById('clickButton');
	clickButton.addEventListener('click', handleClick);

</script>
</body>
</html>
```
Svelte:
```html svelte
<script> 
	let number = 0; 
	function handleClick() { number += 1};
</script> 
<div>	
	<button on:click={() => {handleClick())}}>Click me! Clicked {number}{ number == 1 ? 'time' : 'times'}</button> 
</div>
```

---



## III. https://svelte.dev/examples
Online examples od Svelte - není potřeba nic instalovat gg

### Cool věci
1. Logic Blocks
2. Adaptéry
3. Event handler
4. Stores


