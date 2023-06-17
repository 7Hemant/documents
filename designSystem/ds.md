# Creating own Design system

## using typescript and react ,storybook6

command

- website [link](tsdx.io/#quick.start)
- npx tsdx create mylib or we have another ways also

<b>create a basic custome button </b>

<pre> 
import React, { HTMLAttributes, ReactNode } from react

interface Props extends HTMLAttributes<HTMLButtonElement> {
/*provide a text for the  button  */
children:ReactNode;
variant:'primary' I 'secondary' ;
}

export const Button =({children,variant="primary" , ...props}:Props)=>{
return(
< button {...props}  style={{
     backgroundColor:variant === "primary"? "blue":"gray",
     color:"white" ,
     border:"none"
     borderRadius:100,
     padding :10,
     cursor:"pointer"
       }} >
{children}
 <  / button >)
}

</pre>

# start creating story for this button

<pre>
import React from "react";
import {Meta,Story} from "@storybook/react";
import {Button,Props} from "/location of the button";
import { action } from "@storybook/addon-action";
action
const meta:Meta ={
    title:'Button',
    component:Button,
    argTypes:{
        onClick:{action:'clicked'},
        children:{
            defaultValue:"default text"
        }
    }
}
export default meta ;

<b>const Template:Story< Props >=( args ) => < Button {...args} >  </b>


/* export const default =()=>< Button variant="primary">CLick me < / Button>
 export const  secondary =() => < Button variant="secondary">this is scondary button < / Button> */

export const ButtonName = template.Bind({});
export const Secondary =template.bind({});
Secondary.args={
    variant:"secondary",
    children:"I am secondary"
    onClick :action("secondary click)
}


</pre>
