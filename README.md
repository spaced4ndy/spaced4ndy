### Backend and distributed-systems engineer · Haskell

Founding engineer on [SimpleX Chat](https://github.com/simplex-chat/simplex-chat) since 2020: a private messaging network with no user identifiers.

#### Selected work

**SimpleX Chat**
- Chat relays for SimpleX Channels: [RFC](https://github.com/simplex-chat/simplex-chat/blob/stable/docs/rfcs/2025-10-20-chat-relays.md), [core](https://github.com/simplex-chat/simplex-chat/pull/6383), [iOS](https://github.com/simplex-chat/simplex-chat/pull/6634), [Android/desktop](https://github.com/simplex-chat/simplex-chat/pull/6670)
- Channel integrity: [signed roster of privileged members](https://github.com/simplex-chat/simplex-chat/pull/7017), [message signing](https://github.com/simplex-chat/simplex-chat/pull/7115)
- Group delivery: [restart-safe delivery jobs](https://github.com/simplex-chat/simplex-chat/pull/6178); a [per-member relations vector](https://github.com/simplex-chat/simplex-chat/blob/stable/docs/rfcs/2025-11-24-member-relations-vector.md) instead of per-pair records ([code](https://github.com/simplex-chat/simplex-chat/pull/6459), [forwarding](https://github.com/simplex-chat/simplex-chat/pull/6464), [migration](https://github.com/simplex-chat/simplex-chat/pull/6445), [stage 2](https://github.com/simplex-chat/simplex-chat/pull/6490))
- Group sends: ~20 MB → ~200 kB of temporary storage per message to 1,000 members: [encrypt on delivery](https://github.com/simplex-chat/simplexmq/pull/1446), [body stored once](https://github.com/simplex-chat/simplexmq/pull/1453)
- PostgreSQL backend alongside SQLite, one codebase: [agent](https://github.com/simplex-chat/simplexmq/pull/1421), [chat core](https://github.com/simplex-chat/simplex-chat/pull/5403)
- XFTP file transfers: client agent ([file descriptions](https://github.com/simplex-chat/simplexmq/pull/633), [receiving](https://github.com/simplex-chat/simplexmq/pull/637), [recoverable sending](https://github.com/simplex-chat/simplexmq/pull/707)); integration into the chat core and apps, 35+ PRs ([receiving files](https://github.com/simplex-chat/simplex-chat/pull/1997), [enabled by default](https://github.com/simplex-chat/simplex-chat/pull/2198))
- Incognito mode, a random profile per contact or group, never linked to the main one: [RFC](https://github.com/simplex-chat/simplex-chat/blob/stable/docs/rfcs/2022-08-10-incognito-connections.md), [core](https://github.com/simplex-chat/simplex-chat/pull/926)
- IP protection, approval before downloading from unknown file servers: [RFC](https://github.com/simplex-chat/simplex-chat/blob/stable/docs/rfcs/2024-04-16-ip-address-protection.md), [core](https://github.com/simplex-chat/simplex-chat/pull/4043)
- Supporter badges: [badge service](https://github.com/simplex-chat/simplex-chat/pull/7353); code redemption ([core and service](https://github.com/simplex-chat/simplex-chat/pull/7438), [apps](https://github.com/simplex-chat/simplex-chat/pull/7482)), [monthly renewal](https://github.com/simplex-chat/simplex-chat/pull/7448); App Store and Google Play [purchases](https://github.com/simplex-chat/simplex-chat/pull/7590), [receipt verification](https://github.com/simplex-chat/simplex-chat/pull/7654), [subscriptions](https://github.com/simplex-chat/simplex-chat/pull/7716)
- AI-assisted development: LLM docs ([iOS](https://github.com/simplex-chat/simplex-chat/pull/6633), [Android/desktop](https://github.com/simplex-chat/simplex-chat/pull/6655)); Claude Code app tests in CI ([iOS](https://github.com/simplex-chat/simplex-chat/pull/7737), [Android](https://github.com/simplex-chat/simplex-chat/pull/7786), [desktop](https://github.com/simplex-chat/simplex-chat/pull/7736)); agent-built features ([channel signing and moderators](https://github.com/simplex-chat/simplex-chat/pull/7805), [directory search](https://github.com/simplex-chat/simplex-chat/pull/7939), draft); [bug diagnosed in CI](https://github.com/simplex-chat/simplex-chat/pull/7952)

<details>
<summary><b>More work</b> (click to expand)</summary>

- Member admission, with admins reviewing new members in a private chat: [RFC](https://github.com/simplex-chat/simplex-chat/blob/stable/docs/rfcs/2025-03-07-group-knocking.md), [feature branch](https://github.com/simplex-chat/simplex-chat/pull/5797), [core](https://github.com/simplex-chat/simplex-chat/pull/5726), [iOS](https://github.com/simplex-chat/simplex-chat/pull/5851), [Android/desktop](https://github.com/simplex-chat/simplex-chat/pull/5816)
- Double-ratchet re-synchronization, restoring broken end-to-end encryption: [agent](https://github.com/simplex-chat/simplexmq/pull/774), [core](https://github.com/simplex-chat/simplex-chat/pull/2653), [iOS](https://github.com/simplex-chat/simplex-chat/pull/2663), [Android](https://github.com/simplex-chat/simplex-chat/pull/2666)
- Post-quantum end-to-end encryption in the chat protocol: [RFC](https://github.com/simplex-chat/simplex-chat/pull/3847), [core](https://github.com/simplex-chat/simplex-chat/pull/3859)
- TLS transport for the messaging protocol, with a server identity check: [feature branch](https://github.com/simplex-chat/simplexmq/pull/203), [certificate validation](https://github.com/simplex-chat/simplexmq/pull/234), [offline and online certificates](https://github.com/simplex-chat/simplexmq/pull/238), [old RSA/AES handshake removed](https://github.com/simplex-chat/simplexmq/pull/229)
- App lock with Face ID, Touch ID or Android biometrics: [simplex-chat#696](https://github.com/simplex-chat/simplex-chat/pull/696)
- Disappearing messages with custom timers: [core](https://github.com/simplex-chat/simplex-chat/pull/1561), [custom timers](https://github.com/simplex-chat/simplex-chat/pull/2423), [iOS](https://github.com/simplex-chat/simplex-chat/pull/2428), [Android](https://github.com/simplex-chat/simplex-chat/pull/2455)
- Notification metadata encrypted with a separate key, so the notification server can't read it: [simplexmq#410](https://github.com/simplex-chat/simplexmq/pull/410)
- Push notifications client agent, subscription supervisor and notification modes: [simplexmq#392](https://github.com/simplex-chat/simplexmq/pull/392)
- iOS push-notification reliability rework, several notifications per push: [agent](https://github.com/simplex-chat/simplexmq/pull/1378), [iOS](https://github.com/simplex-chat/simplex-chat/pull/5084)
- Network statistics per server: [agent](https://github.com/simplex-chat/simplexmq/pull/1202), [core](https://github.com/simplex-chat/simplex-chat/pull/4319), [iOS](https://github.com/simplex-chat/simplex-chat/pull/4321)
- Server operators and usage conditions: [iOS UI](https://github.com/simplex-chat/simplex-chat/pull/5114), [conditions APIs](https://github.com/simplex-chat/simplex-chat/pull/5147)
- Recent history sent to new group members: [simplex-chat#3519](https://github.com/simplex-chat/simplex-chat/pull/3519)
- Forwarding without revealing the source: [simplex-chat#3968](https://github.com/simplex-chat/simplex-chat/pull/3968)

</details>

**Other open source**
- TLS 1.3 support in the Haskell tls library's Finished-message API: [haskell-tls/hs-tls#445](https://github.com/haskell-tls/hs-tls/pull/445) (co-authored)
- Apache Spark: [SPARK-23503](https://github.com/apache/spark/pull/20936), [SPARK-23747](https://github.com/apache/spark/pull/20983)
