# SAP-BSP-OCR-Tesseract-Javascript
SAP BSP : Simple OCR Tesseract Javascript

SAP Business Server Pages : Simple Optical Character Recognition (OCR) and save to Z table with Tesseract Javascript

1. Create ZTESERACT_JOHN (SAP BSP Program)
2. Create 2 page html
   a. ImageInput.htm
   b. proses.htm
3. Import file image to folder MIME object 
4. Run program
URL : 
Page -> Properties -> URL
example:
http://sapserver.mydomain.com:port/sap/bc/bsp/sap/zbspapp/page.htm


Page ImageInput.htm
Layout (see ImageInput.html)

Event Handler (OnInputProcessing)
* event handler for checking and processing user input and
* for defining navigation

navigation->set_parameter( 'var1' ).

Page Attributes
var1 TYPE STRING

Page proses.htm
Layout (see proses.html)

EventHandler (OnInitialization)
* event handler for data retrieval

data : lv_var1 TYPE STRING.

data : ls_image TYPE zimage_john.
data : lt_image TYPE STANDARD TABLE OF zimage_john.
data : row TYPE i.

lv_var1 = request->get_form_field( 'var1' ).

if lv_var1 IS NOT INITIAL.

Reference:
http://progur.com/2016/10/how-to-use-tesseract-for-ocr-javascript.html

https://stackoverflow.com/questions/18174372/pass-div-element-into-javascript-

function

https://stackoverflow.com/questions/7764154/pass-a-javascript-variable-value-into-

input-type-hidden-value

https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_hidden_value

http://www.rjruss.info/2011/06/sap-bsp-for-lotus-notes-widgets-display.html
