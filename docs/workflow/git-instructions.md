# Git Instructions

After unzipping this capture layer into the repo root:

```bash
cp -R ainds-capture-layer/* /path/to/ainds/
cd /path/to/ainds
git status
git add .
git commit -m "Add AINDS capture layer and handbook outline"
git push
```

## Suggested Branch Workflow

```bash
git checkout -b feature/capture-layer
git add .
git commit -m "Add AINDS capture layer and handbook outline"
git push -u origin feature/capture-layer
```

Then open a pull request.

## Suggested First Issue

Title:

```txt
Establish AINDS knowledge capture workflow
```

Body:

```md
Create the initial capture workflow for AINDS so important project discoveries are preserved outside of chat.

Includes:
- /book handbook outline
- /sessions working-session notes
- /templates session, ADR, and chapter templates
- Knowledge Curator agent
- Form validation pattern example
- Icon Specialist origin note
```
