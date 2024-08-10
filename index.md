---
layout: col-sidebar
title: OWASP-js
tags: owasp, logging, nodejs, javascript, typescript, security
level: 2
type: code
pitch: Follow OWASP's application security best practices for Node.js applications.
---

### Problem

As a TypeScript Node.js developer, I have often found logging practices to be inconsistent and unguided. In every team I've worked with, developers logged information without clear standards—logging whatever they wanted, whenever they wanted, and at any level they chose. Effective logging is crucial for monitoring, alerting, and securing applications, yet the JavaScript ecosystem lacks a cohesive approach to this.

### Solution

Developers need a standardized approach to logging: clear definitions of what to log, at what level, when to log, and, crucially, what not to log. This project offers a solution by providing a set of logging `event` definitions that adhere to OWASP's best security practices, tailored specifically for the TypeScript ecosystem.

### Project Background

A colleague stumbled upon the OWASP cheat sheet for logging vocab. I started implementing the logging standards in our Node.js servers. During development, it became clear that looking up the logging events on the cheat sheet constantly was cumbersome. As most JavaScript developers do, I looked on GitHub to see if there was a package that satisfied my need to not deal with typos in the events (which can invalidate their usefulness for alerting) or look on the cheat sheet. (Un)fortunately, I found nothing, so I made the package that re-implemented the full set of OWASP logging vocab. When I went to publish the package, I was trying to come up with a cool name and, somehow, got the name `owasp`. I thought it was a mistake, but no, I got it. I knew immediately that I had to contact and collaborate with the OWASP organization.

The idea for this project began when a colleague introduced me to the OWASP Logging Cheat Sheet. Implementing these standards in our Node.js servers highlighted how cumbersome it was to continually reference the cheat sheet. To mitigate this overhead, we created a package that fully implements the OWASP logging vocabulary, minimizing errors and improving efficiency.

### Roadmap

The project is currently focused on establishing itself as a comprehensive set of logging utilities, with the following milestones:

- ✅ **Implementation**: Complete the OWASP Logging Cheat Sheet vocabulary, providing a standardized set of terms for logging security events.
- **ESLint Integration**: Propose and develop an ESLint plugin/configuration to enforce the use of OWASP vocabulary in logging events. This will ensure consistency and adherence to best practices across projects.

## Future Vision

The goal is to expand this project into a broader security toolkit for Node.js developers, aligned with OWASP's mission. This includes:

- **Community Collaboration**: Engage with OWASP and the wider community to identify gaps in Node.js application security and address them through additional tools and libraries.

```ts
import { authn_login_successafterfail } from "owasp/vocab"; // a re-export of `@owasp/vocab`
import { openPopup } from "owasp/dom"; // a re-export of `@owasp/dom`
```

Ultimately, this project aims to provide a robust and secure logging solution for Node.js developers, worthy of the OWASP name.
