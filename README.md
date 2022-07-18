# dish-menu-with-printbill
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        #dv
        {
            background-color: aqua;
            width: 400px;
            margin-top: 20px;
            padding-top: 20px;
            padding-left: 40px;
            padding-bottom: 20px;

        }
        #tdv
        {
            background-color: yellow;
            width: 420px;
            text-align: center;
            padding-top: 20px;
            padding-left: 20px;
        }
        table, th, td {
            border: 1px solid black;
        }
    </style>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="dv">
        Please Enter Your Name: <input type="text" id="name"> <br><br>
        <h3>Please select your order!</h3>
        Non-Veg Pizza(S) &nbsp; 300 &nbsp;<button onclick="fun1()" >+</button><br><br>
        Non-Veg Pizza(M) 450 <button onclick="fun2()">+</button><br><br>
        NOn-Veg Pizza(L) 600 <button onclick="fun3()">+</button><br><br>
        Veg Pizza(S) &nbsp;&nbsp;&nbsp; &nbsp; &nbsp; 280 <button onclick="fun4()">+</button><br><br>
        Veg Pizza(M)&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;420 <button onclick="fun5()">+</button><br><br>
        Veg Pizza(L)&nbsp;&nbsp;&nbsp; &nbsp; &nbsp; 550 <button onclick="fun6()">+</button><br><br>
        Burger &nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; 150 <button onclick="fun7()">+</button><br><br>
    </div>
    <h1 id="val"></h1>
    <div id="tdv">

        <table id="mtable">
            <thead>
                <th>Customer Name</th>
                <th>Dishes Ordered</th>
                <th id="prc">Price</th>
            </thead>
            <tbody id="bdy">
                
            </tbody>
        </table> <br><br>
        <button onclick="funbill()">Print Bill</button>
        <button onclick="print()">Print</button>
    </div>

        <script>
            function fun1()
            {
                var name1=document.getElementById("name")
                var dish1="Non-Veg Pizza(S)";
                var price1=300
                var x1=document.getElementById("bdy");
                x1.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish1+"</td><td>"+price1+"</td></tr>"

            }
            function fun2()
            {
                var name1=document.getElementById("name")
                var dish2="Non-Veg Pizza(M)"
                var price2=450
                var x2=document.getElementById("bdy");
                x2.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish2+"</td><td>"+price2+"</td></tb>"
            }

            function fun3()
            {
                var name1=document.getElementById("name")
                var dish3="Non-Veg Pizza(L)"
                var price3=600
                var x3=document.getElementById("bdy");
                x3.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish3+"</td><td>"+price3+"</td></tb>"
            }
            function fun4()
            {
                var name1=document.getElementById("name")
                var dish4="Veg Pizza(S)"
                var price4=280
                var x4=document.getElementById("bdy");
                x4.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish4+"</td><td>"+price4+"</td></tb>"
            }
            function fun5()
            {
                
                var name1=document.getElementById("name")
                var dish5="Veg Pizza(M)"
                var price5=450
                var x5=document.getElementById("bdy");
                x5.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish5+"</td><td>"+price5+"</td></tb>"
            }
            function fun6()
            {
                var name1=document.getElementById("name")
                var dish6="Veg Pizza(L)"
                var price6=550
                var x6=document.getElementById("bdy");
                x6.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish6+"</td><td>"+price6+"</td></tb>"
            }
            function fun7()
            {
                var name1=document.getElementById("name")
                var dish7="Burger"
                var price7=150
                var x7=document.getElementById("bdy");
                x7.innerHTML+="<tr><td>"+name1.value+"</td><td>"+dish7+"</td><td>"+price7+"</td></tb>"
            }

            function funbill()
            {
                var bill1=document.getElementById("mtable");
              
                sumVal=0;
                
                for(var i=1; i<bill1.rows.length; i++)
                {
                    console.log(bill1.rows[i].cells[2].innerHTML);
                    //sumVal=sumVal+bill1.rows[i].cells[2].innerHTML;
                    sumVal=sumVal +parseInt(bill1.rows[i].cells[2].innerHTML);
                    //console.log(bill1[2].parseInt(cellIndex[i]).innerHTML)

                }
                 document.getElementById("val").innerHTML="SubTotal =" +sumVal;
                console.log(sumVal);
            }


        </script>

           
</body>
</html>
