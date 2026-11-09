# UMBRAL — Privacy Policy

**Effective date:** November 9, 2026

UMBRAL is a browser new-tab extension. It provides customizable shortcuts, visual settings, and optional website suggestions based on browsing patterns.

## Summary

- UMBRAL does not operate a developer-controlled analytics, advertising, or user-data collection server.
- Browsing-history analysis is optional and starts only after the user grants the browser's `history` permission and enables predictions.
- The prediction model is processed and stored locally by the extension.
- Shortcut and appearance settings are stored using the browser's extension sync storage. Depending on the user's Microsoft Edge sync settings, this information may be synchronized through Microsoft's services.
- Website icons may be requested from the destination website, DuckDuckGo, or Google. These requests disclose the domain for which an icon is requested to the relevant provider.

## Information UMBRAL processes

### Optional browsing-history predictions

When the user explicitly enables predictions and grants the optional `history` permission, UMBRAL reads browsing-history entries through the browser's History API to calculate suggestions.

The local prediction model stores:
- The website origin and hostname (not the full page path, query string, or fragment).
- The visit timestamp.
- The browser transition type associated with the visit.

Page titles and full page URLs are not retained in the prediction model.

The model uses a rolling 90-day analysis window and is limited to 2,400 visit events. Initial seeding is limited to up to 200 history entries and up to 60 visits per entry, subject to the overall event limit. Older events are excluded from prediction calculations and are removed as the model is updated. If the extension is inactive, expired records may remain in local extension storage until the next model update or reset.

The model is used only to rank frequently visited and contextually relevant websites for the new-tab page. It is not transmitted to UMBRAL's developer.

### Shortcuts and appearance settings

User-created shortcuts (names and URLs), layout preferences, visual themes, gradient colors, and related settings are stored with the browser's `storage.sync` extension API. The browser may synchronize this information across the user's signed-in devices according to the user's Edge sync configuration. UMBRAL's developer does not receive this information.

### Website icons (favicons)

To display website icons, UMBRAL may request an icon using:
- DuckDuckGo's favicon service.
- Google's favicon service.
- The website itself, using its `/favicon.ico` resource.

These requests necessarily disclose the relevant website domain (and the requester's network information, such as IP address) to the service or website receiving the request. UMBRAL does not send the browsing-history model or a list of visited websites to these providers. The providers process requests under their own privacy policies.

## Permissions

- **Storage (required):** saves shortcuts, appearance settings, and the local prediction model.
- **History (optional):** reads browsing history only for the predictions feature, after the user explicitly grants permission.

UMBRAL does not request access to page contents, passwords, form entries, personal communications, precise location, or health information.

## User controls and deletion

- Predictions are off until the user enables them and grants the optional History permission.
- The user can disable predictions from UMBRAL. The extension then removes the History permission and clears its local prediction model.
- The user can also revoke the History permission through Edge's extension settings. UMBRAL listens for permission removal and clears the local prediction model.
- Clearing browsing history in Edge causes corresponding website events to be removed from the local model. Clearing all history clears the model.
- Shortcuts and appearance settings can be changed or removed from the extension. Browser-synchronized copies are subject to the user's Edge sync and browser data controls.

## Sharing and sale

UMBRAL's developer does not sell browsing history, shortcut data, or settings, and does not transmit the local prediction model to third parties. The only third-party requests initiated for the features described above are favicon requests, which disclose the domain needed to retrieve the icon. Browser synchronization is handled by Microsoft Edge and is subject to Microsoft's own services and privacy terms.

## Changes to this policy

This policy may be updated when UMBRAL's functionality or data practices change. The effective date above will be revised when an update is made.

## Contact

For privacy questions, use the developer contact information provided on the UMBRAL Microsoft Edge Add-ons listing.
