# Main changes

- UI: Improved identification of the currently playing music (music note) in the session and in search results.
- UI: Improved the visual appearance of the controller.
- UI: Removed the remaining oscillating loading ball code from the Fusion screen.
- DEBUG: Fixed invisible areas that could intercept clicks on the home screen: flags and buttons can now be clicked even when Kiki or -BIOPlayer- are over them.
- FEATURE: Improved identifier recovery: a missing licence key is now generated automatically if the account was still using the temporary value `000-000-000`.
- TECH: Improved GitHub Pages release-notes publishing without relying on `rsync`.
- TECH: Separated Windows installers by channel: `BIOPlayer`, `BIOPlayer Beta` and `BIOPlayer Dev` can now coexist on the same computer.
- UI: Fixed the Windows publisher field: it remains `BIOPlayer` for all channels.
