# CollabMatch

**Discover talent. Share your work. Collaborate within your community.**

A project by **Team Huskers** for the **Best Build for Food & Workspaces** challenge, focusing on shared workspaces and communities.

## Project video

[Watch the project demo on Instagram](https://www.instagram.com/reel/DeoXLm8smNt/?obrf=MW5sMW1oZWhlZWNyNA==)

## The problem

People and businesses can share a workspace without knowing who has the skills, experience, or availability to help them. Finding a designer, developer, marketer, or project partner often depends on asking around.

## Our idea

CollabMatch is a community website where members showcase their work, companies publish collaboration needs, and an open-weight AI assistant helps identify relevant people within the workspace.

## Planned pages and features

- **Home:** community updates, active promotional posts, recent requests, and upcoming events.
- **Members and companies:** profiles with skills, experience, availability, projects, optional GitHub/LinkedIn/portfolio links, help offered, and help needed.
- **AI Match:** describe a need in everyday language and receive up to three suitable members with explanations grounded in their profiles.
- **Requests:** create, browse, and close requests for help or collaboration.
- **Connections:** send in-app invitations, accept or decline them, and propose a meeting.
- **Community spotlight:** promote a business, service, or project for 24 hours.
- **Events:** publish community events, RSVP, and cancel an RSVP.

## What the AI does

For example, a perfume company might ask: "We need someone to design Instagram posts for our product launch."

The proposed workflow is:

1. Retrieve eligible member profiles from MongoDB.
2. Send relevant profile summaries and the request to an open-weight Qwen model through Ollama.
3. Identify suitable collaborators and explain the relevant profile evidence.
4. Validate returned member IDs and display the suggestions.
5. Let the requester authorise invitations; let recipients accept or decline.

The AI interprets and recommends. Application code controls eligibility, invitation delivery, and access to conversations. Profiles supply context; the model does not need to be retrained on community members.

## Proposed prototype technology

- **MongoDB:** persistent profiles, companies, requests, invitations, promotions, and events.
- **Ollama with Qwen3-4B:** local open-weight AI matching, with the model configurable.
- **Website framework:** to be documented once the application code is uploaded.

For the small demonstration dataset, eligible profile summaries can be provided directly to the model without a vector database. Local Ollama must be reachable from the application's backend; a public deployment requires a separately reachable inference service.

## Prototype scope

The initial target is a complete profile → request → AI match → invitation → acceptance flow. A clearly labelled demo account switcher and fictional profiles may be used in place of production authentication.

## Repository status

At the time this README was added, the repository contained a license but no application source code. The features and technology above describe the intended prototype; their implementation has not been verified from this repository. Startup commands and completed-feature status should be added after the code is pushed.

## Data and configuration

Use fictional or approved demonstration data. Keep MongoDB connection strings, passwords, API keys, and real environment files out of Git. Commit only placeholder environment examples. Real member data and private conversations must not be included in the public repository.

## License

See [LICENSE](LICENSE) for the repository's license. Model and dependency licences apply separately.
