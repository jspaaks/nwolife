# NWOLife2021 notes

## Pitch

1. The software citation workshop will cover the two sides of software citation:
    1. supplying metadata
    1. archiving a copy of the software, get a persistent identifier
1. You can do either of these by hand, but most of it can be automated
1. I will demonstrate some existing tools and services that can help you simplify this process
1. The demonstration assumes you are somewhat familiar with github
1. For those who can't attend: https://fair-software.nl

## Workshop

### Preparations

1. assert zenodo sandbox permissions have been revoked (here https://github.com/settings/applications)
1. assert logged out of sandbox.zenodo.org (here https://sandbox.zenodo.org/)
1. assert a test repository in jspaaks org exists (here https://github.com/jspaaks/nwolife)
    - has branch with README.md with plaintext instructions on how to cite (https://github.com/jspaaks/nwolife/tree/ye-old-style)
    - has branch with CITATION file (https://github.com/jspaaks/nwolife/tree/wilson)
    - main branch is where we will add CITATION.cff file

### Why cite software?

1. Helps reproducibility
1. Helps build a culture of giving developers credit for their work, in turn improves 
    - the time developers can spend on developing and maintaining software
    - the quality of the software

### Job 1: add machine readable citation metadata

1. Inspect ye-old-style branch
1. Inspect wilson branch
1. Let's use [cffinit](https://bit.ly/cffinit) to make the repo's citation metadata machine-readable with a [Citation File Format](https://citation-file-format.github.io/) file 
    - Helps integration with other tools, services, websites, search engines (e.g. research software.nl, schema.org)

### Job 2: Making a release on GitHub

1. Release without storing a snapshot on Zenodo (here https://github.com/jspaaks/nwolife/releases/new)
    - maybe need to explain semver / semantic versioning (here https://semver.org/)

### Job 3: GitHub-Zenodo integration

1. let's release contents of main branch on sandbox.zenodo.org
1. sandbox.zenodo.org, log in with github, enable app
1. https://github.com/settings/applications now shows sandbox
1. make release on GitHub
1. check zenodo sandbox
1. looks nice, but some things could be better:
    - orcids
    - set of contributors &neq; set of authors
    - name of the tool
    - license
    - keywords

### Job 4: cffconvert and GitHub Actions

1. let's use machine-readability to generate some metadata in a format that zenodo understands
    - cffconvert github action (here https://github.com/marketplace/actions/cffconvert)
1. make a new release on GitHub
1. check the result on sandbox.zenodo.org

### Other resources

- https://guide.esciencecenter.nl/#/citable_software/making_software_citable
- https://pypi.org/project/cffconvert/
- https://fair-software.nl/
- https://citation-file-format.github.io/


