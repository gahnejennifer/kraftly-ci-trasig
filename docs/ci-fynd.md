## Fel 1
**Symptom:** Invalid workflow file, actions/runs/33737585470/workflow
**Orsak:** (Line: 5, Col: 12): Unexpected value 'pull-request'
**Fix:** Fel upplägg på ci.yml, ändra till:
on:
    pull_request:
    push:
        branches: [main]
**Hade upptäckts tidigare av:** Antingen genom att att läsa YAML:en innan

## Fel 2
**Symptom:** Installera beroenden, actions/runs/33746087636/job/100618768061
**Orsak:** Error: Process completed with exit code 254.
**Fix:** ta bort s från npm run tests i ci.yml
**Hade upptäckts tidigare av:** när vi hade kört beroendena själv