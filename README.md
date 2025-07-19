# REDUX-Intro

TO USE REDUX IN YOUR REACT APP and give your app access to the REDUX STATE</br>

1ST 
    index.js
    import React from 'react';
    import ReactDOM from 'react-dom/client';
    import App from './App.js';
    Import { Provider } from 'react-redux';                  //Provider component
    import { store } from 'store.js';                        //Store

2ND
Wrap App component with Provider component to tell redux-react that we want the whole app to have access to the store and states and actions we created in the store file

3RD 
In the Provider pass in the store

index.js
ReactDom.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <Provider store={store}> //if store not passed into provide the app won't have access to store
      <App />
    </Provider>
  </React.StrictMode>
))
