# Contributing Guide

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
yarn dev
```

```json
{
    "scripts": {
        "dev": "concurrently -k \"cross-env BROWSER=none yarn start\" \"wait-on http://localhost:3000 && electron .\"",
        "dist": "yarn build && electron-builder -mw"
    },
}
```
