# Prototype Inheritance

All JavaScript objects have a **proto** property with the exception of objects created with **Object.create(null)**, that is a reference to another object, which is called the object's "prototype".

When a property is accessed on an object and if the property is not found on that object, the JavaScript engine looks at the object's **proto**, and the **proto**'s **proto** and so on, until it finds the property defined on one of the **proto**s or until it reaches the end of the prototype chain. This behavior simulates classical inheritance, but it is really more of delegation than inheritance.

https://davidwalsh.name/javascript-objects
