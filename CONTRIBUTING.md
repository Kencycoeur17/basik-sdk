# Contributing to Bazik SDK

Thank you for considering a contribution to this **unofficial** JavaScript SDK for the Bazik API.

## Before opening a pull request

1. Search existing issues and pull requests for related work.
2. Open an issue to discuss larger API or behavior changes.
3. Fork the repository and create a focused branch.
4. Add or update tests for any behavioral change.
5. Run `npm test` locally (Node.js 18 or newer).
6. Open a pull request describing the change, tests and compatibility considerations.

## Security and financial integrations

- **Never commit real credentials**, access tokens, customer data, payment references tied to real users, or production webhook payloads.
- Use synthetic credentials and mocked API responses in tests and examples.
- Do not send real payments or transfers when running tests.
- Treat API responses and payment status as untrusted until verified server-side.
- Avoid logging secrets or personally identifiable information.
- Report potential credential leaks privately to the maintainer rather than publishing the secret in an issue.

## Review standards

Keep changes small and backward-compatible when possible. Document breaking changes and update README examples when behavior changes. A pull request is not guaranteed to be accepted.

## Attribution

Preserve the repository's MIT license and existing attribution. This is an unofficial integration, not an endorsement by Bazik or its payment providers.
