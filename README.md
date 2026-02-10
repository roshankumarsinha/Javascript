<h1>JavaScript</h1>

<h2>Notes/Concepts of JS</h2>
<ul>
  <li><a href="https://alok722.github.io/namaste-javascript-notes/lectures.html">Basic JS Notes</a></li>
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
            <li>Array.from() -> Used to create new array. Ex : <code>Array.from( {length: 5}, (_, i) => ({id: i+1, name: `name${i+1}`} ))</code>
            </li>
            <li>length -> arr.length property gives length of array. Ex: [1,2,3].length gives 3 as output.</li>
            <li>[].every(callback) -> Every returns true only if all the elements in the array satisfy the callback conditions otherwise false. Ex : <code>const isBelowThreshold = (currentValue) => currentValue < 40; [1, 30, 39, 29, 10, 13].every(isBelowThreshold)  // Returns true</code></li>
            <li>[].some(callback) -> Some returns true if it finds one element in the array that satisfies the provided testing function. Otherwise, it returns false.
            </li>
            <li>[].find(callback) -> Finds that 1st element of array which satisfies the callback function conditions, if no value is found then it returns undefined. Ex : <code>const inventory = [
  				{ name: "apples", quantity: 2 },
  				{ name: "bananas", quantity: 0 },
  				{ name: "cherries", quantity: 5 },
			];  const result = inventory.find(({ name }) => name === "cherries");</code></li>
            <li>[].findIndex(callback) -> Finds the index of 1st element of array which satisfies the callback function conditions, otherwise returns -1.</li>
            <li>[].includes(value to search for) -> Includes search for the value specified, returns true if found otherwise false. Note it doesn’t take callback function instead it takes value to search for.</li>
            <li>[].indexOf(Element to locate in the array) -> Similar to findIndex but just difference is that instead of taking callback function it takes value to locate in array.</li>
            <li>[].join(separator) -> Very useful to convert array into string by separator. If no separator is provided then by default it returns a string separated by commas.</li>
            <li>[].pop() -> Removes the last element from an array and returns that element. This method changes the length of the array.</li>
            <li>[].push(element) -> Adds the new element to the end of an array. This method changes the length of the array.</li>
            <li>[].reverse() -> Reverse the existing array and no new array is created.</li>
            <li>[].shift() -> Very Important to implement queue. As shift removes the first element from an array and returns that removed element. This method changes the length of the array.</li>
            <li>[].unshift(element) -> Adds that element to front of array. But it returns new length of array.</li>
            <li>[].slice(startIndex, endIndex) -> Creates a new array from startIndex till endIndex but endIndex is excluded(from startIndex to one element before endIndex). If endIndex is not provided then it takes till end.</li>
            <li>[].sort(compareFn) -> Sorts the elements of an array and returns the reference to the same array
                <ul>
                    <li>If compareFn is omitted, the array elements are converted to strings, then sorted according to each character’s.</li>
                    <li>compareFn takes 2 arguments :-</li>
                    <li>a : The first element for comparison.</li>
                    <li>b : The second element for comparison.</li>
                    <li>It should return a number where :-
                        <ul>
                            <li>A negative value indicates that a should come before b.</li>
                            <li>A positive value indicates that a should come after b.</li>
                            <li>Zero or NaN indicates that a and b are considered equal.</li>
                            <li>To memorize this, remember that (a, b) => a - b sorts numbers in ascending order, and  (a, b) => b - a sorts in descending order.</li>
                            <li>If you want to sort in ascending order, then return -1 will tell a comes before b, but if you want to sort in descending order then return +1 which tells that b comes before a.</li>
                            <li>If you want to sort the array but don’t want to alter the existing array then you can do something like : const sorted = [...arr].sort();  Here, […arr] creates a shallow copy, so sort() does not mutate the original</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
    <li>
        <b>Object :-</b>
        <ul>
            <li>Object is a collection of key-value pairs.</li>
            <li>Object.groupBy(obj, callbackFn) -> Here, obj is Array of object and callbackFn takes each element of array one by one, it returns in an object where keys represent the grouping criteria and values are arrays of the grouped elements.
            <li>Object.groupBy(obj, callbackFn) -> Here, obj is Array of object and callbackFn takes each element of array one by one, it returns in an object where keys represent the grouping criteria and values are arrays of the grouped elements.<pre>
                <code>
                    const inventory = [
                        { name: 'apples', type: 'fruit', quantity: 2 },
                        { name: 'oranges', type: 'fruit', quantity: 5 },
                        { name: 'bananas', type: 'fruit', quantity: 5 },
                        { name: 'cherries', type: 'fruit', quantity: 5 },
                    ];
                    const grouped = Object.groupBy(inventory, item => item.type);
                    console.log(grouped);
                    <!-- Output will be -->
                    <!-- { fruit: [ { name: 'apples', type: 'fruit', quantity: 2 }, { name: 'oranges', type: 'fruit', quantity: 5 }, { name: 'bananas', type: 'fruit', quantity: 5 }, { name: 'cherries', type: 'fruit', quantity: 5 } ] } -->
                </code>
            </pre></li>
        </ul>
    </li>
    <li>
        <b>String :-</b>
        <ul>
            <li>We can access any character in string using str[index] same as array.</li>
            <li>length -> str.length is used to calculate length of string. Ex “Roshan”.length will give 6.</li>
            <li>str.includes(searchString) -> Performs a case-sensitive search to determine whether a given string may be found within this string, returning true or false respectively. Ex : <code>"Blue Whale".includes("Blue")   // true</code></li>
            <li>str.indexOf(searchString) -> The index of the first occurrence of searchString if found, otherwise -1 if not found.</li>
            <li>str.lastIndexOf(searchString) -> Finds last occurrence of the searchString if found, otherwise -1 if not found.</li>
            <li>str.replace(pattern, replacementString) -> Returns a new string with one or all matches(if regex //g with global is used) of the pattern replaced by the specified replacement.
                <ul>
                    <li>Ex : <code>const p = "Roshan is good boy boy"; const p1 = p.replace("boy", "girl");</code> p1 output is "Roshan is good girl boy". If you use <code>const regex = /boy/g; const p2 = p.replace(regex, "girl");</code> p2 output is "Roshan is good girl girl"</li>
                    <li>We can use str.replaceAll() to replace all the pattern words with replacementString.</li>
                </ul>
            </li>
            <li>str.slice(indexStart, indexEnd) -> It returns a new substring from startIndex till endIndex but excluding endIndex. Ex: <code>"The morning is upon us.".slice(1, 8)</code> will return "he morn"</li>
            <li>str.split(separator) -> It returns an array of strings, split at each point where the separator occurs in the given string.
                <ul>
                    <li>Ex : <code>const str = "The quick brown fox"; const words = str.split(" ");</code> // words = ["The", "quick", "brown", "fox"]</li>
                    <li><code>const chars = str.split("")</code> // chars = ["T", "h", "e", " ", "q", "u", "i", "c", "k", ...]</li>
                </ul>
            </li>
            <li>str.startsWith(searchString) -> It returns true if the given characters are found at the beginning of the string, otherwise false. Ex : <code>"To be, or not to be".startsWith("To be")</code> // true</li>
            <li>str.endsWith(searchString) -> It returns true if the given characters are found at the end of the string, otherwise false. Ex : <code>"question.".endsWith("question.")</code> // true</li>
            <li>str.toLowerCase() -> A new string representing the calling string converted to lower case. Ex : <code>"ALPHABET".toLowerCase()</code> // 'alphabet'</li>
            <li>str.toUpperCase() -> A new string representing the calling string converted to upper case. Ex : <code>"alphabet".toUpperCase()</code> // 'ALPHABET'</li>
            <li>str.trim() -> Removes whitespace from both ends of this string and returns a new string, without modifying the original string.</li>
            <li>str.trimEnd() -> Removes whitespace from the end of this string and returns a new string, without modifying the original string.</li>
            <li>str.trimStart() -> Removes whitespace from the beginning of this string and returns a new string, without modifying the original string.</li>
        </ul>
    </li>
    <li>
        <b>Map :-</b>
        <ul>
            <li>A Map stores data as key → value pairs.</li>
            <li>Keys and Values can be anything (object, array, function, number, etc.).</li>
            <li>A key in the Map may only occur once; it is unique in the Map's collection.</li>
            <li>Map maintains insertion order. Think of like a vector. That's why it is used in LRU.</li>
            <li>Methods of map :-
                <ul>
                    <li>Creating map -> <code>const newMap = new Map();</code></li>
                    <li>set() -> Adds a new entry with a specified key and value to map or updates an existing entry if the key already exists. Ex: <code>newMap.set("bar", 1)</code>. It returns map object (which is newMap).</li>
                    <li>You can also set value like : <code>const mp = new Map([[1, 10], [2, 20], [4, 40], [3, 30]]);</code> Here each array acts as [key, value].
                        <ul>
                            <li>You can then form again array like : <code>const arr = [...mp];</code> Array will look like : [[1, 10], [2, 20], [4, 40], [3, 30]]</li>
                        </ul>
                    </li>
                    <li>get() -> It returns the value corresponding to the key in this Map, or undefined if there is none. Ex: <code>myMap.get("bar")</code> will return 1.</li>
                    <li>has() -> It returns a boolean indicating whether an entry with the specified key exists in this Map or not. Ex: <code>myMap.has("bar")</code> will return true.</li>
                    <li>delete() -> It removes the entry specified by the key from this Map. It returns true if an entry in the Map object has been removed successfully otherwise false if the key is not found in the Map. Ex: <code>myMap.delete("bar")</code> will return true.</li>
                    <li>size -> It returns the number of elements in this map. Ex: <code>myMap.size</code> will return 1.</li>
                    <li>clear() -> It removes all elements from this map.</li>
                    <li>We can iterate on map using entries(), keys(), values().
                        <ul>
                            <li>Use for…of loop to iterate over this.</li>
                            <li>Ex: <code>for(const [k,v] of myMap.entries())</code> -> this will return both key, value. Or <code>for(const key of myMap.keys())</code> -> this will only return key. Or <code>for(const val of myMap.values())</code> -> this will only return values.</li>
                            <li>Note the iteration order will be same as insertion order as map maintains order.</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
    <li>
        <b>Set :-</b>
        <ul>
            <li>Set object lets you store unique values of any type, whether primitive values or object references.</li>
            <li>It stores only unique values.</li>
            <li>Set also maintains insertion order.</li>
            <li>Methods in Set :-
                <ul>
                    <li>Creating set -> <code>const newSet = new Set();</code></li>
                    <li>add() -> It inserts the specified value into this set, if it is not already present. Ex: <code>newSet.add(1)</code>. It returns set object (which is newSet).</li>
                    <li>You can also add value like : <code>const st = new Set([1,2,3,1,5,6,3]);</code> We are passing array of numbers into the set.
                        <ul>
                            <li>You can then form again array like : <code>const arr = [...st];</code> But this arr will only contain unique values, duplicated value will be removed.</li>
                        </ul>
                    </li>
                    <li>has() -> It returns a boolean indicating whether an entry with the specified value exists in this Set or not. Ex: <code>st.has(1)</code> will return true.</li>
                    <li>delete() -> It removes the specified value from this set, if it is in the set. It returns true if a value in the Set object has been removed successfully, otherwise returns false if the value is not found in the Set.</li>
                    <li>size -> It returns the number of elements in this set. Ex: <code>st.size</code> will return 5.</li>
                    <li>clear() -> It removes all elements from this set.</li>
                    <li>We can iterate on set using values(), since set has only value.
                        <ul>
                            <li>Use for…of loop to iterate over this.</li>
                            <li>Ex: <code>for(const val of st.values())</code> -> the val will return each value of set.</li>
                            <li>Note the iteration order will be same as insertion order as set maintains order.</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
</ul>
