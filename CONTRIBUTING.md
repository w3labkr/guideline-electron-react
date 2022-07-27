# CONTRIBUTIN GUIDE

## Create react application

```shell
npx create-react-app .
```

```shell
npm run build
```

```shell
npm start
```

## Create electron application

```shell
yarn add --dev electron electron-builder cross-env concurrently wait-on
yarn add electron-is-dev
```

```shell
yarn electron:build
```

```shell
yarn electron:start
```

```json
{
    "scripts": {
        "electron:start": "concurrently -k \"cross-env BROWSER=none yarn start\" \"wait-on http://localhost:3000 && electron .\"",
        "electron:build": "yarn build && electron-builder -mw"
    },
}
```
