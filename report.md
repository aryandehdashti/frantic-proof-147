# Nameclick dogfood report — Frantic claim 9b282aed (bounty 147)

- **What I tried:** Installed Nameclick 0.2.0 from the Chrome Web Store into Google Chrome 157, signed in with Google, opened the Wikipedia article for Sundar Pichai, selected the name "Sundar Pichai" in the lead, right-clicked and chose the extension's "Find email" context-menu item — the selected-name flow.
- **What happened:** The Nameclick card opened on the page and completed a lookup: "No email found for Sundar Pichai — Nothing was used." It then asked to confirm the employer, pre-filling "Alphabet and Google" from the page context, with a "Find email >" retry. A completed no-match, which the bounty counts.
- **Specific observation:** The miss card still shows the resolved employer guess ("Is this where they work? Alphabet and Google") and offers a one-click corrected retry — useful because a bare name selection has no company signal of its own; the page context supplied it.
- **Environment:** Windows 11, Google Chrome 157.0.8103.40, extension v0.2.0 installed from Chrome Web Store (chrome://extensions shows Source: Chrome Web Store), lookup driven through the extension's own context-menu/selected-name UI on 2026-11-11 ~23:39 UTC.
- **One friction point:** The context-menu "Find email" item only appears when text is actually selected on the page; with no selection the menu shows no Nameclick entry at all.
