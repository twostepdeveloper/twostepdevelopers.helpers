# twostepdevelopers.helpers
This is javascript plugins. for validate forms.
follow this instructions...

1. firt drag and drop css ,and js files in head tag.

follow all input type text box and selector how i am validating form.


<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title>validation</title>
    <link href="vendors/bootstrap/dist/css/bootstrap.css" rel="stylesheet" />
     <link href="/helpers/twostepdevelopers.helpers.css" rel="stylesheet" />
<script src="vendors/jquery/dist/jquery.js"></script>
<script src="/helpers/twostepdevelopers.helpers.css/twostepdevelopers.helpers.js"></script>

   
</head>

<body class="container">
    <br />
    <br />
    <form id="form1" runat="server">
       
        <label for="txt">Name</label>
        <input type="text" id="txt" class="required onlyNumber"  data-required="name is required." data-numeric-msg-for="only number is allowed" />
        <br />
         <label for="txt2">Email</label>
        <input type="text" id="txt2" class="required tsd-validate-email" data-required="email is required."  data-email-required="Please enter valid email address i.e abx@gmail.com" />
        <br />
          <br />
         <label for="select2">state</label>
        <select id="select2" class="required" data-required="state is required..">
            <option value="-1">---select---</option>
          <option >delhi</option>
              <option >Bihar</option>
             <option >UP</option>
        </select>
        <br />
        <button onclick="return validateForm()" class="btn btn-primary btn-lg">Submit</button>
    </form>
    <script>
        function validateForm() {
            twostepdevelopers.validateForm();
            return false;
        }
    </script>
</body>
   
</html>
