# node-red-template

This is a template for a Node-RED project meant to be run in local mode. The idea is to run an instance of Node-RED entirely from within a local directory to make it more portable. This also makes running multiple instances of Node-RED at the same time easier.

Node-RED will start with a blank canvas and will save the flow file to flows.json the first time a deploy is done. If you add your own flows.json file it will load that by default.

## Usage

1. Go to https://github.com/s1seven/node-red-template and click on `Use this template`.
2. Clone your newly created repository
3. Install dependencies (eg: `npm install`)
4. Start Node-RED with `npm start`

When running multiple instances in parallel, you can specify a port:

```
npm start -- -p 1885
```

To run a specific flow file:

```
npm start -- testFlow.json
```

## Dependencies

You can easily add third party nodes by modifying the package.json file. This template include the following dependencies:

- `node-red-dashboard` to build UI
- `@s1seven/schema-tools-certificate-summary` to extract certificate general information
- `@s1seven/schema-tools-extract-emails` to get parties involved in a certificate's transaction
