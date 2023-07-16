<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- linking css file -->
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body{
    
font-family: 'Amatic SC', cursive;
font-family: 'Andika', sans-serif;
font-family: 'Fira Sans', sans-serif;
font-family: 'IBM Plex Mono', monospace;
font-family: 'Poppins', sans-serif;
display: flex;
align-items: center;
justify-content: center;
flex-direction: column;
background-color: #79793b52;
}

h1{
    font-weight: 700;
    font-style: italic;
}
header{
    margin-bottom: 20px;
}

.mainSection{
    display: flex;
    /* align-items: center; */
    justify-content: space-between;
    gap: 250px;
}

.lhs{

    padding: 70px ;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 100px;

}

.first_lhs{
    border: 2px solid #000000;
    padding: 51px;   
    border: 5px ridge #228b22;
    box-shadow:  0 0 0 10px #000000;
}

.second_lhs{
    border: 2px solid #000000;
    padding: 30px;
    border: 4px ridge #ff0000;
    box-shadow:  0 0 0 10px #000000;
}

label , input{
    font-weight: 500;
    margin-bottom: 15px;
}

input{
    padding: 3px;
    border-radius: 5px;
    border: 2px ridge #0000ffac;
}

button{
    padding: 7px;
    font-weight: 600;
    color: #228b22;
    cursor: pointer;
}

.btn1{
    border: 1px ridge #228b22;
    border-radius: 5px;
 
}

.btn1:hover{
    border: 1px ridge #228b2286;
    color: #228b2286;
}

.btn2{
    border: 1px ridge #ff0000;
    border-radius: 5px;
}

.rhs{

    display: flex;
    align-items: center;
    justify-content: center;
    gap: 100px;
    flex-direction: column;
}

.rhs1{
    
    padding: 50px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 100px;
    margin-bottom: 50px;
}

.footerSection{
   
    padding: 50px;
}

.pistol{
    margin-bottom: 15px;
}

.velly1{
    margin-top: 15px;
    font-size: xx-large;
    color: #228b22;
}

.velly2{
    margin-top: 15px;
    font-size: xx-large;
    color: #ff0000;
}

.velly3{
    margin-top: 15px;
    font-size: xx-large;
}

.footerSection{
    display: none;
    font-weight: 700;
    color: #000000;
    background-color: #ff0000;
    padding: 10px 20px;
}

    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&family=Andika:ital,wght@1,700&family=Fira+Sans:wght@900&family=IBM+Plex+Mono:wght@500&family=Poppins&display=swap" rel="stylesheet">

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

<body>

    <header>
        <h1>BUDGET APP</h1>
    </header>

                  <!-- main section -->
    <main class="mainSection">

                <!-- left hand side -->
        <div class="lhs">

                  <!-- siblings 1 -->
            <div class="first_lhs">

                <label for="">Please Enter Your Budget</label> <br>
                <input type="number" id="yourBudget" class="qwerty" value=""> <br>
                <button class="btn1" id="btn">Calculate</button>

            </div>

                  <!-- siblings 2 -->
            <div class="second_lhs">
                <label for="">Please Enter Your Expense</label> <br>
                <input type="text" id="expense" class="expenseText" value=""> <br>
                <label for="">Please Enter Expense Amount</label> <br>
                <input type="number" id="amount" class="expenseAmount" value=""> <br>
                <button class="btn2" id="btn1">Add Expense</button>
            </div>
        </div>

        <!-- right hand side -->
        <div class="rhs">

            <div class="rhs1">

                <div class="first_rhs">
                    <h2 class="pistol">BUDGET</h2> <br>
                    <i class="fa-sharp fa-solid fa-credit-card fa-bounce fa-4x" style="color: #1eb464;"></i>
                    <h2 class="velly1">$ 0</h2>
                </div>
    
                <div class="first_rhs">
                    <h2 class="pistol">EXPENSE</h2> <br>
                    <i class="fa-sharp fa-solid fa-wallet fa-bounce fa-4x" style="color: #1818bb;"></i>
                    <h2 class="velly2">$ 0</h2>
                </div>
    
                <div class="first_rhs">
                    <h2 class="pistol">BALANCE</h2> <br>
                    <i  class="fa-solid fa-dollar-sign fa-bounce fa-4x" style="color: #e90e0e;" ></i>
                    <h2 class="velly3">$ 0</h2>
                    
                </div>

            </div>

            <div class="footerSection">
                
              </div>

            </div>

         
    </main>


const btn1 = document.getElementById("btn")
const btn2 = document.getElementById("btn1")
let resultBudget 
let resultExpense 
let result

btn1.addEventListener("click" , () => {
    let budget = document.getElementById("yourBudget").value
    let sol = document.querySelector(".velly1")
    console.log(budget);
    if(budget < 0  || budget === ""){
        sol.innerHTML =  "Invalid Budget"
    }
    else{
        sol.innerHTML = '$' + budget
    }
    resultBudget = budget
    // console.log("result" , resultBudget);

})


btn2.addEventListener("click" , () => {
    const nameOfExpense = document.getElementById("expense").value
    let amount = document.getElementById("amount").value
    let val = document.querySelector(".velly2")
    const balance = document.querySelector(".velly3")
    const footerSection = document.querySelector(".footerSection")

    console.log(amount);
    console.log(nameOfExpense);

    if(amount < 0 || nameOfExpense === ""){
        val.innerHTML = 'Invalid Expense'
    }
    else{
        val.innerHTML = '$' + amount
    }
    resultExpense = amount
    // console.log("result" , resultExpense);

    result = resultBudget - resultExpense
    console.log( result);
    balance.innerHTML = "$" + result

    footerSection.innerHTML = `Your Budget is ${resultBudget} , ${nameOfExpense} Expense is ${resultExpense} and Total Balance left ${result}`
    footerSection.style.display = "block"
})
</body>
</html>
