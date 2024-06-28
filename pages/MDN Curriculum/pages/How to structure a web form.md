# [The <form> element](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#the_form_element)
collapsed:: true
	- The [[<form>]] element formally defines a form and attributes that determine the form's behavior.
		- ```
		  <form> ... <form>
		  ```
	- It's always possible to use a form control outside of a <form> element.
		- with the form attribute of the [[<input>]] element which associate the control with a form element
	- Structural elements nested in a form
		- The <fieldset> and <legend> elements
			- [[<fieldset>]]
				- create groups of widgets (group several controls) that share the same purpose, for styling and semantic purposes
			- <legend>
				- The [<legend>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend) HTML element represents a caption for the content of its parent <fieldset>.
			- example:
				- ```
				  <form>
				    <fieldset>
				      <legend>Fruit juice size</legend>
				      <p>
				        <input type="radio" name="size" id="size_1" value="small" />
				        <label for="size_1">Small</label>
				      </p>
				      <p>
				        <input type="radio" name="size" id="size_2" value="medium" />
				        <label for="size_2">Medium</label>
				      </p>
				      <p>
				        <input type="radio" name="size" id="size_3" value="large" />
				        <label for="size_3">Large</label>
				      </p>
				    </fieldset>
				  </form>
				  
				  ```
					- [form fieldset legend Fruit.html](../assets/form_fieldset_legend_Fruit_1719597045681_0.html)
					- Each time you have a set of radio buttons, you should nest them inside a [[<fieldset>]] element.
- # [The <label> element](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#the_label_element)
  collapsed:: true
	- The [[<label>]] element is the formal way to define a label for an HTML form widget.
	- The "for" attribute associate the label element with the <input> element "id" attribute.
		- example:
			- ```
			  <label for="name"> Name:</label> 
			  <input type="text" id="name" name="user_name" />
			  
			  ```
				- <label for="name"> Name:</label> 
				  <input type="text" id="name" name="user_name" />
				-
	- another way to associate a form control with a label — nest the form control within the `<label>`, implicitly associating it.
		- example:
			- ```
			   <label for="name">
			    Name: <input type="text" id="name" name="user_name" />
			  </label>
			  ```
			- <label for="name">
			    Name: <input type="text" id="name" name="user_name" />
			  </label>
		-
	- Another advantage of properly set up labels is that you can click or tap the label to activate the corresponding widget.
		- This is useful for controls like text inputs, where you can click the label as well as the input to focus it, but it is especially useful for radio buttons and checkboxes — the hit area of such a control can be very small, so it is useful to make it as easy to activate as possible.
		- EXAMPLE:
			- ```
			  <form>
			    <p>
			      <input type="checkbox" id="taste_1" name="taste_cherry" value="cherry" />
			      <label for="taste_1">I like cherry</label>
			    </p>
			    <p>
			      <input type="checkbox" id="taste_2" name="taste_banana" value="banana" />
			      <label for="taste_2">I like banana</label>
			    </p>
			  </form>
			  ```
			- [form_fieldset_legend_Fruit_1719597045681_0 (Copy).html](../assets/form_fieldset_legend_Fruit_1719597045681_0_(Copy)_1719599039255_0.html)
			-
			-
- # [Common HTML structures used with forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#common_html_structures_used_with_forms)
	- it's common practice to wrap a label and its widget with a [`<li>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) element within a [`<ul>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul) or [`<ol>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) list.
		- Lists are recommended for structuring multiple checkboxes or radio buttons.
	- [`<p>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p) and [`<div>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) elements are also commonly used.
	- In addition to the  [[<fieldset>]] element, it's also common practice to use HTML titles (e.g. [h1](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements), [h2](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)) and sectioning (e.g. [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)) to structure complex forms.
	- ### [Active learning: building a form structure](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form#active_learning_building_a_form_structure)