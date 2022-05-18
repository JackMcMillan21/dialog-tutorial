# Workings with modals

A modal is a dialog box usually a pop-up that is showed on top of whatever page you are on. An example that we will work
threw will be making a modal using the ```<dialog>``` tag. 

## Working with the ```<dialog>``` tag

The HTML tag ```<dialog>``` is used to most often make dialauges within a webpage.
Using Javascript you can use funtions and methods to open and close the dialog being used. The dialog can also be
open or closed using events. 

## Dialogs In HTML

Below you will find an example of a modal and how it is created

```html
<div class="parent-container">

    <button id="button">Open Modal</button>

    <dialog id="dialog-container">
        <div class="container">
            <div class="center-container">
                <div class="modal">
                    <h1>Opened Modal</h1>
                    <button id="button2">Close Modal</button>
                </div>
            </div>
        </div>
    </dialog>
</div>
```

Next is the styling for our modal. We want to make sure to center it, and include a button to close it. When the modal opens its important to reduce the brightness of the content behing the modal to create focus on the modal content. We can do that by making the background color of the parent container black with medium opacity. We

```css

.parent-container{
    height:100vh;
    width:100%;
    z-index:0;
}

.parent-container {
	background: rgba(0 0 0 / 0);
}

dialog{
    height: 450px;
    width: 450px;
    border-radius: 10px;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.center-container{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 450px;
}

.modal{
    display: flex;
    align-items: space;
    justify-content: center;
    flex-direction: column;
    height: 175px;
}

button{
    font-size: 25px;
    color: #fff;
    font-weight: 400;
    text-decoration: none;
    letter-spacing: 0.2px;
    text-transform: none;
    cursor: pointer;
    background-color:#ff007f;
    padding: 7px 12px;
    border-radius: 25px;
}

#button{
    margin-top: calc(100vh - 50%);

}


```

The last step to a modal is the JavaScript, below we are creating the functions of opening and closeing the modal using the button

```javascript

let button1 = document.getElementById("button");
let button2 = document.getElementById('button2')

	button1.addEventListener("click", function () {
		document.querySelector("#dialog-container").showModal();
	});
    
	button2.addEventListener("click", function () {
		document.querySelector("#dialog-container").close();
	});
    

```

## Take aways 

Modals are extremely important amongst all websites because there is going to be some sort of content that needs to be highlighted. Using dialogs can make this very easy. 
Therefor I would consider using them.



## References

- [Section IO](https://www.section.io/engineering-education/creating-a-modal-dialog-with-tailwind-css/)
- [W3 schools](https://www.w3schools.com/w3css/w3css_modal.asp#:~:text=A%20modal%20is%20a%20dialog,%C3%97)

