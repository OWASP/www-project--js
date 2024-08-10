# OWASP-js

The OWASP-js project is a repository for community contributions focused on enhancing security logging practices in Node.js applications. This project provides a standardized logging vocabulary and tools that adhere to OWASP's best security practices. The ultimate goal is to make it easier for developers to log security events consistently and securely in the TypeScript ecosystem.

## Contributing

We welcome contributions to expand and improve the OWASP-js project. This repository follows a [fork-and-pull model](https://docs.github.com/en/github/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model). Here's how you can contribute:

1. [Fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) this repository and [clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository) your fork.
1. Make your changes or additions in the appropriate directory (e.g., `src/` for code, `docs/` for documentation).
1. Push your changes to your fork and open a pull request against this repository.

If your changes address an [existing issue](https://github.com/OWASP/owasp-js/issues), please comment on the issue so it can be assigned to you. This helps prevent duplication of work.

### Creating New Content or Features

Go into the `pages` folder and create a new file.

Place the following front matter and `include` tag at the beginning of your file. Feel free to copy and edit this example:

```md
---
layout: col-sidebar
title: "My Page"
author: "My Name"
contributors: ["Additional Contributor Names", "If Any"]
permalink: /new-page
tags: ["logging", "security", "nodejs"]
---

{% include writers.html %}

Write your content here!
```

The fields `contributors`, `permalink`, and `tags` are optional. When in doubt, it's okay to leave them blank.

### Rules for Contributors

1. Your contribution must be original work. Do not submit copyrighted material you do not own, and avoid plagiarism.
1. Ensure that contributions are vendor-neutral and do not promote specific products.
