---
name: Bilingual UI coverage
description: The app's English data model is preserved while the rendered Salamatak UI supports reversible Arabic and English localization.
---

Salamatak preserves English values for local storage, filtering, routing, and business logic, then localizes rendered text, form attributes, dynamic status values, and RTL layout at the UI boundary.

**Why:** The existing MVP is compact and contains many hardcoded JSX labels; changing stored values would risk breaking filters, routes, and double-blind offer behavior.

**How to apply:** Add new user-visible strings to the shared translation map, and ensure CSS-generated text has an RTL rule because DOM text localization cannot reach pseudo-elements.