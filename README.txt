Note: The directional properties(top/right/bottom/left) doesn't act unless we provide the position and vice-versa
eg:
span{
   top:40px; //doesnt do anything until we provide position
}
span{
   position:______; //element don't move from its position but it leaves gap/space or becomes                       //z-index "static/relative->doesn't do anything; absolute/fixed->span                     // element is taken out of normal flow(compact) and positioned on top
                    //(z-index +ve)"
}

-----------------------------------------------------------------------------------------------
static position
1.it is the default position of all html elements (although they are not styled)
2.the directional properties i.e. top/right/bottom/left is always "auto"

-----------------------------------------------------------------------------------------------

relative position
1.the "element" moves from the position where it should be to where we provide(top/left/right/bottom)
eg:
span{
  position:relative;  //the span is the standard line
  top: 40px;  //it comes 40px down from the normal
  left:30px;  //it comes 30px left
}
2.the natural flow  is left unaltered i.e. a gap/space is left.
3.the element sit on top of things like z-index.  

-----------------------------------------------------------------------------------------------

Fixed position
1.this position take out the "element" from its normal flow leaving no gap/space
2.it position itself wrt to the browser window (not the DOM or the parent)
3.it stretches out if given a "left" and "right" property
4.the position is always fixed whether we scroll or not
5.it is use for fixed header on top where we style the <div> tag with top:0,left:0,right:0,height:50px

-----------------------------------------------------------------------------------------------

absolute position
1.this positon take out the "element" and all other elements compact leaving no gap/space.
2.the "element" flow on top of the other compact element at its own position i.e the "element" is ripped outside of the DOM and the rest of the materials flow as if the "element" was not there.
3.Declaring directional properties(i.e. top,left,right,bottom) on absolute position "element" then it will be position relative to the nearest parent(only when parent has a property position:relative/absolute/fixed).If the parent has no property "position:relative/absolute/fixed" then it will be positioned  relative to DOM.
4.If we declare both ("left" and "right") or ("top" and "bottom") then it will be stretched.
If declare all directional properties like "top,bottom,left,right" then it will become a square/rectangle (i.e. stretched like a rectangle/square).

