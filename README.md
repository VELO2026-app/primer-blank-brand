# primer-blank-brand

A brand for an instance of
[primer-blank](https://github.com/inzoddwetrust/primer-blank): its skin and its
texts in one repository, one tag for both. The deploy machine `pridem` takes
each part by its directory -- `subpath` of the passport -- at the same tag:

```yaml
packages:
  skin:  { repo: git@github.com:<owner>/primer-blank-brand.git, version: 1.0.0, subpath: skin }
  texts: { repo: git@github.com:<owner>/primer-blank-brand.git, version: 1.0.0, subpath: texts }
```

```
skin/primer-package.yaml     schema: 1, contract: "1.0"
skin/tokens/*.tokens.json    W3C DTCG tokens: magenta, Georgia
skin/assets/logo.svg
texts/primer-package.yaml    schema: 1, contract: "1.0"
texts/ui/en.json             the brand's English texts: two of three
texts/ui/ru.json             Russian: only the title
```

Each part is a package of its own, with its own `primer-package.yaml`, in the
format of `primer-blank-skin` and `primer-blank-texts`, published by the same
owner as this repository (their READMEs give it). The difference is the
version: here one tag moves the look and the texts together; the two separate
repositories release each slot on its own.

Releases are tags `vX.Y.Z`; a released tag is never moved.
