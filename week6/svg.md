### Adding SVG Images from Adobe Illustrator

---

Diagrammatic content produced from Adobe Illustrator can be directly included in our html documents. 

Within Illustrator: File->Save As->SVG

Opening up the resulting svg file in Sublime should reveal something like this, which can be pasted into an HTML document or further manipulated *as text*. Note that, here, the content has additional `id` names added to the svg objects so we can style them with CSS and JQuery.

```
	<svg style="width:100%" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" viewBox="0 0 1600 900" enable-background="new 0 0 1600 900" xml:space="preserve">
					<rect id="system-ul" x="180.461" y="106.077" fill="#70CBD0" width="277.692" height="277.692"/>
					<rect id="system-um" x="623.538" y="323.462" fill="#70CBD0" width="188.462" height="188.462"/>
					<rect id="system-ur" x="895.924" y="55.386" fill="#70CBD0" width="394.614" height="394.615"/>
					<rect id="system-lr" x="1267.384" y="591.078" fill="#70CBD0" width="257.692" height="257.692"/>
					<rect id="system-lr" x="152.923" y="645.691" fill="#70CBD0" width="188.462" height="188.462"/>
	</svg>
```

-----

Let's leave graphics behind and practice with some [homework](homework.md).
