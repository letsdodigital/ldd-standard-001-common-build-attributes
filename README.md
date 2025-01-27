# ldd-standard-001-common-build-attributes

A standard that all modern digital healthcare apps should stand to.

Currently building this standard, but here are some initial thoughts:

1. Web first.
2. Backend - python with django (framework), poetry (package management) / black (formatter) / bandit (security) / mypy (typing).
3. Frontend - typescript with react (framework) npm/yarn (package management) / eslint (linter) / prettier (formatter).
4. Git version control.
5. Authentication and authorisation.
6. Configurable pathways (for the disease / company wanting the app).
7. DevSecRegOps (Development Security Regulation and Operations) are the core.
8. Full unit testing and integration testing.
9. Interoperability with other systems - perhaps we will use openEHR (or FHIR).
10. Documentation in code (docstrings and typedoc).
11. Typing (mypy).
12. Cybersecurity (black)
13. Open source all the way baby.

## Other considerations

1. CI/CD
2. OSS licence (MIT)
3. Code of conduct
4. Contributing guidelines
5. Issue templates
6. Pull request templates
7. Security policy
8. The software buyer owns the open source licence (MIT preferred), but Let's Do Digital house the code on Github.
9. Potentially ReactNative for mobile first devices.
10. Perhaps a developer portal or marketplace for modules
11. We need a PR equivalent clinical safety sign off process (ask someone else who was not involved in the code to review it).
