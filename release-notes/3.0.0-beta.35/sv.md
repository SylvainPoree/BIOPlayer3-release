# Huvudsakliga ändringar

- UI: Förbättrad markering av den musik som spelas (musiknot) i sessionen och i sökresultaten.
- UI: Förbättrat kontrollens visuella utseende.
- UI: Resterande kod för den oscillerande laddningsbollen har tagits bort från Fusion-skärmen.
- DEBUG: Osynliga områden som kunde fånga klick på startsidan har korrigerats: flaggor och knappar kan nu klickas även när Kiki eller -BIOPlayer- ligger ovanpå dem.
- FUNKTION: Förbättrad återställning av identifierare: en saknad licensnyckel genereras automatiskt om kontot fortfarande använde det tillfälliga värdet `000-000-000`.
- TECH: Förbättrad publicering av versionsnoteringar på GitHub Pages, utan beroende av `rsync`.
- TECH: Windows-installationsprogrammen har separerats per kanal: `BIOPlayer`, `BIOPlayer Beta` och `BIOPlayer Dev` kan nu finnas sida vid sida på samma dator.
- UI: Windows-fältet för utgivare har korrigerats: det förblir `BIOPlayer` för alla kanaler.
