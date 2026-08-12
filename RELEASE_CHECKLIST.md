# Research artifact release checklist

Do not create a GitHub release or Zenodo DOI until every blocking item is complete.

## Blocking security checks

- [ ] Revoke and rotate every Roboflow credential previously committed.
- [ ] Revoke and rotate every ClearML credential previously committed.
- [ ] Confirm that the current release tree contains no credentials or private configuration.
- [ ] Review provider account activity for unexpected use.
- [ ] Decide whether to rewrite Git history; this is separate, disruptive work and must be coordinated before force-pushing.

## Rights and privacy checks

- [ ] Confirm the right to redistribute the MSc report publicly.
- [ ] Audit `unseen_data.zip` image provenance, consent, copyright, and privacy.
- [ ] Audit saved notebook outputs for third-party images, personal data, and private metadata.
- [ ] Confirm redistribution terms for every bundled or externally hosted model weight.
- [ ] Confirm the external dataset's version and terms; do not imply it is bundled or relicensed.
- [ ] Remove anything confidential, proprietary, or personally identifying that is not essential.

## Reproducibility and metadata checks

- [ ] Validate `CITATION.cff`.
- [ ] Validate `.zenodo.json`.
- [ ] Verify author name, title, version, release date, and supervisor attribution.
- [ ] Verify all links and render the PDF report.
- [ ] Ensure historical metrics match the submitted report.
- [ ] Preserve the statements that the artifact is not peer reviewed and not safety certified.
- [ ] Record known dataset, dependency, seed, timing, and hardware limitations.

## Release sequence

1. Merge the audited research-artifact pull request.
2. Connect Zenodo to GitHub and enable `Nizarassad/Weapon-Detection`.
3. Create GitHub release `v1.0.0` only after all blocking checks pass.
4. Confirm that Zenodo archives the intended release and metadata.
5. Add the DOI badge and DOI to `README.md` and `CITATION.cff`.
6. Add the DOI-backed output to ORCID and the Career HQ Brain.

A Zenodo DOI makes a snapshot persistent. Do not use it as a substitute for peer review or describe the deposit as a peer-reviewed paper.
