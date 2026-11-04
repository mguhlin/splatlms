# SplatLMS 1.0.0 implementation and verification

Adapted from Sapiqo LMS 1.13.1. The original project attribution/license remains in LICENSE, UPSTREAM.md and the application footer.

The SplatWorks visual tokens are purple #6d38e8, deep purple #4720a4, charcoal #172033, golden yellow #f5b942, pale lavender #f8f6fc and white. The system UI type stack follows SplatWorks. A white brand header and prominent classroom course artwork connect the LMS to the ecosystem without changing the established admin workflows.

Runtime code is splatlms/, persistent data is splatlms-data/, and environment variables use SPLATLMS_. No original Sapiqo installation or data was changed. Version 1.0.0 identifies the new product; edition_label SplatLMS separates updater packages. This release is a fresh product, not an automatic in-place migration of a Sapiqo database.

SplatWorks Educator is the first published course. Its twenty narrated slide overviews are optional, use synthetic English speech and are identified as such. Written instructions, captioned local MP4, WebVTT and transcripts are retained. No watching-time condition was introduced. Approved CPE and GT hours are 0.

The sanitizer now permits a constrained list of video/audio/source/track tags and attributes. All src/poster values still pass safe_media_ref; event handlers and scripting schemes are rejected. Learner course access and answer-key stripping remain unchanged. Tests exercise legitimate playback markup and malicious media attributes.

Published course badge artwork is available to the public catalog; draft badges and lesson media remain access-controlled. Three HTTP regressions cover those boundaries.

Local validation passed: 86 security regressions, 42 HTTP regressions, nine author-preview access/order checks, backup/restore round trips, syntax checks, eight-worker contention checks for resets/quizzes/MFA/assignments, SMTP protocol fixtures, recovery/relocation, signed update and rollback fixtures, and the existing desktop/mobile learner and administrator browser journeys. An actual first-course journey separately verified the public catalog badge, optional-overview labels, captioned inline playback and 390px phone layout (see product-browser-check.json). No production learner data or original Sapiqo files were changed. MariaDB and Docker are covered by CI; they were not run locally for this branding release. External identity-provider and real SMTP-provider integration were not retested.

The product introduction can deploy to GitHub Pages. A live multiuser LMS needs PHP hosting and administrator-supplied credentials; GitHub Pages does not run it.
