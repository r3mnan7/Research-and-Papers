---
tags: [control-catalog, ai-fud-whitepaper]
aliases: [Control Catalogs]
---
# Control Catalogs

Index with AI assistance, November 4, 2026. These are the seven general-purpose frameworks RQ3 tests, pulled from primary sources into one table each so that any `53:` / `CIS:` / `ASVS:` / `CSF:` / `ZTMM:` / `63:` / `161:` citation in [[RQ3 Control Coverage]] or [[RQ3.1 Minimum Control Set]] can be checked against the framework's own text without opening the PDF. Extraneous text (introductions, discussion, references, appendices other than the control text itself) is removed; the control text is verbatim apart from extraction cleanup and layout. The CIS catalog stays in the author's vault and out of the public repository; see [[CIS Note]].

| Catalog | Source (primary) | Unit | Count | Notes |
| --- | --- | --- | --- | --- |
| [[NIST CSF 2.0 Catalog]] | NIST CPRT, CSF 2.0 [8] | Function / Category / Subcategory | 6 / 22 / 106 (+26 withdrawn from 1.1, marked W) | Current and withdrawn elements separated by CPRT status |
| [[CIS Controls v8.1 Catalog]] | CIS Controls v8.1.2 guide PDF (user-supplied) [9] | Control / Safeguard | 18 / 153 | Lowest Implementation Group per safeguard (IG1 56, IG2 +74, IG3 +23); RQ3 assumes IG3 [289]. CC BY-NC-ND; vault only, see [[CIS Note]] |
| [[NIST SP 800-53 Rev 5 Catalog]] | NIST CPRT, SP 800-53 Rev. 5.1.1 [15] | Control / Enhancement | 323 base, 1,193 entries incl. enhancements; 182 withdrawn | IDs normalized as `AC-3(2)`; withdrawn entries kept and marked |
| [[CISA ZTMM v2.0 Catalog]] | CISA ZTMM v2.0 PDF [16] | Function × maturity stage | 40 functions × 4 stages | A maturity model, not a control catalog; RQ3 assumes Optimal |
| [[OWASP ASVS 5.0.0 Catalog]] | OWASP ASVS GitHub repository, 5.0.0 CSV [17] | Requirement | 345 (L1 70, L2 183, L3 92) | RQ3 assumes L3 |
| [[NIST SP 800-63-4 Requirements Extraction]] | pages.nist.gov HTML edition, 800-63-4 / A / B / C [18] | Normative statement (SHALL/SHOULD/MAY) | 873 | An extraction, not a catalog: the suite is prose. Row IDs are this extraction's own |
| [[NIST SP 800-161r1 Catalog]] | NIST SP 800-161r1 PDF, Appendix A [19] | Control / Enhancement with C-SCRM guidance | 261 entries (145 base, 116 enhancements) | Page numbers from the PDF; numbering follows Appendix A, with Table B-1 differences marked; CM-9 and MA-2 carry no guidance in the source; SA-9's guidance is in SA-9(1) |

**How these were built.** NIST CSF and SP 800-53 came from NIST's CPRT JSON service; ASVS from the project's own CSV in its repository; CIS from the user's copy of the v8.1.2 guide; ZTMM, SP 800-161r1, and SP 800-63-4 from the published PDF or HTML, read page by page with the page coordinates or heading structure used to rebuild tables. Each catalog's header records its own method and spot checks. Build scripts and intermediate data are not part of the public repository.

**What they are for.** Looking up a cited control's actual text; checking that a control cited at a path step exists at the assumed level (IG3, L3, Optimal); and, for the residual analysis in RQ3, searching a whole framework for any requirement that could bound a step the path analysis calls unbounded, so that "no control" means "none in the catalog," not "none the author recalled."
