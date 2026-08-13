# Main changes

- UI: Added and harmonized the glowing halo / blinking effect on music notes while a track is playing.
- UI: Bold display for the currently playing music.
- UI: Updated the search help text so it now depends on the real maximum limits according to whether the licence is active or not.
- UI: Zoom is now handled during initialization.
- UI: Zoom on hover for exercises, pencil icons and other controls.
- DEBUG: Fixed the offset of the playing search result when pressing Enter repeatedly.
- FEATURE: Without an active licence, interactions remain available and only the number of tracks allowed per exercise changes.
- UI: No visible BIOP / BIOPLayer / Bioplayer remains; only BIOPlayer is displayed.
- UI: No more SMS-style emoticons in the UI JSON files.
- UI: Removed the right-to-left offset restriction in the currently playing music display.
- FEATURE: No-active-licence mode again limits sessions to 5 exercises.
- FEATURE: The maximum number of tracks per exercise now depends on the licence.
- FEATURE: Adding, duplicating, importing and dropping exercises now respect the licence-related limit.
- FEATURE: Sessions exceeding the authorized limit can no longer be edited or saved while the licence is not active.
- FEATURE: New option: center the instruction currently being edited.
- FEATURE: Clicking the name of the currently playing music now finds its origin: exercise or search.
- TECH: Logging for the update procedure.
- TECH: Modified the admin email sent when an account is created.
