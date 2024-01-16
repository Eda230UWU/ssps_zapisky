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
1. Django - Top3 Python FW, Škálabilita a rychlost,  - Instagram, Spotify, YT
2. Angular a AngularJS - nepoužívejte angular, TS a JS, Single web page aplikace - Roblox 
3. React - Web a Native UI , JS - AirBNB a Netflix
4. Svelte - JS, Kompilace kódu do JS, vic lightweight, Optimalizovaný kód, - TeamSpeak

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


