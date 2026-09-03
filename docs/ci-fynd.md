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
**Fix:** lägga till - uses: actions/checkout@v4 i steps i ci.yml
**Hade upptäckts tidigare av:** när vi hade kört beroendena själv

## Fel 3
**Symptom:** Error: Process completed with exit code 254.
**Orsak:** Workflow-filen körde `npm run tests`, men package.json har bara `test:run` (och `test`) – inte `tests`
**Fix:** Ändrade `npm run tests` till `npm run test:run` i ci.yml
**Hade upptäckts tidigare av:** att jämföra scripts-namnen i package.json mot run-kommandona i ci.yml, eller köra kommandot exakt som skrivet lokalt