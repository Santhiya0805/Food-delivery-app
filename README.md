# Food-delivery-app
<!DOCTYPE html>
<html>
  <head>
    <style>
      tr{
        background-color: blue;
        color:white;
        text-align:center;
      }
      dt{
        font-weight:bold;
        background-color:pink;
      }
    </style>
    <script>
      function placeorder(){
        document.getElementById("ordersummary").style.display="block";
       
        uname=document.getElementById("txtname");
        mobile=document.getElementById("txtmobile");
        burger=document.getElementById("optburger");
        roller=document.getElementById("optroller");
        fries=document.getElementById("optfries");
        nuggets=document.getElementById("optnuggets");
       
        var mcost=0;
        var acost=0;
        var mname=" ";
        var aname=" ";
        if(burger.checked){
          mcost=120;
          mname=burger.value;
        }
        if(roller.checked){
          mcost=100;
          mname=roller.value;
        }
        if(fries.checked)
          {
            acost=50;
            mcost+=acost;
            aname+=fries.value+"<br>";
          }
        if(nuggets.checked)
          {
            acost=80;
            mcost+=acost;
            aname+=nuggets.value+"<br>";
          }
        document.getElementById("lblname").innerHTML=uname.value;
       document.getElementById("lblmobile").innerHTML=mobile.value;
        document.getElementById("lblmeal").innerHTML=mname;
         document.getElementById("lbladon").innerHTML=aname;
         document.getElementById("lblamount").innerHTML=mcost;
       
      }
     
    </script>
   
  </head>
  <body>
    <div><font size="6">
      <table width="800px" border="2" cellspacing="4" align="center" id="orderform">
        <tr>
          <td colspan="2">
            <img src="https://assets.simpleviewinc.com/simpleview/image/upload/c_fill,h_560,q_75,w_1680/v1/clients/phoenix/thai_food_cover_image_add1e248-c363-45c2-bc78-54c5811fcbf8.jpg" width=750 height=150>
          </td>
        </tr>
        <tr>
          <td colspan="2">CUSTOMER DETAILS</td>
        </tr>
        <tr>
          <td>Customer Name</td>
          <td><input type="text" id="txtname"></td>
         </tr>
        <tr>
          <td>Mobile number</td>
          <td><input type="number" id="txtmobile"></td>
        </tr>
        <tr>
          <td colspan="2">Select a MEAL</td>
        </tr>
        <tr>
          <td colspan="2">
            <img src="https://images.indulgexpress.com/uploads/user/imagelibrary/2021/2/17/original/1mae-mu-I7A_pHLcQK8-unsplash_revised.jpg" width=100 height=100><br>
            <input type="radio" name="meal" id="optburger" value="Burger">Burger(&#8377;120)
          </td>
        </tr>
          <tr>
          <td colspan="2">
            <img src="https://im.whatshot.in/img/2019/Jan/shutterstock-304847123-cropped-1546929010.jpg" width=100 height=100 ><br>
            <input type="radio" name="meal" id="optroller" value="Roller">Roller(&#8377;100)
          </td>
        </tr>
        <tr>
          <td colspan="2">Select Ad-ons</td>
        </tr>
        <tr>
          <td colspan="2">
            <input type="checkbox" id="optfries" value="largefries">Large fries(&#8377;50)
            <input type="checkbox" id="optnuggets" value="nuggets">Nuggets(&#8377;80)
          </td>
        </tr>
        <tr>
          <td colspan="2">
            <input type="button" value="Proceed" onclick="placeorder()">
          </td>
         
        </tr>
      </table>
      <br>
      <dl id="ordersummary" style="display:none";>
        <h2>Order Summary</h2>
        <dt>Customer Name: </dt>
        <dd id="lblname"></dd>
        <dt>Mobile: </dt>
        <dd id="lblmobile"></dd>
        <dt>Meal: </dt>
        <dd id="lblmeal"></dd>
        <dt>Ad-ons: </dt>
        <dd id="lbladon"></dd>
        <dt>Total bill amount: </dt>
        <dd id="lblamount"></dd>
       
        <br>
        <input type="button" value="Print Bill" onclick="window.print()">
       
      </dl>
     
    </font></div>
  </body>
 
 
</html>
