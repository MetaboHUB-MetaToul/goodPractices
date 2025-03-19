# Good practices for MetaToul bioinformatics project

The aim of this document is to list the best practices to be followed when creating and monitoring a bioinformatics project in MetaToul.

They are listed in order of importance and difficulty of implementation.

## MetaToul bioinformatics referent

If the person in charge of the new development is not a senior developer, and the person in charge is neither a computer scientist nor a bioinformatician, it is necessary to choose a referent from among MetaToul's permanent bioinformaticians. Code review sessions can be organized between the new developer and the permanent member to ensure that the code produced meets the standards of any IT project.

## Inscription to the communication tools for MetaToul developers

Questions can be adressed to two levels:
- MetaToul slack platform
- MetaboHub slack platform

The new developer's manager must ensure that he/she is registered on these 2 platforms.

## Creation of a git repository

In the case of a completely new development, the first step is to create a git repository in the forge that you use in your institute (INRAE forge, github, etc...). It is important that the git project is registered in a github or gitlab group belonging to the project managers.

In the case of non-permanent developer, it's crucial that the repo is available to his/her supervisors.

## Protection of the existing code

When the new developer mission is to add features to an existing software or library, it's crucial to protect the existing code. First, the main branch must be protected so that only merge can change it. Second, each new feature must be handled by a merge request. This allows to make easier the code reviews with the bioinformatics referent, to keep the history of the development and to keep safe the other parts of the code.

## Versioning

The new developer needs to train himself/herself and use the tools specific to git and the language with which he develops to give a version number to each stable version of his code. This enables better tracking of code and ensures reproducibility of analyses by indicating the software version used.

## Documentation

### Creation of a README.md file

The repo must contain at least a README.md file that contains a title, a synopsis and a detailed documentation.

A lot of README.md templates exist (e.g. <https://www.readme-templates.com/>), it's also possible to generate one when you create a new repo in gitlab or github.

### Developer documentation

The code must be commented in english and must follow the language-dependent format required to generate automatic documentation.

### User documentation

The user documentation must be written in english and must integrate examples of how to use the software.

## Tests

In an IT project, there are essentially two types of test.

- Unit tests focus on testing individual components (e.g. methods, classes) of a software product.
- Functional tests aim to test the functionality of an entire application

Librairies computing the proportion of the code covered by tests allow to evaluate the right implementation of the tests.

**The minimum requirement is to provide a set of test data so that the user or new developer can make sure that the library or software works properly.**

## Containerization

IT developments often require a lot of dependencies, which are difficult to trace or install in certain environments.
To ensure that software can be used long after it has been developed, and for reasons of reproducibility, it is necessary to create a container to run it. A container contains the OS and all the libraries required to run the software. [Docker](https://www.docker.com/) and [Singularity](https://sylabs.io/singularity/) are currently the most widely used containerization systems at MetaToul.

## Mirror on github MetaToul organisation

When the software is usable and well packaged, a mirror to the [github Metatoul organisation](https://github.com/orgs/MetaboHUB-MetaToul) has to be set up.

## Links

- <a href="https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1009823#sec002" target="_blank">Ten simple rules for making a software tool workflow-ready</a>
- <a href="https://hal.science/hal-02083801/document" target="_blank">Je code : Les bonnes pratiques de développement logiciel</a>

