
# 🐺 Husky the Git Guardian

**Husky** makes managing and sharing Git hooks among us easier!
(This is an example template, feel free to edit it to suit your project's needs.)

You can find the full documentation here : [https://typicode.github.io/husky/](https://typicode.github.io/husky/)

## Setup on a New Project (Empty Folder)

1. Copy the contents of the `.husky` folder as well as the `package.json` file and paste them **at the root of your project**.

2. Run the command `npm install` to install the necessary dependencies.

3. Commit the Husky setup with the following command:
   ```bash
   git commit -m "chore(husky): Husky install" -n
   ```

## Setup on an Existing Project

1. Copy the contents of the `.husky` folder and paste them at the root of your project.

2. Add the line `"prepare": "husky install"` within the "scripts" section of your `package.json` file, like so:

    ```json
    "scripts": {
        "prepare": "husky install" // <== Line to copy!!!
    },
    ```
    Make sure not to remove or overwrite existing scripts.

3. Merge the `devDependencies` from the Husky `package.json` into the `devDependencies` section of your project's `package.json` file.

    ```json
    "devDependencies": {
        "@commitlint/cli": "^13.2.1",
        "@commitlint/config-conventional": "^13.2.0",
        "eslint": "^7.32.0",
        //... other dependencies
    },
    ```

4. Copy any relevant Husky configuration objects such as `lint-staged`, `validate-branch-name`, `commitlint`, and `git-precommit-checks` from the Husky `package.json` to your project's `package.json` file.

5. **OPTIONAL:** You may want to add or customize configurations for `browserslist`, `prettier`, `prettierIgnore`, `stylelint`, `stylelintIgnore`, `eslintConfig`, `eslintIgnore`, etc., according to your project's needs. These can be included in your `package.json` or in separate configuration files.

6. Run the command `npm install` to install the necessary dependencies.

7. Commit the Husky setup with the following command:
   ```bash
   git commit -m "chore(husky): Husky install" -n
   ```

## Hooks available in this template

### commit-msg

The [`commit-msg`](.husky/commit-msg) hook ensures your commit messages meet the required standards.

### post-checkout

The [`post-checkout`](.husky/post-checkout) hook reminds you to rebuild your project if necessary after a checkout.

### post-commit

The [`post-commit`](.husky/post-commit) hook provides a celebratory message confirming the successful commit.

### pre-commit

The [`pre-commit`](.husky/pre-commit) hook runs checks to prevent commits to