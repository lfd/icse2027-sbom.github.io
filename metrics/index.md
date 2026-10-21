---
layout: default
title: Candidate metrics
---

# Candidate metrics

Hypothetical risk criteria identified by Siemens (S) and metrics from empirical
software engineering literature (Ref.) related to them, and whether they are
implemented by our tool (Impl.).

## Active maintenance

| Metric | Ref. | Description | Impl. |
|--------|------|-------------|:-----:|
| Commits | S, \[[1](#ref-1), [2](#ref-2)\] | # Commits | ✓ |
| Churn | \[[3](#ref-3), [2](#ref-2)\] | # Added and deleted lines | ✓ |
| Function growth | \[[1](#ref-1)\] | # Newly added functions | ✓ |
| Developers | \[[2](#ref-2), [4](#ref-4)\] | # Active developers | ✓ |
| Newcomers | \[[5](#ref-5)\] | # Developers who joined the project (module) | ✓ |
| Newcomers ratio | \[[5](#ref-5)\] | Proportion of developers who joined the project (module) in two consecutive time intervals | ✓ |
| (Core) stayers | \[[5](#ref-5)\] | # (Core) developers who stayed active in the project (module) across two consecutive time intervals | ✓ |
| Stayers ratio | \[[5](#ref-5)\] | Proportion of (core) stayers across two consecutive time intervals | ✓ |
| (Core) leavers | \[[5](#ref-5)\] | # (Core) developers who contributed to the project (module) in the prior but not the latest time interval | ✓ |
| Leavers ratio | \[[5](#ref-5)\] | Proportion of (core) leavers across two consecutive time intervals | ✓ |
| Bus factor | S, \[[6](#ref-6), [7](#ref-7), [8](#ref-8), [9](#ref-9)\] | # Developers who are knowledgeable of a subset of at least *y*% of the codebase based on file or line ownership | – |
| Pony factor | \[[10](#ref-10)\] | Approximation of the bus factor based on developer contributions (e.g. commits) | ✓ |
| Social smells | \[[2](#ref-2)\] | Patterns for sub-optimal social behaviours (e.g. radio silence, missing link, organisational silo) | – |
| Open issues | \[[11](#ref-11)\] | # Open GitHub issues | – |
| Closed issues | \[[11](#ref-11)\] | # Closed GitHub issues | – |
| Funding | S, \[[12](#ref-12), [13](#ref-13), [14](#ref-14)\] | Investment in OSS projects by companies (paid developers) | – |

## Complexity

| Metric | Ref. | Description | Impl. |
|--------|------|-------------|:-----:|
| Lines of code (LoC) | \[[1](#ref-1), [15](#ref-15), [16](#ref-16), [17](#ref-17), [18](#ref-18)\] | # LoC in the project | ✓ |
| Lines of code density | \[[15](#ref-15)\] | Lines of code per entity, e.g. function | ✓ |
| Churn | \[[1](#ref-1), [19](#ref-19)\] | # Added and deleted lines | ✓ |
| Churn density | | Churn per entity, e.g. function | ✓ |
| Files | \[[1](#ref-1)\] | # Files in the project | ✓ |
| Modules | \[[15](#ref-15)\] | # Modules in the project | – |
| Functions | \[[1](#ref-1)\] | # Functions in the project | ✓ |
| Parameter count | \[[15](#ref-15)\] | # Parameters per function | – |
| Tokens | \[[1](#ref-1)\] | # Tokens in the project | ✓ |
| Cyclomatic complexity / McCabe | \[[15](#ref-15), [19](#ref-19), [18](#ref-18)\] | # Linearly independent paths in the program control flow graph | ✓ |
| Cyclomatic complexity density | \[[18](#ref-18), [17](#ref-17)\] | Cyclomatic complexity per entity, e.g. function | ✓ |
| Halstead effort | \[[1](#ref-1), [19](#ref-19)\] | Effort to create or maintain a program based on operators and operands | – |
| Cognitive complexity | \[[20](#ref-20), [21](#ref-21)\] | Understandability rating of code structures | – |
| Cognitive complexity density | \[[16](#ref-16)\] | Cognitive complexity per entity, e.g. LoC | – |
| Weighted methods per class (WMC) | \[[19](#ref-19), [22](#ref-22), [17](#ref-17)\] | Sum of complexities of all methods in a class | – |
| Response for a class (RFC) | \[[19](#ref-19), [22](#ref-22), [17](#ref-17)\] | # Methods invokable in response to a message to an object of the class | – |
| Number of methods (NOM) | \[[15](#ref-15), [17](#ref-17)\] | # Methods in a class | – |
| Number of children (NOC) | \[[19](#ref-19), [17](#ref-17)\] | # Immediate descendants in the inheritance tree | – |
| Lack of cohesion in methods (LCOM) | \[[19](#ref-19), [22](#ref-22), [17](#ref-17)\] | Difference between # method pairs sharing no instance variables and # method pairs sharing at least one | – |
| Coupling between objects (CBO) | \[[19](#ref-19), [22](#ref-22), [17](#ref-17)\] | # Other classes a class is coupled to, e.g. via method calls, inheritance or arguments | – |
| Depth of inheritance tree (DIT) | \[[19](#ref-19), [17](#ref-17)\] | # Inheritance levels between the root node and the node of interest | – |
| Dependencies | \[[15](#ref-15)\] | # Outgoing edges of an entity (e.g. module) in the dependency graph | – |
| Fan-in | \[[15](#ref-15), [23](#ref-23), [17](#ref-17)\] | # Dependents of an entity (e.g. class, file, module) | – |
| Fan-out | \[[15](#ref-15), [23](#ref-23), [17](#ref-17)\] | Total # entities an entity depends on | – |
| Propagation cost (PC) | \[[23](#ref-23)\] | Proportion of actual (indirect and direct) relative to all possible dependencies across modules | – |
| Decoupling level (DL) | \[[23](#ref-23)\] | Level of independence of modules based on the absence, presence and strength of dependencies | – |
| M-Score | \[[23](#ref-23)\] | Modularity based on cross-layer dependencies in a hierarchical dependency graph, internal dependencies and size of modules | – |
| Package type | S | Purpose of a package (e.g. research, complex algorithms, collection of configurations, collection of utility scripts), potentially determined by an LLM | – |

## Quality

| Metric | Ref. | Description | Impl. |
|--------|------|-------------|:-----:|
| Code smells | \[[15](#ref-15), [17](#ref-17)\] | # Code style issues and anti-patterns, e.g. Blob, Long Method | – |
| Code duplication | \[[15](#ref-15)\] | # Duplicated code blocks exceeding *n* copied lines | – |
| Smell density | \[[15](#ref-15), [16](#ref-16)\] | Code smells per entity, e.g. LoC | – |
| Bugs (static) | \[[18](#ref-18)\] | # Errors of a certain severity level found by static analysis tools | C/C++ |
| Bugs (LLM) | \[[24](#ref-24), [18](#ref-18)\] | # Bugs identified by an LLM, potentially in conjunction with static analysis tools | – |
| Bug commit density | \[[5](#ref-5), [3](#ref-3)\] | # Corrective commits per entity (e.g. module, file) | – |
| Fault proneness | \[[19](#ref-19), [16](#ref-16)\] | Bug fixing commit ratio | – |
| Fault prediction | \[[19](#ref-19)\] | # Estimated remaining defects in the code | – |
| Mean bug resolution time | \[[16](#ref-16)\] | Mean time a bug issue is open | – |
| CWE count | \[[18](#ref-18)\] | # CWE-related code issues identified by static analysis tools | C/C++ |
| Vulnerabilities | S, \[[25](#ref-25)\] | # Known vulnerabilities of a certain (e.g. critical) severity level for the package version, determined by vulnerability database query | ✓ |

## References

1. {:#ref-1} C. Gote, P. Mavrodiev, F. Schweitzer, and I. Scholtes, “Big Data = Big Insights? Operationalising Brooks’ Law in a Massive GitHub Data Set,” in *2022 IEEE/ACM 44th International Conference on Software Engineering (ICSE)*, 2022, pp. 262–273.
2. {:#ref-2} C. Paradis, R. Kazman, and M. Konrad, “A socio-technical perspective on software vulnerabilities: A causal analysis,” *Information and Software Technology*, vol. 176, p. 107553, 2024.
3. {:#ref-3} W. Mauerer, M. Joblin, D. A. Tamburri, C. Paradis, R. Kazman, and S. Apel, “In Search of Socio-Technical Congruence: A Large-Scale Longitudinal Study,” *IEEE Transactions on Software Engineering*, vol. 48, no. 8, pp. 3159–3184, 2022.
4. {:#ref-4} K. Champion and B. M. Hill, “Underproduction analysis of open source software,” *Empirical Software Engineering*, vol. 30, no. 6, p. 164, 2025.
5. {:#ref-5} M. Foucault, M. Palyart, X. Blanc, G. C. Murphy, and J.-R. Falleri, “Impact of developer turnover on quality in open-source software,” in *Proceedings of the 2015 10th Joint Meeting on Foundations of Software Engineering (ESEC/FSE)*, 2015, pp. 829–841.
6. {:#ref-6} V. Cosentino, J. L. C. Izquierdo, and J. Cabot, “Assessing the bus factor of Git repositories,” in *2015 IEEE 22nd International Conference on Software Analysis, Evolution, and Reengineering (SANER)*, 2015, pp. 499–503.
7. {:#ref-7} E. Jabrayilzade, M. Evtikhiev, E. Tüzün, and V. Kovalenko, “Bus factor in practice,” in *Proceedings of the 44th International Conference on Software Engineering: Software Engineering in Practice (ICSE-SEIP)*, 2022, pp. 97–106.
8. {:#ref-8} V. Haratian, M. Evtikhiev, P. Derakhshanfar, E. Tüzün, and V. Kovalenko, “BFSig: Leveraging File Significance in Bus Factor Estimation,” in *Proceedings of the 31st ACM Joint European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE)*, 2023, pp. 1926–1936.
9. {:#ref-9} E. Klimov, M. U. Ahmed, N. Sviridov, P. Derakhshanfar, E. Tüzün, and V. Kovalenko, “Bus Factor Explorer,” in *2023 38th IEEE/ACM International Conference on Automated Software Engineering (ASE)*, 2023, pp. 2018–2021.
10. {:#ref-10} L. Cañas-Díaz and Bitergia, “The Pony Factor: Metric of the Month,” 2022. [Online]. Available: <https://bitergia.com/blog/the-pony-factor-metric-of-the-month-november-2022/>
11. {:#ref-11} A. Lemay and N. Katiyar, “Supply Chain Risk Analysis Via SBOM Data Enrichment,” in *2025 IEEE International systems Conference (SysCon)*, 2025, pp. 1–8.
12. {:#ref-12} M. Guizani, A. A. Castro-Guzman, A. Sarma, and I. Steinmacher, “Rules of Engagement: Why and How Companies Participate in OSS,” in *2023 IEEE/ACM 45th International Conference on Software Engineering (ICSE)*, 2023, pp. 2617–2629.
13. {:#ref-13} Y. Zhang, M. Zhou, A. Mockus, and Z. Jin, “Companies’ Participation in OSS Development–An Empirical Study of OpenStack,” *IEEE Transactions on Software Engineering*, vol. 47, no. 10, pp. 2242–2259, 2021.
14. {:#ref-14} M. Claes, M. Mäntylä, M. Kuutila, and U. Farooq, “Towards automatically identifying paid open source developers,” in *Proceedings of the 15th International Conference on Mining Software Repositories (MSR)*, 2018, pp. 437–441.
15. {:#ref-15} T. Sharma and M. Kessentini, “QScored: A Large Dataset of Code Smells and Quality Metrics,” in *2021 IEEE/ACM 18th International Conference on Mining Software Repositories (MSR)*, 2021, pp. 590–594.
16. {:#ref-16} J. Bogner and M. Merkel, “To Type or Not to Type? A Systematic Comparison of the Software Quality of JavaScript and TypeScript Applications on GitHub,” in *2022 IEEE/ACM 19th International Conference on Mining Software Repositories (MSR)*, 2022, pp. 658–669.
17. {:#ref-17} R. Malhotra, B. Jain, and M. Kessentini, “DIR-SMOTE: a density-influence resampling framework for imbalanced code smell detection,” *Automated Software Engineering*, vol. 33, no. 3, p. 76, 2026.
18. {:#ref-18} M. F. Kharma, S. Choi, M. Alkhanafseh, and D. Mohaisen, “Security and Quality in LLM-Generated Code: a Multi-Language, Multi-Model Analysis,” *IEEE Transactions on Dependable and Secure Computing*, pp. 1–15, 2026.
19. {:#ref-19} U. Iftikhar, N. B. Ali, J. Börstler, and M. Usman, “A tertiary study on links between source code metrics and external quality attributes,” *Information and Software Technology*, vol. 165, p. 107348, 2024.
20. {:#ref-20} G. A. Campbell, “Cognitive complexity: an overview and evaluation,” in *Proceedings of the 2018 International Conference on Technical Debt (TechDebt)*, 2018, pp. 57–58.
21. {:#ref-21} M. Muñoz Barón, M. Wyrich, and S. Wagner, “An Empirical Validation of Cognitive Complexity as a Measure of Source Code Understandability,” in *Proceedings of the 14th ACM / IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM)*, 2020.
22. {:#ref-22} E. K. Adejumo and B. Johnson, “Explaining Code Risk in OSS: Towards LLM-Generated Fault Prediction Interpretations,” in *2025 40th IEEE/ACM International Conference on Automated Software Engineering Workshops (ASEW)*, 2025, pp. 199–203.
23. {:#ref-23} E. Pisch, Y. Cai, R. Kazman, J. Lefever, and H. Fang, “M-score: An Empirically Derived Software Modularity Metric,” in *Proceedings of the 18th ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM)*, 2024, pp. 382–392.
24. {:#ref-24} I. Jaoua, O. B. Sghaier, and H. Sahraoui, “Combining Large Language Models with Static Analyzers for Code Review Generation,” in *2025 IEEE/ACM 22nd International Conference on Mining Software Repositories (MSR)*, 2025, pp. 174–186.
25. {:#ref-25} N. Zahan, S. Shohan, D. Harris, and L. Williams, “Do Software Security Practices Yield Fewer Vulnerabilities?” in *2023 IEEE/ACM 45th International Conference on Software Engineering: Software Engineering in Practice (ICSE-SEIP)*, 2023, pp. 292–303.
