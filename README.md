# REDUX-Intro

TO USE REDUX IN YOUR REACT APP and give your app access to the REDUX STATE</br>

## 1ST 
#### Import required files and libraries
    --index.js--
    import React from 'react';                                //React
    import ReactDOM from 'react-dom/client';                  //ReactDom
    import App from './App.js';                               //App component
    Import { Provider } from 'react-redux';                   //Provider component
    import { store } from 'store.js';                         //Store

## 2ND
#### Wrap App component with Provider component </br>
#### This tells redux-react that we want the whole app to have access to the store, states and actions we created in the store file </br>

## 3RD 
In the Provider component pass in the store

    --index.js--
    ReactDom.createRoot(document.getElementById('root')).render(
      <React.StrictMode>
        <Provider store={store}> //if store not passed into provide the app won't have access to store
          <App />
        </Provider>
      </React.StrictMode>
    ))
