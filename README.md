📚 Curriculum Repository — How to Contribute

Welcome! This repository contains structured curriculum JSON files used to generate learning courses inside the OnlyEver app.

We welcome contributions — including new curriculums, improvements, and fixes — but please follow the guidelines below carefully so your PR can be reviewed and merged smoothly.


## ✅ What You Can Do

* Add a new curriculum
* Edit an existing curriculum
* Fix typos or improve sources


## ❌ Do Not Edit

* `curriculum_schema_*.json`
* GitHub Actions / workflows


## 📁 File Location & Naming

All curriculums live inside folders such as:

```
curriculums/<provider>/
```

File naming format:

```
<COURSE-NAME>.json
```

Example:

```
CURRICULUM-PRAXIS-Core-Math.json
```

Rules:

* No spaces
* Must be in `.json` format

---

## 📐 Schema Requirement

Your JSON **must match** the schema:

```
curriculum_schema_vX.X.json
```

Validate before PR:

```
jq . your_file.json
```

If this fails, your PR will be rejected.

---

## 🧱 Required Top-Level Structure

```json
{
  "schema_version": "1.0",
  "course": {},
  "curriculum": [],
  "supplemental_resources": {}
}
```

---

## 🎓 Course Image (Optional)

```json
"image": "images/praxis-hero.jpeg"
```

Rules:

* Must be repo-relative
* File must exist in `/images/`
* Do NOT use GitHub URLs

---

## 🔗 Sources

Each topic contains sources:

```json
{
  "title": "...",
  "url": "https://www.youtube.com/...",
  "type": "video"
}
```

Rules:

* YouTube links only (for now)
* Publicly accessible
* High quality and relevant to the course
* No duplicates

---

## 🔐 Merging

* Only maintainers can merge
* All checks must pass

---

## 🛠 How to Create a Pull Request

1. Fork this repository

2. Create a new branch

```
git checkout -b branch-name
```

3. Add or edit curriculum JSON file(s)

4. (Optional) Add image file to `/images/`

5. Validate your JSON

6. Commit your changes

```
git add .
git commit -m "Add/update curriculum"
```

7. Push your branch

```
git push origin add-my-curriculum
```

8. Open a Pull Request into `main`

9. Wait for checks and maintainer approval

---

## 🚫 Common Rejection Reasons

* Invalid JSON
* Schema mismatch
* Missing image
* Bad file name
* Non-YouTube links
* Broken URLs

---

## ❤️ Thanks

Your contributions help learners worldwide.
If unsure, open a discussion.


