# JavaScript-practice


## practice Time Part 3
##### Create a function that takes a single parameter, an array,
 and logs all the items of the array to the console.
 Call the function while passing in myCourses as an argument
```js
let myCourses = ["Learn CSS Animations", "UI Design Fundamentals", "Intro to Clean Code"]
function randerdarry(arry){
    
    for (let i=0; i<arry.length; i++){
        console.log(arry[i])
    }
}
randerdarry(myCourses)

```
 #### Save a value to localStorage
 Delete your code and refresh the page
 Fetch your value from localStorage and log it out

```js

localStorage.setItem("name","Jon Doe")//Delete this line
console.log(localStorage.getItem("name"))


```

#### Fetch the button from the DOM, store it in a variable
 Use addEventListener() to listen for button clicks
  Log Jane's score when the button is clicked (via data)
```js
let data = [
    {
        player: "Jane",
        score: 52
    }, 
    {
        player: "Mark",
        score: 41
    }
]
const janeBtn = document.getElementById("jane-btn")

janeBtn.addEventListener("click", function() {
    console.log(data[0].score)
})
```
  ### Challenge 
 The generateSentence(desc, arr) takes two parameterer: a description and an array.
 It should return a string based upon the description and array.

 Example 1: if you pass in "largest countries",and ["China", "India", "USA"],
 it should return the string: "The 3 largest countries are China, India, USA"

Example 2: If you pass in "best fruits" and ["Apples", "Bananas"], it should return:
"The 2 best fruits are Apples, Bananas"

 Use both a for loop and a template string to solve the challenge

 ```js
function generateSentence(desc, arr) {
    let baseString = `The ${arr.length} ${desc} are `
    for (let i = 0; i < arr.length; i++) {
        baseString += arr[i] + ","
    }
    return baseString
}

const sentence = generateSentence("highest mountains", ["Mount Everest", "K2"])
console.log(sentence)
-------------------------------------------------------------------------------------
================================remove comma after last arry iten =================
function generateSentence(desc, arr) {
    let baseString = `The ${arr.length} ${desc} are `
    const lastIndex = arr.length - 1
    for (let i = 0; i < arr.length; i++) {
        if (i === lastIndex) {
            baseString += arr[i]
        } else {
            baseString += arr[i] + ", "   
        }
    }
    return baseString
}

const sentence = generateSentence("highest mountains", ["Mount Everest", "K2"])
console.log(sentence)
```
  ### Challenge 
 Create a function that renders the three team images
 Use a for loop, template strings (``), plus equals (+=)
 .innerHTML to solve the challenge.
```js
   //In the container of HTML
const imgs = [
    "images/hip1.jpg",
    "images/hip2.jpg",
    "images/hip3.jpg"
]

const container = document.getElementById("container")

function renderImages() {
    for (let i = 0; i < imgs.length; i++) {
        container.innerHTML += `<img class="team-img" src="${imgs[i]}">`
    }
}

renderImages()
-------------------------------------------------------------------------------------
================================Render Dom Out of HTML Loop =================
const imgs = [
    "images/hip1.jpg",
    "images/hip2.jpg",
    "images/hip3.jpg"
]

const container = document.getElementById("container")

function renderImages() {
    let imgsDOM = ""
    for (let i = 0; i < imgs.length; i++) {
        imgsDOM += `<img alt="Employee in the company"  class="team-img" src="${imgs[i]}">`
    }
    container.innerHTML = imgsDOM
}

renderImages()
```

Challenge:
 Round the price in the button down to two decimal places.
 Don't know which method to use? Google it!
```js

const totalPrice = 420.69235632455
const btn = document.getElementById("purchase-btn")
btn.textContent = `Buy €${ totalPrice }`
-------------------------------------------------
const totalPrice = 420.69235632455
const btn = document.getElementById("purchase-btn")
btn.textContent = `Buy €${ totalPrice.toFixed(2) }`


```

 Challenge:
 The toFixed() method doesn't work anymore. Can you make it work?
Converted  string number into number by using Number ()
```js
const totalPrice = "420.69235632455"
const btn = document.getElementById("buy-btn")
btn.textContent = `Buy €${ Number(totalPrice).toFixed(2) }`
```
