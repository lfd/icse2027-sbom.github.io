---
layout: default
title: Home
---

# Beyond a Bill: Tracing, Mining and Assessing Packages in the Debian Ecosystem

Supplementary Website

## Abstract

This study proposes and evaluates an SBOM analysis tool for the Debian
ecosystem. The tool traces packages to their packaging and project
repositories, mines and fuses their development history and code, and
annotates the SBOM dependency graph with maintenance and quality indicators.
Across three Debian releases, we analyse these indicators and combine them
into a package attention score to prioritise packages for quality assurance
review.

## Study repository

Visit our [git repository](https://github.com/lfd/icse2027-sbom) to get a copy
of the reproduction setup, including the tool and all scripts for data
extraction, analysis and visualisation.

## Annotated dependency graphs

- Debian Trixie: [attention score]({{ site.baseurl }}/graphs/trixie-score.html), [rule]({{ site.baseurl }}/graphs/trixie-rule.html)
- Debian Bookworm: [attention score]({{ site.baseurl }}/graphs/bookworm-score.html), [rule]({{ site.baseurl }}/graphs/bookworm-rule.html)

## Candidate metrics

The table of candidate metrics, with references to the literature, can be found [here]({{ site.baseurl }}/metrics/).
