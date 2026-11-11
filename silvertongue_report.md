# Silvertongue voice draft — run report

- **App / model:** Devin CLI (Cognition, interactive agent), model SWE-2 Flash Max. MCP client over Streamable HTTP, protocol revision 2025-03-26, no account, no API key.
- **Server:** https://mcp.silvertongue.dev/mcp (serverInfo name=silvertongue, version 0.1.5). Call: tools/call get_voice_packet.
- **Voice and ask:** voice=gordon-ramsay, format=post, length=short, platform=generic, intensity/edge/emoji/spelling at defaults (full/full/on/voice). Packet returned voice_id gordon-ramsay@sha256:02f7a630…, release sha256:92b08996…, target range per packet.
- **Draft exactly as written:**

> Your steak isn't tough, it's cooked to death. Pat it dry, get the pan properly smoking, two minutes a side, then rest it. That's the whole trick. Everything else is noise.

- **Score: 8/10.** It reads as Ramsay: direct second-person address, one food image carried through (cooked to death / smoking pan), short commands, and it lands on the fix rather than a sign-off. Held back from 9-10 because 'the whole trick' is close to a generic guru closer and the packet asked for a post, so a slightly more specific grievance (e.g. naming the actual mistake, salt or resting) would give it more of his particularity.
- **Finding:** none blocking. What I tried: fetched the packet twice (search_voices not needed; slug resolved directly), confirmed target unit=characters and the clean/full edge flags behave as documented. The only friction was that a bare tools/call without a prior initialize still returns the packet — stateless transport, which is convenient but means a receipt is the only proof the fetch happened.
- **One change:** I would add the packet's character target to the report request flow itself — knowing min/max up front would have saved a second call to confirm the length bucket.
