# SplatWorks Educator

A complete five-module, self-paced professional-learning course for K–12 educators. The course follows the native JSON contract reviewed in the earlier `course.md` instructions.

## Start here

- **Import:** `splatworks-educator.tar.gz` is the native course package for GopherLMS or SapiqoLMS. Use Admin → Imports & backups → Course content → Course package. Do not use the LearnDash JSON form.
- **Course data:** `course.json` is the canonical course content, with five modules, 20 lessons, 20 videos, five quizzes and 25 questions.
- **Preview:** serve this folder with a local web server and open `preview.html` for a read-only view. For example, run `python3 -m http.server 8000` from this folder, then visit `http://localhost:8000/preview.html`. Double-clicking the preview can show its text and images, but browser media/caption behavior may differ for local files.
- **Badge:** `badge.png` is the generated purple/gold inverted-triangle SplatWorks Educator badge. A user-supplied blue/gold alternative is included under `media/images/educator-badge-alternative.png`.
- **Editing:** `source.md` is an additional editable creator source. Keep the JSON as the canonical version for this delivery; a generic Markdown rebuild will not preserve every final HTML annotation, metadata field, caption setting or linked resource automatically.

## Modules

1. **Getting Started with SplatWorks** — learning intentions, success criteria, ecosystem navigation, saving, planning and self-regulation.
2. **Teach and Create with DrawSplat** — worked examples, visual relationships, self-explanation, structured collaboration and accessible creation.
3. **Build with SplatWorks Apps and Media Tools** — office applications, data, publishing, audio/video production and accessible explanations.
4. **Practice, Feedback and Assessment** — retrieval, criterion-based feedback, revision, classroom utilities and evidence of individual learning.
5. **Play, Type and Transfer** — the four typing experiences, suitable K–12 games, accessibility, debriefs and a classroom capstone.

Each module has About, Explore, Practice On Your Own, and Resources/Knowledge Check sections. Three optional video overviews appear in Explore and a fourth supports Practice. The written instructions, practice and assessments remain complete without watching them. The linked ecosystem field guide covers all 68 destinations in the current live Studio registry, including the five office apps, PlanSplat, whiteboard, creation/media tools, utilities, games and support destinations. This is comprehensive orientation, not a requirement to use 68 tools in one lesson.

## Media and illustrations

The course includes 20 optional narrated visual overviews, approximately 26 minutes total. The videos use synthetic English narration, original scripts, instructional slides and real screenshots captured from the local project. They are not live recordings of a presenter operating the apps. Each video includes burned-in captions, a separate WebVTT caption file, a poster image and HTML/plain-text transcripts.

The five module banners and blue/gold alternate badge were supplied by the user. The illustrations are concept art. Module 4 contains imagined names such as ReflectSplat, ProgressSplat, FeedbackSplat and CoachSplat; those are labeled as teaching concepts, not actual products. Module 5’s art does not reproduce the actual game mechanics: Cipher Chase is the typing-and-steering experience, and Story Sprint is passage practice. Course text and actual screenshots make these distinctions explicit.

The main badge was generated with the built-in image_gen tool. Its prompt and provenance are in `media/resources/badge-generation.txt` and `asset-manifest.json`. Project images and screenshots illustrate this ecosystem; retain applicable project and third-party license notices when redistributing source assets. No identifiable student work was used.

## Import and compatibility

The native archive contains one top-level folder named `splatworks-educator`, with `course.json`, a reader shell, badge and media. It uses standard USTAR headers inside gzip because the reviewed importers reject PAX/GNU extended headers.

The standalone course export is a **draft**; SplatLMS bundles its first course as **published**. Review it as an administrator, check local file and upload limits, then publish when ready. Keep the slug `splatworks-educator` when updating this same course; choose a new slug for a distinct course because the importer copies over an existing matching slug.

The package’s bundled media, transcripts, worksheets and illustrations are local. App links and research links need internet access. The destination LMS supplies its shared reader assets. `preview.html` is a separate read-only convenience view; it does not save progress or award completion.

**SapiqoLMS 1.13.1 compatibility:** the reviewed HTML sanitizer removes inline `<video>`, `<source>` and `<track>` elements. GopherLMS 1.13.2 preserves those elements. Every video therefore also has an ordinary direct MP4 link, a transcript link and a caption-file link. The direct MP4 contains burned-in captions and can be opened/downloaded in either system. No LMS code was changed. This preserves course access in the older Sapiqo build while allowing inline playback in GopherLMS.

If the archive exceeds your server’s request limit, have the administrator increase the permitted upload size or use the installation’s supported file-deployment workflow. The reviewed archive validators limit expanded content to 2 GiB and 20,000 entries; this course is well below both limits.

## Completion, credit and evidence

- Complete all 20 lesson sections and pass the five knowledge checks at 80%. Quizzes allow unlimited retries. These are 25 tracked completion units; video watching is not separately verified by the course JSON.
- Practice artifacts and the capstone are self-checked. An administrator/facilitator can separately configure an LMS assignment if submission and grading are needed. Text instructions alone do not create that workflow.
- Estimated course time is about five hours including reading, practice and reflection. `cpe_hours` and `gt_hours` are 0, and `certification` is false. The badge is a course-completion artifact, not a claim of external accreditation.
- Research references distinguish teacher clarity, self-explanation, metacognition, retrieval and feedback estimates. Effect sizes and EEF months-of-progress summaries are different metrics. None is presented as a measured effect of a SplatWorks product.
- `schoolyard-observations.csv` is fictional practice data, explicitly labeled throughout. It supports discussion of evidence and uncertainty, not a real-world causal claim.

## Validation

See `validation-report.json` for checks performed on this delivery. The report covers native import/discovery/quiz grading in isolated instances of both LMSs, package paths, all bundled file references, media format/decoding, image loading, caption timing, the browser preview and public ecosystem links. It distinguishes inline playback in GopherLMS from Sapiqo’s direct-link fallback. No live courses, student records or repository files were changed.

The final research, source and asset review date is October 31, 2026. Recheck product features and public links before a later rollout.
