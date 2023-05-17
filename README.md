# NodeJS Cheatsheet
NodeJS is a JavaScript runtime built on Chrome's V8 Javascript Engine.

## Installation
- NodeJS Download - [Download](https://nodejs.org/en/download)

## NodeJS Core Modules

A Node.js module is a reusable block of code that encapsulates related functionality, promoting modularity and code reusability in applications.
Below are the most used modules lists:

1. __http__
2. __fs__
3. __path__
4. __os__
7. __stream__
5. __event__
6. __util__
7. __crypto__

### 2. fs
The fs module in Node.js provides file system-related operations, allowing you to interact with the file system, read from and write to files, create directories, and perform other file-related tasks.

1. __Importing fs__ module

```
const fs = require('fs');
```

2. __Reading__ Files:

```
// Asynchronous Read
fs.readFile(path, 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});

// Synchronous Read
const data = fs.readFileSync(path, 'utf8');
console.log(data);
```

3. __Writing__ Files:

```
// Asynchronous Write
fs.writeFile(path, data, 'utf8', (err) => {
  if (err) throw err;
  console.log('File written successfully.');
});

// Synchronous Write
fs.writeFileSync(path, data, 'utf8');
console.log('File written successfully.');
```

4. __Appending__ to Files:

```
// Asynchronous Append
fs.appendFile(path, data, 'utf8', (err) => {
  if (err) throw err;
  console.log('Data appended successfully.');
});

// Synchronous Append
fs.appendFileSync(path, data, 'utf8');
console.log('Data appended successfully.');

```

5. __Creating__ Directories:

```
fs.mkdir(path, { recursive: true }, (err) => {
  if (err) throw err;
  console.log('Directory created successfully.');
});

```

6. Checking if a __File or Directory Exists__:

```
fs.existsSync(path); // Returns true or false

```

7. __Renaming__ or __Moving__ Files:

```
fs.rename(oldPath, newPath, (err) => {
  if (err) throw err;
  console.log('File renamed successfully.');
});


```

8. __Deleting__ Files:

```
fs.unlink(path, (err) => {
  if (err) throw err;
  console.log('File deleted successfully.');
});

```


9. __Reading__ Directories:

```
fs.readdir(path, (err, files) => {
  if (err) throw err;
  console.log(files);
});
```
