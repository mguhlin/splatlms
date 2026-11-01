# SplatLMS

The SplatWorks learning management system. SplatLMS is a separately branded, self-hostable product adapted from **Sapiqo LMS by Miguel Guhlin**. Its first bundled course is **SplatWorks Educator**.

Version **1.0.0** · © 2026 Miguel Guhlin · [CC BY-SA 4.0](LICENSE)

## Run SplatLMS

Requires PHP 8.1+ with PDO SQLite (or MariaDB/MySQL), mbstring, GD, fileinfo, Phar and the extensions checked by the installer. The runtime does not require Node or Composer.

```bash
bash installer/install.sh
bash installer/serve.sh 8000
```

The installer creates an administrator from credentials you supply. No default login or real user database is shipped. Open http://localhost:8000 after setup. For a scripted setup, use `php splatlms/bin/setup.php --from-env` with ADMIN_EMAIL and ADMIN_PASSWORD set in your environment.

Docker: set ADMIN_EMAIL and ADMIN_PASSWORD, then run `docker compose -f installer/docker-compose.yml up -d --build`. It binds to localhost:8080. Use your configured HTTPS host for production. GitHub Pages serves the product introduction only; it cannot run the PHP LMS or store learner records.

## First course

`content/splatworks-educator/` contains the complete first course: five modules, twenty lesson sections, five quizzes/25 questions, a transparent inverted-triangle badge, a field guide to all 68 reviewed ecosystem destinations, worksheets and illustrations.

Twenty **optional video overviews** use original scripts, app screenshots and synthetic English narration. They are narrated slides, not live screencasts. Burned-in captions, WebVTT files and complete transcripts are included. Written lessons and activities remain complete without watching them. The five-module structure covers getting started; DrawSplat teaching/creation; office apps and media; practice/feedback; typing, suitable K–12 games and a capstone.

The bundled course is published as the first catalog offering. Completion uses 20 lesson steps and five 80% knowledge checks. Practice/capstone artifacts are self-checked unless an instructor creates an assignment. CPE/GT credit remains 0; the badge is not external accreditation.

## Product identity and isolation

- `splatlms/` — replaceable application code.
- `splatlms-data/` — persistent local data, credentials, uploads and configuration (not committed).
- `content/` — course folders and shared reader assets.
- `SPLATLMS_DATA` and `SPLATLMS_COURSES` — optional data/content overrides.
- Purple, golden yellow, white and charcoal match SplatWorks; brand assets and course illustrations are bundled locally.

The SplatLMS edition label prevents accidentally installing an updater package intended for a different branded edition. Original Sapiqo installations and their data are untouched. This is a new product namespace, not an automatic migration of existing learner records.

## Features

Learner accounts, enrollment, course authoring, quizzes, assignments/rubrics, forums, organizations/groups, badges/certificates, transcripts, reports, imports/exports, MFA, scoped API access, SSO configuration and an updater come from the Sapiqo foundation. Inline local video/audio/caption support is preserved through the course HTML sanitizer in this edition. Provider integrations still require real configuration and appropriate end-to-end validation.

## Checks and provenance

Run `python3 tests/run.py`, `python3 tests/concurrency.py`, and the browser checks documented in [CONTRIBUTING.md](CONTRIBUTING.md). Current product-specific scope and results are in [docs/SPLATLMS.md](docs/SPLATLMS.md). Inherited dated audits under docs/ describe upstream Sapiqo, not a new SplatLMS certification. See [UPSTREAM.md](UPSTREAM.md) for attribution and asset provenance and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for third-party licenses.
