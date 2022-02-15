# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### 개발 lint , prettier 참조

https://kimdabin.tistory.com/entry/Reactjs-ESLint%EC%99%80-Prettier%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-React-%ED%99%98%EA%B2%BD-%EC%84%A4%EC%A0%95-VSCode

npm install eslint --save-dev
npm install prettier --save-dev --save-exact
npm install eslint-plugin-prettier eslint-config-prettier --save-dev

익스텐션 Prettier ESLint 설치

.eslintrc.js
module.exports = {
root: true,
env: {
browser: true,
es6: true,
},
extends: [
"plugin:@typescript-eslint/recommended",
// typescript 표준 규칙 모음
"plugin:import/errors",
"plugin:import/warnings",
"plugin:import/typescript",
// import 관련 규칙 모음

        "plugin:prettier/recommended",
        "prettier/@typescript-eslint",
        "prettier/react",
         // prettier 관련 규칙 모음
    ],
    parserOptions: {
        ecmaVersion: 2018,
        project: ["./tsconfig.json"],
        // tsconfig 파일의 경로를 참조 해줍니다.
        // 기준은 root 입니다.
    },
    rules: {
            // 추가하고 싶은 rule을 더 추가해줍니다.
        }

};

.prettierrc.js

module.exports = {
endOfLine: "lf",
tabWidth: 4,
semi: true,
singleQuote: false,
trailingComma: "all",
printWidth: 120,
};

setting.json
{
"editor.defaultFormatter": "esbenp.prettier-vscode",
"[typescriptreact]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[typescript]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"editor.formatOnSave": true
}
