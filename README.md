# modal_with_vanila_js
# Languages
```
1.HTML
2.CSS
2.SASS
3.JavaScript
```

## HTML Code Here
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modal with JS</title>
    <!-- added style.css -->
    <link rel="stylesheet" href="./dist/css/style.min.css">
</head>
<body>

    <!-- showcase section  -->
    <section class="showcase_container">
     <div class="all_one">
        <h1>Click this button and see the modal.</h1>
        <button class="show_modal">Click</button>
     </div>
    </section>

    <!-- modal section  -->
    <div class="modal_container">
        <div class="modal_body">
       Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut, consectetur. Asperiores alias cumque unde similique nisi atque quaerat sint! Similique incidunt facilis esse minus minima aliquid dignissimos, nemo velit impedit quod debitis cumque sint. Mollitia autem enim ullam ipsam fuga veritatis vel incidunt aperiam natus at nulla sapiente iusto quibusdam nostrum, repellendus rem quis quo et voluptas modi laudantium voluptatem sit! Corporis est dicta non neque culpa sunt saepe pariatur beatae incidunt doloribus eveniet accusantium deleniti ut repellendus et, officia id error, eum magni iure harum ab perferendis cumque facere! Vitae quaerat ab quis facere autem incidunt voluptas eligendi accusantium.
            <button class="close_modal">X</button>
        </div>
    </div>

<!-- added custom js file -->
<script src="./index.js"></script>
</body>
</html>

```

## SASS Code Here
```css

// for showcase
.showcase_container{
   background-image:linear-gradient(#136a8a,#267871);
   display: flex;
   justify-content: center;
   margin: 0;
   padding:260px;
   transition: .5s;
.all_one{
// for heading
    h1{
        text-transform: uppercase;
        font-size: 35px;
        margin: 0;
        font-weight: 700;
        color: #fff;
        padding-bottom: 10px;
    }
    // for show modal button
    .show_modal{
        background-color: orange;
        width: 200px;
        border: none;
        padding: 10px;
        color: #fff;
        font-size: 20px;
        letter-spacing: 4px;

    }
}
}

// for modal parent
.modal_container{


// for modal body
.modal_body{
background: #fff;
width: 800px;
padding: 30px;
font-size:20px;

position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
animation: .3s Drop;
display: none;

// for close_modal button
.close_modal{
    position: absolute;
    right: 20px;
    top: 5px;
    background: red;
    color: #fff;
    border: none;
    padding: 10px;
    border-radius: 10px;
}

}
}

// for animation
@keyframes Drop{
    0%{
        top: -100px;
    }
    100%{
        top: 50% ;
    }
}

// end here

```

```javascript 
var showModal = document.querySelector('.show_modal') ;
var modal = document.querySelector('.modal_body');
var close_modal = document.querySelector('.close_modal')
var WholeSection = document.querySelector('.showcase_container')


// after click showModal button
showModal.addEventListener('click', afterClickbtn) ;
function afterClickbtn(){
    modal.style.display = 'block' ;
    WholeSection.style.filter = 'blur(6px)'
}

// after click close_modal button
close_modal.addEventListener('click', afterClickCloseBtn);
function afterClickCloseBtn(){
    modal.style.display = 'none' ;
    WholeSection.style.filter = 'blur(0px)'
}

// after click WholeSection area
WholeSection.addEventListener('click', clickSpace);
function clickSpace(e){
    if(e.target.className == 'showcase_container'){
        modal.style.display = 'none' ;
    WholeSection.style.filter = 'blur(0px)'
    }
}

// end here

```
