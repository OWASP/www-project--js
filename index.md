---

layout: col-sidebar
title: OWASP -js
tags: example-tag
level: 2
type: code
pitch: A very brief, one-line description of your project

---

Problem:

As a TypeScript Node.js developer, I've felt unguided while writing logging events. On every team I've worked on, developers logged whatever they wanted, when, and at any level they wanted. Logging is crucial to monitoring and alerting for security and sensitive application events, and the JavaScript ecosystem hasn't focused enough on it.

Solution:

Developers need clearly defined standard definitions for logs: what to log when to log, and what _not_ to log. Ideally, the same package, or a suite of packages, can be used in conjunction to implement the best security practices in the TypeScript ecosystem, as identified by OWASP.

This project's background:

A colleague stumbled upon the OWASP cheat sheet for logging vocabulary. I realized immediately that it was exactly what I was looking for. I started implementing the logging standards in our Node.js servers. During development, it became clear that looking up the logging events on the cheat sheet constantly was cumbersome. As most JavaScript developers do, I looked on GitHub to see if there was a package that satisfied my need to not deal with typos in the events (which can invalidate their usefulness for alerting) or look on the cheat sheet. (Un)fortunately, I found nothing, so I made the package that re-implemented the full set of OWASP logging vocabulary. When I went to publish the package, I was trying to come up with a cool name and, somehow, got the name `owasp`. I thought it was a mistake, but no, I got it. I knew immediately that I had to contact and collaborate with the OWASP organization.

### Road Map
The project will start with solidifying its stance as a well-defined and complete set of logging utilities:

* ✅ Implement the OWASP Cheat Sheet for Application Logging Vocabulary, a standard vocabulary for logging security events.
* Create a new project (will require another proposal) for an ESLint configuration to strictly enforce adding the `event` property with a value from the `owasp` library to logging events (`eslint-plugin-owasp` and/or `eslint-config-owasp`; both of which are currently not taken)

Next, I would like to review and talk to other OWASP and community members and identify gaps in Node.js application security.

Ultimately, I want the `owasp` package to be worthy of the namesake.

One idea is to eventually `owasp` a "re-exporting" package for other NPM packages owned by the OWASP organization.

* Get access to an OWASP NPM organization (@owasp is taken; OWASP needs to review if they can claim access or if they can get another org name)
* Create a package `@owasp/vocabulary`
* Move the code currently in `owasp` to `@owasp/vocabulary`
* Make the `owasp` package export the contents from `@owasp/vocabulary` and other related security packages using subpath exports [https://nodejs.org/api/packages.html#subpath-exports|https://nodejs.org/api/packages.html#subpath-exports]. Developers can `npm install owasp` and get a suite of useful JavaScript utilities by using any of the subpath exports. Here's an example:

```

import { authn_login_successafterfail } from 'owasp/vocabulary';  // a re-export of `@owasp/vocabulary`
import { openPopup } from 'owasp/dom'; // a re-export of `@owasp/dom`
```

Alternatively, developers can choose to install each package individually if they know that they only need or want a subset of the packages.

These packages could live in a monorepo in the OWASP organization, perhaps `github.com/owasp/owasp-js`. I have several years of experience managing and publishing complicated TypeScript monorepos.
