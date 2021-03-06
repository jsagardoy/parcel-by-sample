# SASS

Let's see how to add SASS support

# Steps to build it

## Prerequisites

Install [Node.js and npm](https://nodejs.org/en/) (min v8.9) if they are not already installed on your computer.

> Verify that you are running at least node v8.x.x and npm 5.x.x by running `node -v` and `npm -v` in a terminal/console window. Older versions may produce errors.

## Steps

- We will start from _02 custom css_, just copy the project and execute _npm install_

```cmd
npm install
```

- We will need to install node-sass

```bash
npm instal node-sass --save-dev
```

> We could skip this step and let parcel detect it automatically when we are running the build
it will automatically install it.

- Now let's rename _mystyles.css_ to _mystyles.scss_ and update the content.

_mystyles.scss_

```diff
+ $blue-color: teal;

.red-background {
- background-color: indianred;
+ background-color: $blue-color;
}
```

- Let's update _index.js_ to point out the sass file

_index.js_

```diff
- import './mystyles.css';
+ import './mystyles.scss';

const sampleNumber = 1;
console.log(`Hello from sample ${sampleNumber}`);
```

- Let's run the sample.

```bash
npm start
```



