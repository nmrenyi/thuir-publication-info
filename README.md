# THUIR Publication Collection Info
## Overview
These days we've been working on constructing a website for THUIR. Here's the [demo](https://thuir.github.io/lab-website-template/) of the website.

Now we're working on the publication collection, which needs everyone to submit their publication list in a pre-defined manner, if any. A demo for publication page is available [here](https://thuir.github.io/lab-website-template/publications/). 

![publication-illustration](_fig/publication-illustration.jpeg)

The image above shows the basic layout of the publication page. Publications are categorizd by year, descendingly. Each publication is represented by a block, which contains the following components:
1. Title
2. Author List
3. Conference/Journal
4. Publication Date
5. Tags
6. Other Links (like GitHub link to your paper code, website for your paper, etc.)
7. Picture of your paper (a model screenshot or any picture you like)

Although seven parts are displayed in this block, we do not need to fill them all. Actually, the minimal requirement for each paper is only the DOI of the paper. Other information, like tags, links and pictures are optional (but recommended if possible). Steps to submit publication info is illustrated in the following section.

## Submission Guide
To ensure convenience of both fellows and website maintainers, we decide to use **Pull Request** to submit publication info. Pull Request is a powerful feature of GitHub collaboration. If you are not familiar with it, Google must be your strong backup! 

Here are some basic steps to submit your publication info:

1. Fork this repository to your own GitHub account.
2. Add your own YAML file with your publication information in it.
3. Commit and push your changes to your own repository.
4. Raise a Pull Request to this repository.
5. Wait for the maintainers to review your PR(Pull Request). If everything goes well, your PR will be merged into the master branch. Otherwise, the maintainer will reject your PR and you will be notified to make some changes.

## YAML File for Publication Info
Here is an example of YAML file for publication info:
```yaml
- id: doi:10.1016/j.csbj.2020.05.017
  image: https://ars.els-cdn.com/content/image/1-s2.0-S2001037020302804-gr1.jpg
  date: 2020-6-2
  extra-links:
    - type: manubot
      link: https://greenelab.github.io/knowledge-graph-review/
  tags:
    - knowledge graphs

- id: doi:10.1371/journal.pcbi.1007128
  image: https://journals.plos.org/ploscompbiol/article/figure/image?size=inline&id=info:doi/10.1371/journal.pcbi.1007128.g001&rev=2
  repo: greenelab/meta-review
  extra-links:
    - type: manubot
      link: https://greenelab.github.io/meta-review/
    - type: source
      link: https://github.com/greenelab/meta-review
    - type: website
      link: http://manubot.org/

- id: doi:10.7554/eLife.32822
  image: https://iiif.elifesciences.org/lax:32822%2Felife-32822-fig8-v3.tif/full/863,/0/default.webp
  extra-links:
    - type: preprint
      link: https://doi.org/10.7287/peerj.preprints.3100v1
    - type: manubot
      link: https://greenelab.github.io/scihub-manuscript/
    - type: source
      link: https://github.com/greenelab/scihub-manuscript
      text: Manuscript source
    - type: source
      link: https://github.com/greenelab/scihub
      text: Analyses source

```
This example could be accessed at [TODO](). The ONLY compulsory item is the `id` field, which is the DOI of your paper. Other fields are optional. Some fields, however, are recommended, if possible. `image` is recommended, since it will be displayed in the publication block.

A recommended template for a single paper is as follows:
```yaml
- id: doi:10.1371/journal.pcbi.1007128  # compulsory
  image: https://journals.plos.org/ploscompbiol/article/figure/image?size=inline&id=info:doi/10.1371/journal.pcbi.1007128.g001&rev=2  # optional, but recommended
  repo: greenelab/meta-review  # optional, but recommended, stands for https://github.com/greenelab/meta-review

```

## QA


