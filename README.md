# modal_with_vanila_js


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
