# Redux createSlice

## What is Redux?

Redux is a predictable state container for JavaScript apps.

## What is createSlice?

createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

## How to use createSlice?

```js
import { createSlice } from '@reduxjs/toolkit'

const initialState = { value: 0 }

const counterSlice = createSlice({
  name: 'counter',
  initialState,
  reducers: {
    increment: state => {
      // Redux Toolkit allows us to write "mutating" logic in reducers. It
      // doesn't actually mutate the state because it uses the immer library,
      // which detects changes to a "draft state" and produces a brand new
      // immutable state based off those changes
      state.value += 1
    },
    decrement: state => {
      state.value -= 1
    },
    incrementByAmount: (state, action) => {
      state.value += action.payload
    }
  }
})

export const { increment, decrement, incrementByAmount } = counterSlice.actions
export default counterSlice.reducer
```

## What is the difference between createSlice and createReducer?

createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

createReducer is a function that accepts an initial state, an object full of reducer functions, and returns a reducer function.

## What is the difference between createSlice and createAsyncThunk?

createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

createAsyncThunk is a function that accepts an action type string, a payload creator function, and an options object, and returns a thunk action creator function.

## What is the difference between createSlice and configureStore?

createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

configureStore is a function that accepts an object full of reducer functions, and an optional options object, and returns a Redux store.

## What is the difference between createSlice and combineReducers?

createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

combineReducers is a function that accepts an object full of reducer functions, and returns a reducer function.
