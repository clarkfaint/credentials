# Course Certificates

A simple page listing course certificates from providers that don't issue Credly badges, each linked to the provider's official verification page.

Live at: https://clarkfaint.github.io/credentials/

## Adding a new course

Edit `credentials.json` and add an entry to the `credentials` list:

```json
{
  "title": "Course title exactly as on the certificate",
  "provider": "Provider via Coursera",
  "completed": "2026-11-08",
  "skills": ["Skill one", "Skill two"],
  "certificate_image": "certificates/course-name.png",
  "certificate_pdf": "certificates/course-name.pdf",
  "share_url": "https://coursera.org/share/...",
  "verify_url": "https://coursera.org/verify/YOUR-ID"
}
```

Put the certificate PDF and a PNG image of it in the `certificates` folder (on Linux: `pdftoppm -png -r 110 -singlefile course-name.pdf course-name`). Commit the change. GitHub Pages updates within a minute or two, and the page sorts entries newest first.
