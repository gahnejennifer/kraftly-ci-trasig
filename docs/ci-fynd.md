## Fel 1
**Symptom:** Invalid workflow file, actions/runs/33737585470/workflow
**Orsak:** (Line: 5, Col: 12): Unexpected value 'pull-request'
**Fix:** Fel upplägg på ci.yml, ändra till:
on:
    pull_request:
    push:
        branches: [main]
**Hade upptäckts tidigare av:** Antingen genom att att läsa YAML:en innan