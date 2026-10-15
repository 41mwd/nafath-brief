Version: NAFATH-V3
Track: Networking

## Overview
The government AI assistant must provide citizens with clear and accurate answers about public services. The six IT fields work together to make this possible. Software engineering helps the team manage changes to the assistant’s API. AI can use Retrieval-Augmented Generation (RAG) to find trusted information before preparing an answer. Mobile security protects the connection between the app and its servers. Networking supports communication between devices and provides enough IP addresses as use grows. Cybersecurity helps reduce attacks, while data protection reduces risks from stored chat logs. These parts should be planned and tested together. A correct AI answer is not enough if the connection is unsafe or personal data is exposed. Together, these choices help build a service citizens can trust.
## Software
Semantic Versioning (SemVer) helps teams explain changes to a public API using MAJOR.MINOR.PATCH numbers. Increase the MAJOR number when a change is not backward compatible and may break existing users. Increase MINOR when adding new features that remain backward compatible. Increase PATCH for backward-compatible bug fixes. For example, a breaking API change needs a major version increase, while a safe new feature may use a minor version increase. This makes updates easier to understand.

Resource: Semantic Versioning 2.0.0 - https://semver.org/spec/v2.0.0.html
## AI
Retrieval-Augmented Generation (RAG) combines a language model with a search step. When a citizen asks a question, the system first retrieves relevant information from trusted documents, such as official service pages, and then uses that information to prepare an answer. This can help reduce incorrect answers because the model can use information instead of relying only on its stored knowledge. RAG does not guarantee correctness, so the assistant should use current sources and be tested for wrong or missing information.

Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401
## Mobile
App Transport Security (ATS) is an Apple platform feature that helps protect privacy and data integrity. It requires secure network connections using HTTPS and Transport Layer Security (TLS) when apps use the standard URL loading system. If an app tries to connect to a plain HTTP endpoint, ATS blocks the connection unless an exception is configured. These exceptions can reduce security, so the team should prefer fixing the server to support HTTPS instead of weakening the app’s protections.

Resource: Preventing Insecure Network Connections - https://developer.apple.com/documentation/security/preventing-insecure-network-connections
## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
