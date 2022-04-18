#### Eslint & Prettier setup

-   [ ] npm install -g eslint
-   [ ] eslint --init
-   [ ] Select appropriate options , given eslint settings needs to be added additionally.
-   [ ] npm install eslint-config-prettier eslint-plugin-prettier husky lint-staged
-   [ ] npx husky-init (Will setup pre-commit hook)
-   [ ] Edit npx in husky precommit file

##### .eslintrc configuration

```
"extends": [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:prettier/recommended"
]


"rules": {
		"react/react-in-jsx-scope": "off",
        }

"settings": {
		"react": {
			"version": "detect"
		}
	}

"env": {
		"jest": true
	},
```

📝 `Indent` will be taken care by prettier , `no need to mention` Indent rule in eslint

##### .prettierrc configuration

```
{
    "semi": true,
    "tabWidth":4,
    "printWidth": 100,
    "singleQuote": false,
    "trailingComma": "none",
    "useTabs":true
}
```

##### Package.json

```
"lint": "eslint src/**/*.js",
"fix": "eslint src/**/*.js --fix",
"format": "prettier --write \"**/*.{js,jsx,json,md}\""
```

```
"lint-staged": {
	"*.{js,jsx,json,css,md}": "npm run format"
	            }
```
