Create a very very very detailed markdown checklist of all of the stories for this project plan, with one-story-point tasks (with unchecked checkboxes) that break down each story. It is critically important that all of the details to implement this are in this list. Note that a very competent AI Coding Agent will be using this list to autonomously create this application, so be sure not to miss any details whatsoever, no matter how much time and thinking you must do to complete this very challenging but critically important task. It is critically important as well to the agent that it knows what tests to write. From integration tests, unit tests, and e2e tests, every single detail should be spelled out in each story. In every story, please describe what tests to write first and reference the PRD ID in the test descritpion for traceability.

Ensure stories follow these best practices based on project type:

**React/React Native:**

- Use TanStack Query, SUSTAN for storage, MMKV for persistence
- Always use Expo and TypeScript
- For native dependencies not in Expo, include tasks to create Expo development client

**Python:**

- Use UV for environment management

**All Projects:**

- Strongly type and validate environment variables (runtime/build time)
- Follow idiomatic environment variable practices

**Multi-system Projects:**

- Use Turbo Repo for monorepo management
- Include setup instructions for Turbo Repo
- Prioritize getting tests running with shared modules across applications
- Implement TypeScript with shared types
