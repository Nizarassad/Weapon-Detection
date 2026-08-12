# Ethics and responsible use

## High-consequence context

Automated weapon detection can affect safety, civil liberties, privacy, and how authorities respond to people. A model output is uncertain evidence, not a determination that a person possesses a weapon or poses a threat.

This research artifact must not be used as the sole basis for policing, accusation, access denial, disciplinary action, or use-of-force decisions.

## Main risks

- **False positives:** benign objects, gestures, empty hands, image artifacts, or unfamiliar scenes may trigger an alert.
- **False negatives:** weapons may be missed because of occlusion, scale, lighting, viewpoint, appearance, motion blur, or domain shift.
- **Unequal performance:** a narrow dataset may not represent locations, camera systems, clothing, behaviours, or populations encountered elsewhere.
- **Automation bias:** operators may over-trust a numerical confidence score.
- **Privacy and surveillance:** deployment may increase collection or analysis of identifiable imagery.
- **Security and misuse:** models and pipelines can be attacked, evaded, or repurposed.

## Minimum safeguards for any further study

A deployment-oriented study would need representative local data with lawful provenance, independent validation, subgroup and scenario analysis, calibrated thresholds, trained human review, auditable escalation rules, continuous drift/error monitoring, adversarial testing, access controls, retention limits, incident review, and legal and ethical oversight.

Alert thresholds must reflect both the cost of missed detections and the operational capacity to investigate false alerts. Performance should be reported at the intended operating point, not only with aggregate metrics.

## Research claims

The repository documents a 2023 MSc experiment. It does not demonstrate field reliability, demographic fairness, legal compliance, or fitness for operational use. Any derivative work should preserve this distinction and report failures as prominently as headline metrics.
