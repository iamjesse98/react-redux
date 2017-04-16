import { createStore } from 'redux'
import React, { Component } from 'react'
import './App.css'

const reducer = (state, action) => {
	switch(action.type){
		case "ADD":
			state += action.payload
			break
		case "SUBTRACT":
			state -= action.payload
			break
		default:
			//console.log(`not a valid option`)
			state = 0
	}
	return state
}

const store = createStore(reducer, 1)

store.subscribe(() => {
	console.log(`Store Updated: ${store.getState()}`)
})

store.dispatch({
	type: "ADD",
	payload: 10
})

store.dispatch({
	type: "ADD",
	payload: 14
})

store.dispatch({
	type: "SUBTRACT",
	payload: 14
})

store.dispatch({
	type: "MULTIPLY",
	payload: 14
})

store.dispatch({
	type: "ADD",
	payload: 12
})

class App extends Component {
  render = ()=><div>
                <h1>{store.getState()}</h1>
               </div>
}

export default App
