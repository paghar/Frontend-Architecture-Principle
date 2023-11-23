# Contributing Guidelines

## I Have a Question

Before you ask a question, it is best to search for existing [Issues](https://github.com/.../issues) that might help you. In case you have found a suitable issue and still need clarification, you can write your question in this issue. It is also advisable to search the internet for answers first.

If you then still feel the need to ask a question and need clarification, we recommend the following:

- Open an [Issue](https://github.com/.../issues/new).
- Follow the **Issue template** and fill it out as completely as possible. Don't forget to:
  - Provide as much context as you can about what you're running into.
  - Provide project and platform versions (nodejs, npm, etc), depending on what seems relevant.

We will then take care of the issue as soon as possible.


## Issue template
### Feature request: Suggest an idea for application

- [ ]  I have searched the [Issues](https://github.com/.../issues) to see if this feature has already been reported
- [ ]  I have tested the latest version

### Summary

Describe how it should work, and provide examples of the solution, which might include screenshots or code snippets.

### Context

What are you trying to accomplish? How is your use case affected by not having this feature?

### Bug report : Report a bug in application

- [ ]  I have searched the [Issues](https://github.com/.../issues) to see if this bug has already been reported
- [ ]  I have tested the latest version

### Steps to reproduce

    1. Go to '...'
    2. Click on '....'
    3. Scroll down to '....'

### Current behavior

    Describe what is currently happening and why it's a problem.

### Expected behavior

    Describe what you expected to happen.

### Context

    What are you trying to accomplish? Does this only happen on a specific browser, screen size, or operating system?

    If possible, provide a live example URL, screenshot, video, or a repository with the minimal reproduction of the issue.


### Your First Code Contribution

#### Creating a Pull Request

1. Clone the fork and add a remote called `upstream`:
```bash
git clone [...]
cd ...
```
2. Create a new branch named after your PR:
```bash
git checkout -b fix/...
```
3. Install dependencies with yarn:
```bash
yarn install
```
4. Start a development server on your machine:
```bash
yarn dev
```
5. Commit changes with `yarn commit` to follow the required commitizen format:
```bash
yarn commit
```
6. Make sure your changes work and don't break anything else:
```bash
yarn prettier:fix && yarn lint && yarn test && yarn build
```
7. Push to your forked repository
```bash
git push -u origin fix/...
```
8. Go to the repository and create a Pull Request 

9. Fill out the Pull Request template, which will be available automatically

