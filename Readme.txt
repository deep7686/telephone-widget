International Telephone Number Widget
Author: Deepak Sharma
Reviewer1: Pushpendra
Reviewer2: Anurag Arya
Company: I-Cube Systems Private Limited

Its a simple javascript & HTML implementation of international telephone number widget.

Benifits:
- Easy to plug into your code
- Works well on iphone, ipad and android phones
- Very ligt weight
- CSS sprites used in rendering the country flags - so there is no negetive impact on page load performance.

Installation & Usage:

- Download the code from ------- and keep the css files in your base css folder and js files in your base js folder (in the root directory of your project)
-index.html has the sample code to implement the widget. You can simply embed the code in index.html to your page. 
OR Follow the following steps:

Step 1 - Include the required JS & CSS:

<link rel="stylesheet" type="text/css" href="css/dd.css" />
<link rel="stylesheet" type="text/css" href="css/flags.css" />
<script src="js/jquery-1.8.2.min.js"></script>
<script src="js/jquery.dd.js"></script>
<script src="js/jquerymaskedinput.js"></script>

Step 2 - Rendering the countries dropdown: The country dropdown is rendered as select options and if you use the code in the demo.html as is then your telephone widget would work for all the countries. If you want to populate the list of countries from database then you can simply render the options in a loop, instead of hard-coding the options.
<select name="countries" id="countries" style="width:80px;">
	<option value='+93' data-image="images/blank.gif" data-format="9999999999" data-imagecss="flag af" data-title="Afghanistan">AF</option>
	.
	.
	<option value='pl' data-image="images/blank.gif" data-format="(99)999.99.99" data-imagecss="flag pl" data-title="Poland">PL</option>
	.
	.
	<option value='+1' data-image="images/blank.gif" data-format="999-999-9999" data-imagecss="flag us" data-title="United States"  selected="selected">US</option>
	.
	.
</select>

Step 3 - Rendering the phone number text box
<input type="hidden" name="country-code" id="country-code">
<input name="phone_number" class="text-box" type="text" id="phone_number"  align="top" />

Step 4 - Final nail in the coffin
<script>
$(document).ready(function() {
	$("#countries").icsCountry();
	$("#phone_number").mask("999-999-9999");
})

</script>
