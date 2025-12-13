# CONTRIBUTING

You can add sample sources of document generators to this repository. Please follow the flow and editing convention.

## Basically workflow

1. Make an issue of edit description
2. Fork this repository and edit source with following these conventions
3. Make a pull request with linking target issue
4. [aKuad](https://github.com/aKuad) will check and approve the pull request

## Editing conventions

### Source files

Put source files on `/<language-name>` or `/<generator-name>`.

- If the name has spaces, replace them to `-`
- If the name has capital characters, convert to `lowercase` or `snake-case`

The sample should contains all standard usages.

### Build workflow

Add a build workflow to `docs-build-deploy.yml`.

1. Make a job `jobs.build-<generator-name>`, what uploads an build files artifact
2. Add the job ID to `jobs.prepare-artifact.needs` list
3. Add a step `jobs.prepare-artifact.steps` to include build files to finally artifact `github-pages`

### Add a link to index

Add a link to `general-index/index.md` to the generated document, like below:

```md
## [<Generator Name>](<generator-name>/index.html)

Light description
```
