# CONTRIBUTIN GUIDE

## Create react application

```shell
npx create-react-app .
npm run build
npm start
```

## Create electron application

```shell
npm i --save-dev electron electron-builder concurrently wait-on
npm i cross-env
```

```shell
npm run electron:start
```

```json
{
    "scripts": {
        "electron:start": "concurrently -k \"cross-env BROWSER=none yarn start\" \"wait-on http://localhost:3000 && electron .\"",
        "electron:build": "yarn build && electron-builder -mw"
    },
}
```
