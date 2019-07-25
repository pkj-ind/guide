---
title: Write a Counter with Redux
---
## Write a Counter with Redux

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/front-end-libraries/redux/write-a-counter-with-redux/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
const INCREMENT = 'INCREMENT'; // define a constant for increment action types
const DECREMENT = 'DECREMENT'; // define a constant for decrement action types

const counterReducer = (state=0,action)=>{
    if (action.type === INCREMENT)
    {
        return state +1;
    }
    else if (action.type === DECREMENT){
        return state -1;
    }
    return state;
}; // define the counter reducer which will increment or decrement the state based on the action it receives

const incAction = () => {
    return {type:INCREMENT} 
    
}; // define an action creator for incrementing

const decAction  = () => {
    return{
        type:DECREMENT
    }
    }; // define an action creator for decrementing

const store = Redux.createStore(counterReducer); // define the Redux store here, passing in your reducers
