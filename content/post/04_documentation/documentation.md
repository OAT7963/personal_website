---
author: "Hugo Authors"
title: "Documentation"
date: "2019-03-08"
description: "A brief guide to setup KaTeX"
images: ["images/documentation.jpg"]

categories: 
  - Documentation
---

## Importance of Technical Documentation

Technical documentation is essential in any tech project as it provides users and stakeholders with a detailed understanding of the product's functionality. It also serves as a guide for developers and maintainers, reducing the onboarding time and ensuring consistency in product development and troubleshooting. It plays a vital role in communication among teams, facilitating better collaboration and efficiency.

- Technical documentation provides a detailed understanding of product functionality.
- It guides developers and maintainers, reducing onboarding time.
- Ensures consistency in product development and troubleshooting.
- Facilitates better team communication and collaboration.

## Role of Non-Technical Documentation

Non-technical documentation is equally important as it communicates the project's purpose, goals, and strategies to non-technical stakeholders. It may include project proposals, marketing materials, user manuals, and other organizational documents. It helps to ensure that everyone involved in the project, regardless of their technical expertise, understands and aligns with the project's objectives.

- Non-technical documentation communicates project's purpose, goals, and strategies to non-technical stakeholders.
- It may include project proposals, marketing materials, user manuals, etc.
- Helps everyone involved in the project understand and align with the project's objectives.

## Documentation as a Communication Tool

Both technical and non-technical documentation serve as crucial communication tools. Documentation provides a clear roadmap for the project, aids in decision-making, reduces ambiguity, and facilitates knowledge transfer. Regular updating and maintaining of documentation ensure it remains relevant and useful over the project's lifecycle.

- Documentation provides a clear roadmap for the project.
- Aids in decision-making and reduces ambiguity.
- Facilitates knowledge transfer.
- Documentation should be regularly updated and maintained.

<!-->
Mathematical notation in a Hugo project can be enabled by using third party JavaScript libraries.
more

In this example we will be using [KaTeX](https://katex.org/)

- Create a partial under `/layouts/partials/math.html`
- Within this partial reference the [Auto-render Extension](https://katex.org/docs/autorender.html) or host these scripts locally.
- Include the partial in your templates like so:  

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- To enable KaTex globally set the parameter `math` to `true` in a project's configuration
- To enable KaTex on a per page basis include the parameter `math: true` in content files

**Note:** Use the online reference of [Supported TeX Functions](https://katex.org/docs/supported.html)

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<!-- <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### Examples

{{< math.inline >}}
<p>
Inline math: \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
--> 