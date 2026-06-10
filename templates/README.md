# Material Share Repo Guide

See [README.md](../README.md) for the full guide.

This folder contains copy-ready templates:

```
templates/
├── hub-repo/           # Empty multi-category repo
├── course-chapter/     # Chapter-based course
└── course-day/         # Day-based bootcamp
```

## Quick copy

```bash
# New hub repo
cp -r templates/hub-repo/* ../my-new-hub/

# New chapter course inside existing hub
mkdir -p ../my-hub/courses/my-course
cp -r templates/course-chapter/* ../my-hub/courses/my-course/
```

Then create sibling folders manually:

```bash
mkdir -p ../my-hub/{courses,guides,labs,research,interview-prep}
```
