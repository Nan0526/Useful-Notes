# useCallback
It's useful when **passing callbacks** to children components.     
当parent component render的时候，每个callback function都会重新被create一遍。而callback function作为child component的props之一，因为其改变， 也会导致child component从新render一遍。    
With useCallback hook, callback function只会在one of dependecies改变的时候重新create.从而避免child component被render的次数。    
### What?
useCallback is a hook that will return a memorized version of the callback function that only changes if one of the dependencies has changed.    
### Why?
It's useful when passing callbacks to optimized child components that rely on reference equality to prevent unnecessary renders.    
### Code example
`useCallback` takes in 2 params, one is the callback function, another one is the dependency array.     
```
import React from "react";
import { useState, useCallback } from "react";
import { Count } from "./Count";
import { Title } from "./Title";
import { Button } from "./Button";
export default function CallBackParent() {
  const [age, setAge] = useState(25);
  const [salary, setSalary] = useState(4000);

  const incrementAge = useCallback(() => {
    setAge(age + 1);
  }, [age]);

  const incrementSalary = useCallback(() => {
    setSalary(salary + 1000);
  }, [salary]);

  return (
    <div>
      <Title />
      <Count name="Age" count={age} />
      <Button handleClick={incrementAge} children="Increment Age" />
      <Count name="Salary" count={salary} />
      <Button handleClick={incrementSalary} children="Increment Salary" />
    </div>
  );
```
