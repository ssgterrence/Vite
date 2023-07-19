////////////////////////////////////
Example One

  <div class="grid">
    <div class="left"></div>
    <div class="right"></div>
  </div>
---------------------------------------------
.grid {
  display: grid;
  gap: 3px;
  height: 100vh;
  grid-template-columns: 48px auto;

`/_make the left column super narrow, and later increase its width on hover_/`

`/_ the right column takes up the rest of the remaining space by "auto"_/`

transition: 300ms; /_ because we do transition, so need it in the gridContainer _/

`/_ when the .left element is hovered over, the grid-template-columns property is modified to 30% auto, which changes the width of the left column. Without the transition property, the change would be instant and abrupt. _/`

}
.grid:has(.left:hover) {
`/_ if it is id, then use "#left" _/`
`/_ targeting .grid class element if it has a child element named as '.left', and apply 'hover'to it. _/`

grid-template-columns: 30% auto; `override the ".left"element when hoved`
}

.left {
background-color: crimson;
}
.right {
background-color: navajowhite;
border: 1rem solid rgb(0 0 0 / 10%);
}
/////////////////////////////////////////////////////////////
Expanding Panels.CSs+grid
-> % vs fr , where , has

  <div class="grid">
    <div class="left"></div>
    <div class="center"></div>
    <div class="right"></div>
  </div>

.grid {
display: grid;
height: 100vh;
grid-template-columns: repeat(3, 1fr);
transition: 500ms;
gap: 2px; `/* so it output gap is red. */`
background-color: crimson; ` /* the whole grid's background is red */`
}
:where(.left, .center, .right) {
`/* target element with these class name , and apply these CSS */`
background: navajowhite;
transition: 300ms; `/* any CSS property changes on the elements should have a transition duration of 300 milliseconds.  */`
}
:where(.left, .center, .right):hover {
background: crimson;
}

.grid:has(.left:hover) {
grid-template-columns: 2fr 0.5fr 0.5fr;
}
.grid:has(.center:hover) {
grid-template-columns: 0.5fr 2fr 0.5fr;
}
.grid:has(.right:hover) {
grid-template-columns: 0.5fr 0.5fr 2fr;
}
