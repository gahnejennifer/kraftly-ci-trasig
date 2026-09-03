# Uppdrag: laga den trasiga pipelinen

Förra tech leaden skrev `.github/workflows/ci.yml` en sen kväll, testade lokalt ("funkar hos mig") och gick hem.
Pipelinen har aldrig varit grön. Er uppgift: få den grön – **och rätt** – utan att sänka kraven.

Instruktionerna finns i Canvas: *Övning 2 · Laga den trasiga pipelinen*. Kortversion:

1. Skapa ett nytt, tomt repo på GitHub och pusha det här projektet dit (`git remote add origin … && git push -u origin main`).
2. Öppna fliken **Actions**. Läs. Börja med det första felet – det som hindrar allt annat.
3. Ett fel i taget: hypotes → fix → push → läs loggen igen.
4. Logga varje fel ni hittar i `docs/ci-fynd.md`: symptom · orsak · fix · hur ni skulle upptäckt det tidigare.

Ledtråd: pipelinen ska följa reglerna från förstudierna. Grönt är inte samma sak som rätt.
