<general_rules>
When creating new functions or modules, always first search in the `src/` directory to see if similar functionality exists. If not, create it within an existing or new file in the `src/` directory.

Before committing, ensure your code adheres to the repository's style and linting rules. You can run the following scripts:
- To format your code: `yarn format`
- To check formatting: `yarn format:check`
- To lint your code: `yarn lint`
- To automatically fix linting issues: `yarn lint:fix`
</general_rules>

<repository_structure>
This repository is a TypeScript template project. The main application logic resides in the `src/` directory, with the primary entry point being `src/index.ts`. Compiled output is placed in the `dist/` directory. Test files are located within the `src/` directory, following the `*.test.ts` naming convention.
</repository_structure>

<dependencies_and_installation>
This project uses `yarn` as its package manager (version `3.5.1`). To install all necessary dependencies, run `yarn install` in the root of the repository. A `yarn.lock` file will be generated upon the first installation.
</dependencies_and_installation>

<testing_instructions>
Tests in this repository are written using Jest and TypeScript, configured via `jest.config.js` and `ts-jest`. Test files are identified by the `*.test.ts` suffix and are located within the `src/` directory.

To run tests:
- Run all unit tests (excluding integration tests): `yarn test`
- Run only integration tests: `yarn test:int`
- Run a specific test file with an extended timeout (useful for debugging): `yarn test:single <path/to/your/test.test.ts>`

Environment variables for tests are loaded via `dotenv/config` as configured in `jest.config.js`.
</testing_instructions>

<pull_request_formatting>
Pull request titles must follow the Conventional Commits specification. The allowed types are:
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- `ci`: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- `chore`: Other changes that don't modify src or test files
- `revert`: Reverts a previous commit
- `release`: New release

Examples:
- `feat: add user authentication`
- `fix(auth): resolve login issue`
</pull_request_formatting>

