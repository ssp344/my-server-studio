# Lesson 01 Specification

## STUDIO-001 - Launch a tested calculator on an existing server

**Status:** Calculator deployed and verified on November 2, 2026.

## Agreed result

My goal was to launch the supplied calculator image on my existing DigitalOcean server using Docker and Traefik.

I used my existing `hosting-web` Docker network and configured a new HTTPS hostname. I did not replace Traefik or my existing Production and QA websites.

- **Public calculator:** https://calc.shiv-is373.xyz
- **Deployment:** New calculator launch
- **GitHub issue:** https://github.com/ssp344/my-server-studio/issues/1
- **Docker network:** `hosting-web`
- **Agreed scope:** Deploy the supplied calculator without changing existing services
- **Remaining work:** Final checks, pull request, CI verification, and merge

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Calculator website | https://calc.shiv-is373.xyz |
| Hosted deployment | Passed |
| Image and commit verification | Passed |
| HTTPS verification | Passed |
| Multiplication test | 6 × 7 = 42, HTTP 200 |
| Division by zero test | HTTP 400 |
| Invalid numeric input test | HTTP 422 |
| Existing Docker containers | Four checked, unchanged |
| Runtime evidence | [studio/evidence.json](studio/evidence.json) |
| Learning summary | [LEARNING.md](LEARNING.md) |
| GitHub issue | https://github.com/ssp344/my-server-studio/issues/1 |
| Prepared local checks and GitHub CI | Pending |
| Pull request and merge | Pending |

## Limitations

The calculator is a supplied Docker image. I did not build the application or create its CI/CD pipeline.

The automated checks confirmed selected container states and API behavior. They do not prove that the whole server is secure.

My separate pre-plan request-path prediction was not recorded before deployment. This missing record is disclosed in LEARNING.md.

Private SSH information and raw server configurations will not be published.
## Optional instructor history

The records below are background, not steps to repeat. Their original anchors
remain here so earlier links continue to work.

## HOST-001 · Keep the Traefik dashboard private

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-001--keep-the-traefik-dashboard-private).

## HOST-002 · Controlled host maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-002--controlled-host-maintenance).

## HOST-003 · Companion image security maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-003--companion-image-security-maintenance).
