# jira-app-tutorial
https://developer.atlassian.com/cloud/jira/platform/getting-started/

## Dependencies
- [ngrok](https://ngrok.com/)
  - ngrok exposes local networked services behinds NATs and firewalls to the public internet over a secure tunnel. Share local websites, build/test webhook consumers and self-host personal services.
- [http-server](https://www.npmjs.com/package/http-server)

## Local development instructions
1. Navigate to `jira-app-tutorial` directory
1. ```http-server -p 8000```
1. ```ngrok http 8000```
1. From ngrok information table, copy the `Fowarding` HTTPS URL
1. Paste the copied URL into the value for `baseUrl` in the `atlassian-connect.json`. Verify this URL works as expected when visited locally, and then use this URL when uploading to Jira apps.

### Useful Links
- [Atlassian Connect validator](https://atlassian-connect-validator.herokuapp.com/validate)
  - Validates `atlassian-connect.json` app descriptor files
- [Jira modules documentation](https://developer.atlassian.com/cloud/jira/platform/about-jira-modules/)
- [Atlaskit](https://atlaskit.atlassian.com/)
  - Library of reusable front-end UI components
  - Eg, CSS: `<link rel="stylesheet" href="https://unpkg.com/@atlaskit/css-reset@2.0.0/dist/bundle.css" media="all">`
- [Atlassian Connect JavaScript API documentation](https://developer.atlassian.com/cloud/jira/platform/about-the-javascript-api/)
  - Client library for API included via: `<script src="https://connect-cdn.atl-paas.net/all.js" async></script>`