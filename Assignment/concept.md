
**Advance Web Technology**

   **1.HTTP methods are:**

GET – Retrieve data (e.g., a webpage or an API resource).

POST – Submit data to create a new resource.

PUT – Update or replace a resource entirely.

PATCH – Partially update a resource.

DELETE – Remove a resource.

HEAD – Like GET, but only returns headers (no body).

OPTIONS – Describes the communication options for the target resource.

 **HTTP status codes:**

 200 OK

201 Created

202 Accepted

204 No content

206 Partial Content

300	Multiple Choices

301	Moved Permanently

303	See Other	Redirect to another resource using GET.

304	Not Modified

307	Temporary Redirect

308	Permanent Redirect

400	Bad Request

401	Unauthorized

403	Forbidden	Access denied even if authenticated.

404	Not Found

405	Method Not Allowed

408	Request Timeout

410	Gone

415	Unsupported Media

429	Too Many Requests	Rate limit exceeded.

500	Internal Server Error

501	Not Implemented

502	Bad Gateway

503	Service Unavailable

504	Gateway Timeout

505	HTTP Version Not Supported 

**Four CSS selectors**

1.Element Selector

```
h1 {
  font-size: 30px;
}
``````

2.Class selector
```
.card {
  border: 1px solid gray;
}
```
3.ID selector
```
#main {
  background-color: lightblue;
}
```
4. Pseudo-class selector

```
a:hover {
  color: red;
}
```
**GIT Basics**

1.git init:-> Initializes a new Git repository in folder.
 command=git init ( This creates a hidden .git folder and starts tracking changes.)
  
  1. git add:-> Adds changes or a specific file.
      command= git add filename.txt(specific file)/ git add.(for all files)
  
  2. git commit:-> Saves the staged changes to the local repository
      command= git commit -m "Your meaning full message"
  
  3. git push:-> Sends local commits to the remote repository(eg. Github).
      command= git push origin main (using main and master depends on branch)

  4. git pull:-> Fetches changes from the remote repositoty and merges them into  our local branch.
      command= git pull origin main

  5. git clone:-> copies an entire remote repository to your local machine.
     command= git clone https://github.com/username/repo-name.git

  6. git branch:-> Used to manage branches (isolated version of project)
      command= git branch (view all branch)
               git branch feature-1 (creats a new branch)
               git checkout feature-1 ( switch to a branch)
               git checkout -b feature-1 

**Callback and Higher-Order function**

**Callback** – A function passed as an argument into another function to be executed later.


```
function greet(name, callback) {
  console.log("Hi " + name);
  callback();
}

function sayBye() {
  console.log("Goodbye!");
}

greet("Lumi", sayBye);
````

**Higher-Order**- Function that takes another function as an argument or returns a function.
````
function multiplyBy(factor) {
  return function (number) {
    return number * factor;
  };
}

const double = multiplyBy(2);
console.log(double(5)); // 10
````

**Array Methods: (filter , map , forEach , push , pop)**
```
// forEach
const result = numbers.forEach((num) => console.log(num + 1));


// map
const squares = numbers.map(num => num * num);


// filter 
const even = numbers.filter(num => num % 4 === 0);

// push
numbers.push(6); // [1,2,3,4,5,6]

// pop 
numbers.pop(); // [1,2,3,4,5]

```
