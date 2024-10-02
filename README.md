 <html>
 <body style="background-color:#feefc3;">
 
 <form id="myForm">
   <textarea id="myTextBox" name="myTextBox" rows="10" cols="150" width="100%"></textarea>
   <br>
   <input type="submit" value="Submit">
 </form>
 
 <p id="myParagraph">Simple MS Edge Read Aloud text tool.<BR>This text will be replaced once you submit.<BR> Then you can use the read aloud feature.<BR> Use Ctrl+Shift+U, or right click "Read Aloud" to start it. </p>
 
 <script>
 document.getElementById('myForm').addEventListener('submit', function(event) {
   event.preventDefault(); // Prevent the form from submitting
   var textBoxValue = document.getElementById('myTextBox').value;
   
   // Split the text into paragraphs based on line breaks
   var paragraphs = textBoxValue.split('\n');
   var formattedText = paragraphs.map(function(paragraph) {
     return '<p>' + paragraph + '</p>';
   }).join('');
   
   document.getElementById('myParagraph').innerHTML = formattedText;
 });
 </script>
 
 </body>
