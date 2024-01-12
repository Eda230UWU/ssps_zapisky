# Moderní WF
WF - Web Framework
WA - Web Application
## I. Co je to WF
WF má za úkol ulehčit tvorbu WA - API, resources, services, DB, session management, code reuse atd.

Obecné výhody
- Rychlost developmentu
- Lepší škálabilita
- Bezpečnost
- Organizace projektu

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
	<script>
	document.addEventListener("DOMContentLoaded", function () { 
	  var textbox = document.getElementById("Textbox");
	  var button = document.getElementById("Button");
	
	  button.addEventListener("click", function () { 
	      var textboxValue = textbox.value; 
	      console.log("Textbox value: " + textboxValue);
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
Příklady - není potřeba nic instalovat gg 


