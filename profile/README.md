# OpenMCX — 3GPP Release 19 Mission Critical Services

Project OpenMCX is an open implementation of the **3GPP Release 19 Mission Critical Services (MCX)** which comprises **MCPTT** (mission-critical push to talk), **MCData** (mission-critical data) and **MCVideo**
(mission-critical video), with their common services, written from the 3GPP specifications. Everything runs in
containers, and every feature is exercised by automated scenarios in a fresh lab.

## Repositories

| Repository | What it holds |
|---|---|
| **[openmcx&#8209;server](https://github.com/openMCX/openmcx-server)** | The MCPTT, MCData and MCVideo servers (participating and controlling functions), the common services (IdMS, GMS, CMS, KMS, LMS, message store), the HTTP proxy, the user database, the lab tools, the regression scenarios and the tutorials |
| **[openmcx&#8209;client](https://github.com/openMCX/openmcx-client)** | The clients: the Android app, the dispatcher position in the browser, and `mcx-client`, the headless Linux MC client that the lab scenarios drive |
| **[openmcx&#8209;admin](https://github.com/openMCX/openmcx-admin)** | MCX Admin: MC user profiles, groups and rights in a web UI or from a spreadsheet, and client activation |

## Services

- **MCPTT**: Prearranged, chat, broadcast and ad hoc group calls with floor control; private calls in every
  commencement mode; emergency and imminent-peril calls and alerts; ambient listening, transfer and forwarding,
  functional aliases, regroups, location
- **MCData**: Short data (SDS), file distribution over HTTP and the media plane, IP connectivity, enhanced status,
  communication release, message store
- **MCVideo**: Group and private calls with transmission control, video push and pull, ambient viewing, emergency
- **Security**: OIDC sign-in, end-to-end protected media, payloads and XML signalling

## Try it

The **[Tutorials](https://github.com/openMCX/openmcx-server/blob/main/tutorials/README.md)** run the whole system on
one computer from the pre-built [Docker Hub images](https://hub.docker.com/u/openmcx). OpenMCX also supports cluster deployment based on Kubernetes Helm charts.

Debian packages are planned for the dispatcher and the headless Linux client, so that both can be installed natively,
without Docker.

## Status

This is the **Standalone Edition**: One MC system for all three services, on-network. Interconnection between MC
systems, MC migration, MC interworking and off-network (ProSe) operation are not part of the current OpenMCX version. OpenMCX is not an
interoperability-certified implementation; each repository documents its current limits.

## Licence

OpenMCX is licensed under the [GNU Affero General Public License v3.0 or later](https://github.com/openMCX/openmcx-server/blob/main/LICENSE);
a commercial licence is available from the OpenMCX authors. Third-party software and its licences are listed in each
repository's NOTICE.
