# Small Hours

A local web application that suggests short outdoor activities. The interface collects preferences, and a Node.js server filters activities and ranks suitable options.


## Run the fixture demo

Use Node.js 22 or newer:

```sh
npm run demo
```

Open http://127.0.0.1:4317. Fixture mode uses deterministic ranking and does not run AI inference.

## Run local model inference

```sh
npm ci
npm run setup:model
npm start
```

Setup downloads the pinned model assets. Normal inference uses the local CPU model. The application reports an unavailable model instead of silently substituting fixture results.

## Check the code

```sh
npm test
```

See [development notes](docs/DEVELOPMENT.md) for the project structure and runtime details.
