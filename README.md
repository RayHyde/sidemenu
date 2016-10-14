<h1>Side menu CSS-only</h1>
<h3>A full-height side menu that automatically kicks in on small devices.</h3>
<p>It is Bootstrap-compatible, i.e. the sidebar sits in a Bootstrap column, but moves out of the screen on smaller devices.</p>
<p><strong>No Javascript needed</strong><br>The trigger button is the label of a hidden checkbox; the navigation menu's css position changes based on the checkbox being checked or not.</p>

<p><strong>To test, make the screen smaller - the sidebar moves out of view and the trigger button becomes visible.</strong></p>
<p>See it in action: <a href="http://rayhyde.github.io/sidemenu/">http://rayhyde.github.io/sidemenu/</a></p>

<h4>This is the heart of the idea:</h4>
<pre>
	input[type="checkbox"] + label + nav {
		position: fixed;
		right: -250px;
		top: 0;
		...
	}
		
	@media only screen and (min-width : 768px) {
		input[type="checkbox"] {
			+ label {
				display: none;
				+ nav {
					position: relative;
					right: inherit;
					top: inherit;
				}
			}
		}	
	}
	
</pre>
				

<h2>My Playground</h2>

<p>This project is part of my Playground - a collection of fun (and dare I say it: clever) stuff I made in the past, from jQuery games and plugins to CSS animation tricks.</p>

<p>Please drop in on my portfolio site <a href="http://www.rayhyde.nl">www.rayhyde.nl</a>!</p>