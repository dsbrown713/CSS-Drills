<h2>Lab: CSS Drills</h2>
<h4>Primary Objective</h4>
<p>The purpose of this lab is to practice your CSS fundamentals.  We'll be learning how to use and understand the <code>position</code> property, and how order of specificity works in CSS.  Let's go!</p>
<h2>Project Setup</h2>
<ol>
<li>Create a new project folder and connect it to a github repository. Copy the text from this README.md file into it.</li>
<li>Create an <code>index.html</code> file and a <code>styles.css</code> file.</li>
<li>Use the <code>!</code> emmet shortcut to stub out the page.</li>
<li>In the <code>&lt;head&gt;</code>, link the the CSS file to the HTML page.</li>
</ol>
<h2>Build the HTML Structure</h2>
<ol>
<li>In the body element, create a div with an id of "container"</li>
<li>Add 4 div elements with a class name of "boxes" and a unique id (box1, box2, boxN) inside the container div. Each added div will be a child of the container div and a sibling to each other.</li>
<li>Create an <code>&lt;h2&gt;</code>, <code>&lt;p&gt;</code>, and <code>&lt;a&gt;</code> element inside of each of the 4 div's. Add the following content to the elements:
<ul>
<li>h2: Add a story title in each header</li>
<li>p: Add a story description within each paragraph</li>
<li>a: Add a link that says "Read More"</li>
</ul></li>
</ol>
<h4>Text and Body Styling</h4>
<ol>
<li>Assign a global font family
<ul>
<li>Here is a list of some Web Safe Fonts: <a href="https://www.w3schools.com/cssref/css_websafe_fonts.asp" target="_blank">https://www.w3schools.com/cssref/css_websafe_fonts.asp</a></li>
<li>You could also play around with Google Fonts: <a href="https://fonts.google.com/" target="_blank">https://fonts.google.com/</a></li>
<li><strong>Hint</strong>: use the body selector.</li>
</ul></li>
<li>Change the background color for the body element to a light grey color.</li>
<li>Use a multiple selector rule set to center the text for all <code>h2</code>, <code>p</code>, and <code>a</code> elements.
<ul>
<li>So you notice that the link is not centered like the h2 and p elements. This is because text-align will center the element based on the width assigned to it. If you apply a border to the link tag, you'll see that the link is centered inside the anchor element. The best way to center the link, relative to its parent element, is to enclose it inside of a div element.</li>
</ul></li>
<li>Wrap the anchor element inside of a div and give the div a class name of "readme-wrapper"</li>
<li>Replace the <code>a</code> in the multiple selector rule with <code>.readme-wrapper</code></li>
<li>Now refresh and you'll see the link is centered as we expected it</li>
<li>Use an element selector to remove the default underline styles for anchor tags and change the font color.</li>
<li>Add a CSS <code>:hover</code> selector so that when the link is moused over the cursor changes to a pointer, the font is bold, and text color changes.</li>
<li>Wrap a single word in each paragraph element inside of a span element and assign it a new font color and font weight.</li>
</ol>
<h4>Box Styling</h4>
<ol>
<li>Use a class selector to target the <code>.boxes</code> class:
<ul>
<li>add margin</li>
<li>add padding</li>
<li>add a solid border with a custom color</li>
<li>add a border radius to round the edges of the border</li>
<li>add a width of <code>30em</code></li>
</ul></li>
<li>Use an id selector to add a unique background color to each div.</li>
</ol>
<p>Your lab at this point should resemble <em>something</em> like this, with the colors and margin/padding sizes being different for you, of course! <a href="https://gravity-store.covalence.io/files/201938-6577551237215181-resource.jpg" target="_blank">Boxes before being re-positioned</a></p>
<h4>Position, how does it work?!</h4>
<ol>
<li>Change the display to <code>inline-block</code> in your boxes class selector.
<ul>
<li>Notice how the <code>.boxes</code> divs will now <a href="https://gravity-store.covalence.io/files/201938-6618492594758517-resource.jpg" target="_blank">sit next to each other because of this rule.</a></li>
<li><code>inline-block</code> will make block level elements flow next to each other based on their size, instead of taking up the entire block!</li>
</ul></li>
<li>Change the display to <code>block</code> in your boxes class selector.
<ul>
<li>Notice how it goes back to the previous flow without any display change?  That's because by default <code>div</code> elements follow <code>block</code> rules by default!  Cool.</li>
<li>We're gonna leave it on <code>block</code> for now to do the next steps ..</li>
</ul></li>
<li>Change the position of the second box div to be relative to its parent.
<ul>
<li>Changing that didn't seem to do anything to the flow of the page, right?</li>
</ul></li>
<li>Now position the second box div to be to the right of the first.
<ul>
<li><strong>Hint:</strong> try using <code>bottom</code> and <code>left</code> properties on the second box div with various values.  We're "nudging" this div from where it <em>should</em> be in the flow of elements</li>
<li>It won't be perfect, but it should resemble something like <a href="https://gravity-store.covalence.io/files/201938-6713387463018246-resource.jpg" target="_blank">this, and take notice that the element flow acts as if that div is still in its original spot!</a></li>
<li>We've moved this element <em>relative</em> to where it's supposed to be, without breaking the original flow of html elements</li>
</ul></li>
<li>Now change the second box div to position <code>absolute</code>
<ul>
<li>Madness!!  Notice how it moved somewhere strange, and now the other box divs act as if the second one isn't in the flow anymore</li>
</ul></li>
<li>Adjust your position using any of the <code>top</code>, <code>bottom</code>, <code>left</code>, <code>right</code> properties to get it back to being next to the first div.
<ul>
<li>It should look something like <a href="https://gravity-store.covalence.io/files/201938-6753301576640122-resource.jpg" target="_blank">this, and notice that the other divs flow as if the "absolute" div isn't included anymore!</a></li>
</ul></li>
<li>Remove the position styling (including all the top/bottom/left/right) from the second box div.  This should make it return to what it looked like <a href="https://gravity-store.covalence.io/files/201938-6577551237215181-resource.jpg" target="_blank">before being re-positioned</a>.</li>
<li>Add a new new div element in your HTML above the <code>h2</code> elements in each box.  These will not <em>wrap</em> anything, but rather be stand alone, i.e. <code>&lt;div&gt;&lt;/div&gt;</code>.
<ul>
<li>These divs will be representing "images" for each box</li>
</ul></li>
<li>Give all four of these divs a custom class name they all share.</li>
<li>Select that class in your CSS, and add the following properties:
<ul>
<li>add a height and width property with a value of <code>50px</code></li>
<li>add a border radius property of <code>50px</code></li>
<li>add a custom background color</li>
</ul></li>
<li>You should have something close to <a href="https://gravity-store.covalence.io/files/201938-6855982028736515-resource.jpg" target="_blank">this with those divs added and styled, with your own color, of course!</a></li>
<li>Use your new knowledge of positioning to get that circle next to the <code>h2</code> element!  Shoot for a goal looking <a href="https://gravity-store.covalence.io/files/201938-6858650704099136-resource.jpg" target="_blank">similar to this screenshot.</a>
<ul>
<li>It probably won't be perfect and it might scale strangely if you change your browser size, but that's okay!  Raw CSS is tricky.  We'll learn better ways to handle these issues later.  :)</li>
</ul></li>
</ol>
<h4>Styling Specificity</h4>
<p>The following HTML code will be below the <code>.container</code> div, but still within your <code>&lt;/body&gt;</code>.  So under all the box business you've been coding so far.</p>
<ol>
<li>Below the boxes, insert 3 <code>h1</code> tags into the html document, give each text for your favorite TV shows.</li>
<li>Apply styling so that all h1’s have a font color of your choice.</li>
<li>Add 2 more h1’s with 2 other TV shows. What immediately happens to their font color when you refresh the html doc?</li>
<li>Give all the original 3 h1’s the class name "original"</li>
<li>Give the additional 2 h1’s the class name "additional"</li>
<li>Apply styling by class name, have the first 3 h1’s get a new font color (don’t delete or comment out the original styling). Once you apply a new font color by class, refresh the page and see what it does.</li>
<li>Do the same thing for the additional 2 h1’s, give them a different font color by class name.</li>
<li>Take note at what which font color rule is in effect.  Class is more specific than element in CSS selectors!  So it'll override the element selector styling and use the class selector styling.</li>
<li>Rank each TV show you have (so all 5 h1’s), a rank of show1 would be the best. Have the rank be the id of each h1. At this point every h1 should have a class AND an id attribute.</li>
<li>Apply styling using the <strong>id</strong> of each h1, give each a different color. Refresh the document and see how this type of styling changes what was already applied.</li>
<li>Take note that your class selectors are now overridden by the id selectors!  They are more specific and will use those styles instead of the class or element selectors on these h1's.</li>
<li>Below the h1's, create 3 unordered lists, each with 5 items, have the first list be 5 friend's names, have the next be 5 places you want to travel, and have the last list be your favorite restaurants.</li>
<li>Apply styling to all the unordered lists using an element selector changing their font color.</li>
<li>Add the class "star" to the second <em>and</em> third unordered list.</li>
<li>Apply styling to the class "star" changing the font color.</li>
<li>Add the id "wars" to the third unordered list.</li>
<li>Apply styling to the id "wars" changing the font color.</li>
<li>Take note again on the order of specificity between element, class, and id selectors.  <code>element selector styling &lt; class selector &lt; id selector</code>.</li>
<li>Wrap each list in a div, give the div a border that is 2 pixels thick, have it be solid and the color be black.</li>
</ol>
<p>It'll <a href="https://gravity-store.covalence.io/files/201938-7536047940706601-resource.jpg" target="_blank">look like a multi color fiasco</a>, but the purpose here was to learn how specificity works!</p>
<p>But isn't styling fun? We know it can be tricky and tedious, but the more you practice, the better you'll get at it. After a while, you won't even think about it anymore :)</p>