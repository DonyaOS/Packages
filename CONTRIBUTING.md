# Contributing

We use `markdownlint` to lint the Markdown. From the root folder run:

```
markdownlint '**/*.md' --ignore node_modules --config .github/.markdownlint.yml
```

We also lint the YAML files with `yamllint`. From the root folder run:

```
yamllint -c .github/.yamllint .
```

<https://www.npmjs.com/package/markdownlint-cli>
<https://yamllint.readthedocs.io/en/stable/>
