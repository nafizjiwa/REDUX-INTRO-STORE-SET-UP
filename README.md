# REDUX-Intro

TO USE REDUX IN YOUR REACT APP and give your app access to the REDUX STATE</br>

## 1ST 
#### Import required files and libraries
    --index.js--
    import React from 'react';                                //React
    import ReactDOM from 'react-dom/client';                  //ReactDom
    import App from './App.js';                               //App component
    Import { Provider } from 'react-redux';                   //Redux Provider component
    import { store } from 'store.js';                         //Store

## 2ND
#### Wrap App component with Provider component </br>
#### This tells redux-react that we want the whole app to have access to the REDUX store, states and actions we created in the store file </br>

        <Provider> 
          <App />
        </Provider>

## 3RD 
In the Provider component pass in the store as a prop to Provider component

    --index.js--
    ReactDom.createRoot(document.getElementById('root')).render(
      <React.StrictMode>
        <Provider store={store}> //if store not passed into provide the app won't have access to store
          <App />
        </Provider>
      </React.StrictMode>
    ))

## 4TH
- Create a STORE --- In a file called store.js
- The STORE holds the App's state and the logic to update the state
- The STORE allows the Components to access state without passing it manually through props

 1st
    --store.js--
     import { configureStore } from '@reduxjs/toolkit'        --> Import function configureStore to setup store
     
2nd
    --store.js--
     import { configureStore } from '@reduxjs/toolkit' 
     
     const store = configureStore({ })                         --> Define constant store
    
3rd 
     --store.js--
     import { configureStore } from '@reduxjs/toolkit' 
     
     const store = configureStore({
         reducer: {                                           --> Define a reducer to manage all reducers
         todos: todoReducer,                                  --> Add a reducer to call
             },
         });       
         
     export default store;                                    --> Export the store to use in the Provider component app above
