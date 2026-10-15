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
IPv4 uses 32-bit IP addresses, while IPv6 uses 128-bit addresses. This gives IPv6 a much larger address space and helps support the growing number of phones, sensors, computers, and other connected devices. In a government service, IPv6 can help the network support more connected devices as use grows. However, IPv6 does not automatically make every connection faster. Speed also depends on network design, routing, servers, and the user’s connection. The system should be tested on IPv4 and IPv6 where needed.

Resource: RFC 4291: IP Version 6 Addressing Architecture - https://www.rfc-editor.org/rfc/rfc4291
## Cybersecurity
Prompt injection happens when someone gives a large language model instructions that try to change its intended behavior. Direct prompt injection comes from a user’s own input. Indirect prompt injection can be hidden in outside content, such as a webpage or file the assistant reads. To reduce the risk, the team should treat outside content as untrusted and keep it separate from system instructions. It should also limit the assistant’s tool permissions and test inputs and outputs for unsafe behavior.

Resource: LLM01: Prompt Injection - https://genai.owasp.org/llmrisk2023-24/llm01-24-prompt-injection/
## Data
When storing chat logs, anonymization means changing information so a person can no longer be identified. Pseudonymization replaces direct identifiers with a code, but extra information may still link the record back to a person. Under the GDPR, pseudonymized data can still be personal data, while truly anonymous information is outside the Regulation’s scope. The service should collect only needed log data, restrict access, set a retention period, and protect any key that links codes to people.

Resource: Regulation (EU) 2016/679 (General Data Protection Regulation) - https://eur-lex.europa.eu/eli/reg/2016/679/oj
## Misconception in My Track
A common misconception is that IPv6 addresses are still 32 bits, just like IPv4, but written in a different format. In fact, IPv6 addresses are 128-bit identifiers, which gives IPv6 a much larger address space than IPv4. This matters because more connected devices need IP addresses as technology grows. The difference is about address size, not a promise of faster internet. Section 2, “IPv6 Addressing,” in RFC 4291 states that IPv6 addresses are 128-bit identifiers for interfaces and sets of interfaces.
## Open Question
How should the government app support IPv4 and IPv6 during the transition while keeping connections secure and ensuring that citizens using older networks can still reach the service?
