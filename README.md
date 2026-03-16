# YAML ADRs (YADR)

[YAML](https://en.wikipedia.org/wiki/YAML) is a human-friendly, programming language-independent data serialization language; it is commonly used for configuration files. Its human-friendliness makes YAML suited for the capturing [Architectural Decisions](https://en.wikipedia.org/wiki/Architectural_decision) in [Architecture Decision Records (ADRs)](https://github.com/joelparkerhenderson/architecture-decision-record) as well.

This repository provides YAML ADR templates and examples.

## Content overview

* [YAML port of the Markdown Architectural Decisions (MADR) template](templates/yadr-template-full.yaml), as well as a [usage example](examples/use-yaml-as-adr-syntax.yaml) for it.
  * [Bare version of the YADR template](templates/yadr-template-bare.yaml) and shortened [usage example](examples/yaml-as-additional-syntax-for-madr.yaml).
  * [JSON conversions](examples-validation) of the YADR usage examples validate against the [JSON schema](schemas/yadr-schema.json)[^1] for the template.[^2]
* The folder [other YAML templates](templates/other-yaml-templates/) contains YAML ports of templates not originating from the MADR project, for instance, the [Y-Statement](https://medium.com/olzzio/y-statements-10eb07b5a177) template.
  * An [example](examples/other-yaml-templates/yaml-as-additional-y-statement-syntax.yaml) and two corresponding [JSON conversions](examples-validation/other-yaml-templates/) are available as well.

[^1]: Note that this schema has been designed to validate all array elements, which requires the type definitions of the array elements to be scalar. See answer 1 to the question ["How do I make a jsonschema so that it validates all objects in array?"](https://stackoverflow.com/questions/49319692/how-do-i-make-a-jsonschema-so-that-it-validates-all-objects-in-array) on Stack Overflow for rationale.

[^2]: The template contains a placeholder `id-of-option-1` for the option name in its `pros-and-cons-of-the-options` object. The JSON schema [contains an `additionalProperties` object](https://stackoverflow.com/a/62242833/873282) so that options pros and cons are validated properly.

## Background information and tools

* Homepage of the [ADR organization on GitHub](https://adr.github.io/)
* [Markdown ADR (MADR)](https://adr.github.io/madr/) project with four variants of the [MADR template](https://github.com/adr/madr/tree/develop/template) versions (minimal and full, bare and commented with usage instructions) <!-- note that the minimal template has not been ported to YAML/YADR yet. -->
* Olaf Zimmermann blogs about [architectural decision making and capturing](https://ozimmer.ch/tags/#architectural-decisions):
  * Patterns and anti patterns for [ADR creation](https://ozimmer.ch/practices/2023/04/03/ADRCreation.html)
  * Architectural decision making [fallacies and biases](https://ozimmer.ch/practices/2025/09/01/ADMFallacies.html)
  * ["The Markdown ADR (MADR) Template Explained and Distilled"](https://ozimmer.ch/practices/2022/11/22/MADRTemplatePrimer.html)
* YAML: [YAML homepage](https://yaml.org/), [YAML specification](https://yaml.org/spec/1.2.2/) and [YAML best practices](https://yamlscript.org/blog/2025-07-20/yaml-best-practices/)
* One of many online [JSON schema validators](https://www.jsonschemavalidator.net/) and a sample [YAML to JSON converter](https://openreplay.com/tools/json-yaml/)
