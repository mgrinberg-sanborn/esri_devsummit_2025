# What is REST JS and why is it different from Javascript SDK

## Intro

- <https://github.com/Esri/arcgis-rest-js>
- Open source, lightweight javascript library for using the ArcGIS REST APIs and Node apps
- 100% Test coverage across the API
- New versions pretty frequently
- Core library is 10kb
- Maximize Compatibility
- Available packages
  - Update items
  - Search route
- Project Structure, have a screenshot of overall structure
  - Tools for auth (Oauth / API key management) are most interesting
- Can be used for dashboards and management Uis, scripting and automation, servers and backend, authentication

- Basic Usage and concepts
  - Npm install @esri/arcgis-rest-request
  - Import {request} from "@esri/arcgis-rest-request"

- Authentication Managers
  - Import {ApiKeyManager} from @esri/arcgis-rest-request
  - OR ARCGISIdentityManager
    - Can use Oauth here with beginOAuth2 and CompleteOAuth2

- Handling Errors:
  - Network/Auth Errors reject the promise.
  - See error screenshot
  - Auth Errors
    - Invalid token response (there is a retry method)

## Demos

- API Key to Rotate
  - Use API keys instead of passcodes and limited the scope of those API keys

- Demo of getting all registered Oauth apps
  - nextPage method with this that you can call to just grab that next page and concatenate instead of having to do next page
  - Console.table for an array in table format

- Creating a new feature service and filling it with data.
  - Uses a feature service package
    - Can specify schema, etc. when creating a feature service
  - Can also use an endpoint for adding data that analyzes the items, batch geocodes, and schema and publishes them
- Also showed this as a web app where you can create these, using Calcite (ESRI's name for their UI/UX, which I hate!)

## What's new / Roadmap

- Support for new Node and Typescript
