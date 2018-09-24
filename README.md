# per-project-node-version
At the time of writing I had installed Node v8.11.1 on my Mac but I'd like to test if I can add and use a custom version of Node.
Then I installed the v10 with
```bash
npm install --save-dev node@10
```
so if you run
```bash
node index.js
```
the result is
```
TypeError: Cannot read property 'open' of undefined
    at doTruncate (/Users/NoriSte/Sites/noriste/per-project-node-version/index.js:13:35)
```
Instead, if you run
```bash
npm test
```
you get
```
Node.js

(node:6157) ExperimentalWarning: The fs.promises API is experimental
Node.js
```
and it means that the local NPM uses the node@10.fs APIs.
