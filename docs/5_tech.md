# Tech

## How does Warestack work?

**We are building a platform that automates workflow creation, execution and monitoring for any codebase in GitHub using AI.**

1. Our ChatGPT-inspired copilot guides users to create workflows and takes care of all configurations and integrations replacing manual work, hacks and tweaks. The copilot utilizes our sythesis service. We parse and tag user’s existing GitHub repositories (codebase, tags, README and more), and then we match with existing composite actions (from our corpus and GitHub Actions marketplace) to generate workflows based on the matched actions.

2. To execute workflows we create the self-hosted runners at the user's region. Our runners are at infrastructure cost and not at billable time on unknown regions as GitHub does. Users can create their own runners, or utilize our powerful runners (again at infrastructure costs).

3. We further have an AI-assistant that consolidates logs and metrics from multiple workflows in a single dashboard. The dashboard helps users to debug and provides recommendations (reduce costs and increase performance) and in the future will be integrated with Datdog.


## How is our solution unique?

We abstract workflow creation to modular jobs, so they can be scaled and maintained independently. We use the GitHub actions marketplace to take advantage of the existing community. Our runners can execute these workflows at infrastructure cost, and not in billable time units as GitHub does. 

Our users manage costs (can save thousands of $) and control limits while ensuring compliance. For example, by executing workflows in their region or private networks and not wherever a GitHub runner relies. Our single dashboard consolidates metrics from multiple workflows in one space, in contrast to GitHub, so debugging becomes easier, especially with the help of AI. The copilot is the icing on the top, guiding users to compose and operate workflows by fitting modern UI/UX expectations.

## What is our software stack?

- Front-end: Typescript, Javascript, HTML, SCSS, NextJS, MUI, Zustand, ESLint, Prettier and Firebase and Docker.
- Back-end: GoLang, Echo, GORM, FAST API, Redis and PostgreSQL and Docker.
- Copilot: Python, OpenAI, Mistral, Langchain, Spacy.
- Infra: Kubernetes clusters on AWS and GCP.
- Integrations: GitHub, GitLab, Cloudflare, Google.