# Rudderstack Docusaurus Plugin

A Docusaurus plugin for [Rudderstack](https://rudderstack.com/) that sends page event on each page switch.

For full documentation and configuration, see [Rudderstack JS sdk](https://www.rudderstack.com/docs/sources/event-streams/sdks/rudderstack-javascript-sdk/)

## How to install

1. Build `docusaurus-plugin-rudderstack`

    `npm run build`

This creates dist folder that has index.js file.

2. Add plugin to `docusaurus.config.js`

    ```javascript
    module.exports = {
      plugins: [
        [
            require.resolve("../dist/index.js"),
            {
            appUrl: "https://rudderstack.com",
            writeKey: "RUDDERSTACK_WRITE_KEY",
            dataPlaneUrl: "RUDDERSTACK_DATAPLANE_URL",
            },
        ],
      ],
    };
    ```

3. Test it works, go to testDocusaurus folder

    ```bash
    npm install

    npm run start
    ```
