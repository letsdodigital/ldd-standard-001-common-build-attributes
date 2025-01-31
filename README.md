# ldd-standard-001-common-build-attributes

A standard that all modern digital healthcare apps should stand to. Initial thoughts on the base module model can be found [here](https://letsdodigital.org/posts/2025-01-30-do-you-what-to-build-a-health-app/).

Currently building this standard, but here are some initial thoughts:

![A possible stack](/media/django-react.png)

1. Web first.
2. Backend - python with django (framework), poetry (package management) / black (formatter) / bandit (security) / mypy (typing).
3. Frontend - typescript with react (framework) npm/yarn (package management) / eslint (linter) / prettier (formatter).
4. Git version control.
5. Authentication and authorisation.
6. Configurable pathways (for the disease / company wanting the app).
7. DevSecRegOps (Development Security Regulation and Operations) at the core.
8. Full unit testing and integration testing.
9. Interoperability with other systems - perhaps we will use openEHR (or FHIR).
10. Documentation in code (docstrings and typedoc).
11. Typing (mypy).
12. Cybersecurity (black).
13. A theming framework (eg Semantic UI / Bootstrap).
14. Open source all the way baby.

## Other considerations

1. Build a community around the base and modules
2. CI/CD
3. OSS licence (MIT)
4. Code of conduct
5. Contributing guidelines
6. Issue templates
7. Pull request templates
8. An external clinical safety sign off process
9. Security policy
10. The software buyer owns the open source licence (MIT preferred), but Let's Do Digital house the code on Github.
11. Potentially ReactNative for mobile first devices.
12. Perhaps a developer portal or marketplace for modules
13. We need a PR equivalent clinical safety sign off process (ask someone else who was not involved in the code to review it).

## Other stack possibilities

- To separate data access further from the frontend, a database(or other)/django(or fastAPI)/Nextjs/React.typescript stack could be used.

![2nd possible stack](/media/django-react-react.png)

## Notes

- We would like to build a system that enables people will less programming skills to pick up, tinker with and use. This means we have to separate the more complex components of the system into the base. The modules that are added as needed on top of this give the end-user (clinician, admin person or patient/family member) the functionality that they need.
- It would be nice to only have one computer language to learn, but we have highlighed some issues with this. Firstly, common practice is to have a javascript/typescript frontend, and a separate language for this backend. Python is fairly popular for the backend. There are of course some frameworks that utilise a single language across the frontend and backend, but these are not as popular and may not be as well supported. Furthermore, there is a powerful argument to be had that in utilising two separate languages, one for the frontend and one for the backend, you then separate the concerns of the frontend and backend. This can enable better security of data, as the frontend is not able to access the backend directly.

### Base module

- The base module will house as much of the complexities of the platform as possible. Where possible, it will abstract away:
  - Authentication and authorisation
  - DevSecRegOps
  - Interoperability
  - Data storage
  - Documentation
  - Typing
  - Cybersecurity

### Module

- A module will be a standalone piece of functionality that can be added to the base module. It will be a self-contained piece of code that can be added to the base module to give the end-user the functionality that they need. Digital healthcare app functionalities range vastly in number and complexity, but a list of modules could include:

1. ePROMS (electronic patient reported outcome measures)
2. Clinician / admin facing CDSS (clinician decision support systems)
3. Patient facing CDSS
4. Medical note taking
5. PAS (patient administration system) for clinic and bed management.
6. LIMS - for labs
7. PACS for imaging
8. Requests and referrals
9. ePMA for prescribing
10. Messaging system (clinician-admin-patient)

## Logo

Potential logo idea

<img src="/media/logo.png" alt="Logo" style="max-height: 100px;">
