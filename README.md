<h1>JavaScript</h1>

<h2>Notes/Concepts of JS</h2>
<ul>
  <li><a href="https://alok722.github.io/namaste-javascript-notes/dist/lectures.html">Basic JS Notes</a></li>
  <li>Rest Study from JavaScript Folder Notes</li>
  <li><a href="https://chatgpt.com/share/68fb4a34-0490-8006-ae73-60fd54ad37d2">Call, Apply, Bind for Normal, Arrow and IIFE Functions</a></li>
  <li><a href="https://chatgpt.com/share/691f42a2-54a0-8006-b3ff-e908562b172b">THIS behaviour for Normal, Arrow and IIFE Functions</a></li>
  <li><a href="https://chat.deepseek.com/share/sajt080zlq15e6tgul">Static keyword in JS (Can be used to make global object something like Redux)</a></li>
  <li>
    <b>Classes in JS</b>
    <ul>
        <li>When we call with ‘new’ keyword, it calls constructor and returns an object.</li>
        <li>Classes are made using ES6 syntax.</li>
        <li><a href="https://chatgpt.com/share/695d22bd-deac-8006-8f77-be8d65d60be4">Study Classes</a></li>
        <li>Note : Primitive data types gets memory in stack, but non-primitive data type(like class) get memory in heap.</li>
        <li><a href="https://chatgpt.com/share/695d2472-9918-8006-a1ae-da13159264d8">Heap Memory v/ Stack Memory</a></li>
    </ul>
  </li>
  <li>
    <b>Prototypes in JS</b>
    <ul>
        <li>Prototype is a shared object that holds common methods. Everything inside ClassName.prototype will be shared by all ClassName object.</li>
        <li><a href="https://chatgpt.com/share/695d20dd-527c-8006-8f2e-b0b263026eef">Prototypes in JS</a></li>
    </ul>
  </li>
</ul>

<h2>Important Output Questions</h2>
<ul>
  <li><a href="https://github.com/surbhidighe/Javascript-Output-Based-Questions">Solve Question numbers :- 2, 3, 4, 5, 9, 12, 15, 16, 17, 18, 24, 25, 28, 30, 33, 36, 41, 42, 43, 45, 47, 50</a></li>
  <li><a href="https://chatgpt.com/share/6976083e-c564-8006-9e50-6930628fa3e0">For Question no. 41 check this link</a></li>
  <li><a href="https://umarfarooquekhan.medium.com/javascript-tricky-promises-related-questions-nodejs-aca3f7c4ed80">Solve Promises Questions</a></li>
</ul>

<h2>Things to Keep in Mind about Array, Object, String, Map, Set</h2>
<ul>
    <li>Try to use normal function instead of arrow function because this is consistent in normal function.</li>
    <li>Use for(const val of arrays) -> Use for…of loop to loop arrays</li>
    <li>Use for(const val in obj) -> Use for…in loop to loop objects. Here val represents ‘key’.</li>
    <li>Use for(const [k,v] of Object.entries(obj)) -> Object.entries() return an array with key and value</li>
    <li>Similarly we have Object.keys() -> Which returns an array with keys of object, and similarly Object.values() return an array with values of object.</li>
    <li>Object.freeze() -> It freezes the obj which means an obj can no longer be changed, no new properties can be added, no existing properties can be removed or changed.</li>
    <li>Object.seal() -> Here existing properties can be changed but no new properties can be added.</li>
    <li>
        Difference between …args and args :-
        <ul>
            <li>fn(…args) mean spread the array so each item becomes its own argument. Ex : if args = [2, 3] then, fn(...args) === fn(2, 3);</li>
            <li>But if just write args then it’s an array, so in above line we are spreading the array. args === [].</li>
            <li>Mostly if we have to accept arguments and pass arguments in function and we don’t know the count then use …args but if we have to use array like for JSON.stringify(args)</li>
        </ul>
    </li>
    <li>
        typeof :- It returns the type of a variable.
        <ul>
            <li>typeof for any function will return “function”</li>
            <li>typeof for any object will return “object”</li>
            <li>typeof for array also return “object” since array is also an object, so to check if any argument is array or not use Array.isArray(arr)</li>
            <li>typeof for any string will return “string”</li>
            <li>typeof for any number will return “number”</li>
            <li>typeof for any boolean will return “boolean”</li>
            <li>typeof for any undefined will return “undefined”</li>
            <li>typeof for any null will return “object”</li>
        </ul>
    </li>
    <li>
        <b>Array :-</b>
        <ul>
            <li>Array.isArray() -> Determines whether passed value is array or not</li>
            <li>Array.from() -> Used to create new array. Ex :
            <code>
                Array.from( {length: 5}, (_, i) => ({id: i+1, name: `name${i+1}`} ))
            </code>
            </li>
        </ul>
    </li>
</ul>
