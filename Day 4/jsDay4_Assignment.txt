document.querySelector(".items");


let item = document.querySelector(".item1");
item.textContent="Good Morning";


let item_2 = document.querySelector(".item2");
item_2.innerHTML="<h1>Hello</h1>";

let button_1 = document.querySelector(".btn1");
button_1.style.background = "blue";



let nameInput = document.querySelector("#name");
nameInput.addEventListener("input",e =>
                           {
    document.querySelector(".container").append(nameInput.value);
});

let emailInput = document.querySelector("#email");
emailInput.addEventListener("input",e =>
                           {
    document.querySelector(".container").append(emailInput.value);
});

let mobInput = document.querySelector("#mob");
mobInput.addEventListener("input",e =>
                           {
    document.querySelector(".container").append(mobInput.value);
});

let clgInput = document.querySelector("#clg");
clgInput.addEventListener("input",e =>
                           {
    document.querySelector(".container").append(clgInput.value);
});


const myForm = document.querySelector('#my-form');
const name1Input = document.querySelector('#name');
const email1Input = document.querySelector('#email');
const mob1Input = document.querySelector('#mob');
const clg1Input = document.querySelector('#clg');
const msg = document.querySelector('.msg');
const userList = document.querySelector('#users');

// Listen for form submit
function onSubmit(e) {
  e.preventDefault();
}
//console.log(name1Input);
console.log(name1Input.value);
console.log(email1Input.value);
console.log(mob1Input.value);
console.log(clgInput.value);



// addEventListener to form on console via Message on <div> selection
let msg1 = document.querySelector(".msg");




  // As & when users get registered add into LIST
let userList1 = document.querySelector("#users");


  if(nameInput.value === '' || emailInput.value === ''|| mobInput.value ==='' || clgInput.value ==='')
  {
    msg1.classList.add('error');
    msg1.innerHTML = 'Please enter all fields';
    setTimeout(() => msg.remove(), 3000);
  }
  else
  {
    // Create new list item with user
    let li = document.createElement('li');

    // Add text node with input values
    li.appendChild(document.createTextNode(`${nameInput.value}: ${emailInput.value}: ${mobInput.value}: ${clgInput.value}`));

    // Append to ul
    userList1.appendChild(li);
    // Clear fields
    nameInput.value = '';
    emailInput.value = '';
mobInput.value = '';
clgInput.value = '';

  }
