# Best Practices for Testing

## Overview

- **QA & Developers perform Functional Testing**
  - End-to-end tests
  - Time-consuming to automate
  - Often fragile
- **QA & Developers perform Visual Testing**
- **Developers perform Integration Testing**
- **Developers perform Unit Testing**
  - Tests small components
- **Testing Pyramid Efficiency**
  - The further down the pyramid (unit tests), the greater the return on investment

## Best Practices

- **Don't test other people's code**
- **Encapsulation**
  - Separate each piece of functionality
  - Keep logic independent
  - Avoid embedding actions like `onClick` events
  - Consider writing test plans before coding
  - Utilize AI assistance to draft test cases
- **Prioritization**
  - New projects should integrate testing from the start
  - Existing projects should have tests added when modifying existing functionality
  - Focus on the most critical parts of the application

## Demo

- **Dropping a point on LA**
- **Testing using Jasmine**
  - Specifications (.spec.js)
  - Pass a point string and verify the expected outcome
  - Return an error if the input string is invalid
- **Use Nodemon with Jasmine**
  - Enables real-time testing upon code changes

## Real-World Challenges

- Ensuring cross-browser compatibility
- Device testing (mobile, tablets, touchscreens)
- Handling dynamic content
- Performance testing
- Security testing
- Managing test data
- Facilitating communication and collaboration

## Testing Frameworks

- **Testing follows a bottom-up approach**
  - Lower levels involve developers testing fine-grained components
- **Unit Testing**
  - **Vitest** (testing-library)
- **Integration Testing**
  - No specific framework but a "golden path" test encompassing multiple unit tests
  - Great starting point for testing
- **Visual Testing**
  - Ensures UI consistency and user experience
- **Functional Testing**
  - Final validation, often manual
  - Covers application functionality in multiple ways
  - Tools include Selenium, Puppeteer, Playwright
  - Automate setup tests for database population
- **Vitest UI**
- **Storybook for UI testing**
  - Allows component interaction
- **Playwright**
  - Runs in Node.js and aligns console messages with visual changes

## Collaboration

- Plan and review testing strategies
- Maintain a dedicated team communication channel for testing
- Provide open access to test results
- Keep code owners informed about test outcomes
- **Document testing procedures and results**

## Automating Testing

1. **Code Source**
   - Developers push code to a version control system (e.g., GitHub)
2. **CI/CD Pipeline Triggers**
   - GitHub Actions initiates the build process
3. **Build Step**
   - Install dependencies (`npm install`)
4. **Transpilation**
   - Convert source code (e.g., via Vite, TypeScript Compiler, Webpack)
5. **Testing Execution**
   - Run tests using the chosen framework
6. **Deployment**
   - Managed via CI/CD tools (e.g., GitHub Actions, CircleCI, Jenkins)

### CI/CD Tools

- **GitHub Actions**
  - Tightly integrated with GitHub
  - YAML-based configuration
  - Supports self-hosted runners
  - Configurations stored in `.github/workflows` folder
  - Example workflow (`cicd.yml`):
    - Includes `name`, `workflow_dispatch`, and `schedule` (e.g., cron jobs)
  - Used for automating pull request checks
- **CircleCI**
  - Cloud-based CI/CD platform
  - Strong Docker support
- **Jenkins**
  - Self-hosted
  - Maximum flexibility but steeper learning curve

## Questions?

