# Monitus-Mentor

## Project Description

This project aims at emulating a **real-life** software development scanario, where a **virtual supervisor** will oversee your personal project.

### User experience

The supervisor (Bot) will:

1. Obtain user-defined project description, as well as goals and milestones if provided
2. Bot then follows agile development practice and iterate through project requirement and discuss with user
3. Bot assigns tasks and tickets to let user to follow
4. After user pushes to repo and performs a merge request, Bot will look at:
  - commit messages
  - pull request content quality
  - actual code changes
5. Bot ensures project has sufficient test cases and good code quality through CI/CD and code quality test like SonarQube
6. Bot will provide feedback if anything goes wrong, in terms of code quality and documentation of messages and pull request doc
7. Bot will approve merge request if accepted and proceed to next task

### Technical stuff

1. Bot is an LLM agent which has access to user's github repo and has right to view code changes and approve merge request
2. Bot has local memory of past conversations and code changes stored in sqlite
3. The whole application is bundled as a single executable with UI as a webpage

### Dependencies

- LLM: Langchain, OpenAI with user Auth provided
- Memory: LlamaIndex
- UI: NiceGUI