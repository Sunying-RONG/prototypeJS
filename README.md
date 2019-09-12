# prototypeJS
var a = {a: 1}; // a ---> Object.prototype ---> null
var b = Object.create(a); // b ---> a ---> Object.prototype ---> null
console.log(b.a); // 1 (inherited)
// b = {}; b is empty, inherit from it's prototype a.
// b doesn't have own property/variable, inherite from a. 
// b doesn't have prototype property, a is b's prototype.


function Graph() {
  this.vertices = [];
  this.edges = [];
}
Graph.prototype = {
  addVertex: function(v) {
    this.vertices.push(v);
  }
};
var g = new Graph();
//g has own properties: vertices[] and edges[], g doesn't have prototype property.
//Graph.prototype ---> Function.prototype ---> Object.prototype ---> null


Capitalize the first letter for constructor function.

Object() is Person()'s prototype object and constructor, Person() is person1's prototype object and constructor.
_proto_ contains the object's constructor's prototype object.

object's prototype is the property on each instance, available via 
    Object.getPrototypeOf(person1)
    person1._proto_ 
    //person1._proto_ is derived from the prototype property on the constructor which is Person.prototype
prototype property on constructor function is the property on the constructor. 
    person1._proto_ --> Person.prototype
    person1._proto_._proto_ --> Object.prototype
    Person.prototype._proto_ --> Object.prototype //Person.prototype is an object, prototypt property's value
    Person._proto_ --> f() {[native code]}
Only constructor function/object has prototype object.
The created instance, itself is prototype object, don't have prototype property.

Calling a function with the new operator returns an object that is an instance of the function. Own properties can then be added onto this object.

variable and function in object called property and method.

The prototype property's value is an object, which is basically a bucket for storing properties and methods that we want to be inherited by objects further down the prototype chain.

inherited properties and methods are the ones begin with:
Object.prototype.

methods/properties available just on the Object() constructor itself:
Object.

