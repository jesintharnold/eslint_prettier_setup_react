###ESLINT SETUP
*******
####Global Install
- [ ] npm install -g eslint 
- [ ] eslint --init
- [ ] npm install -g eslint-plugin-react
---
####Invidual project Install
- [ ] npm install eslint --save-dev
- [ ] npm init @eslint/config
- [ ] npx eslint yourfile.js (we can run any file invidually like this)
- [ ] npm install eslint-plugin-react --save-dev
---
#### REACT
---
```
"extends": [
    "eslint:recommended",
    "plugin:react/recommended"
]
```

```
"lint": "eslint src/**/*.js src/**/*.jsx"
```
