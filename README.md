<div align="center">
<h1> LibMedium </h1>
<p>

**Privacy-focused proxy for medium.com**

</p>

[![Awesome Humane Tech](https://raw.githubusercontent.com/humanetech-community/awesome-humane-tech/main/humane-tech-badge.svg?sanitize=true)](https://github.com/humanetech-community/awesome-humane-tech)
[![Build](https://github.com/realaravinth/libmedium/actions/workflows/linux.yml/badge.svg)](https://github.com/realaravinth/libmedium/actions/workflows/linux.yml)
[![dependency status](https://deps.rs/repo/github/realaravinth/libmedium/status.svg)](https://deps.rs/repo/github/realaravinth/libmedium)
[![codecov](https://codecov.io/gh/realaravinth/libmedium/branch/master/graph/badge.svg)](https://codecov.io/gh/realaravinth/libmedium)

</div>

## Status

Usable. Should you run into a `HTTP 500 Internal Server Error`, please
file a bug report with the URL of the post you were trying to read and
the git commit hash of the build. Git commit hash can be obtained from
[/api/v1/meta/build](https://md.whateveritworks.org/api/v1/meta/build).

This proxy works by interacting with Medium's undocumented(probably
private but unauthenticated) API. So I've had to make assumptions and
tweak API schematics as I run into errors.

## Features

-   [x] proxy images
-   [x] proxy GitHub gists
-   [x] render posts
-   [x] syntax highlighting for gists
-   [ ] user pages(WIP)
-   [ ] RSS feeds

## Why?

Knowledge is the true wealth of humanity. If it weren't for our
ancestors, who chose to pass down their knowledge and experiences, we
would still be a primitive species. Whatever advancement that we as
a species have achieved is because we chose to share information.

To put a paywall on knowledge like that is both obscene and goes against
the very nature of humanity.

It is possible to run a sustainable publication business while still
respecting freedom. [LWN.net](https://lwn.net) is one of my favourite
publications that has been around forever. So it is possible. I hope
medium.com comes up with other, non-harmful ways to run a sustainable
business.

## Instances

| Instance                                                                  | Country | Provider          | Host                                     |
| ------------------------------------------------------------------------- | ------- | ----------------- | ---------------------------------------- |
| https://libmedium.batsense.net                                            | India   | Airtel            | @realaravinth                            |
| https://md.vern.cc                                                        | US      | Hetzner           | [~vern](https://vern.cc)                 |
| http://md.vernccvbvyi5qhfzyqengccj7lkove6bjot2xhh5kajhwvidqafczrad.onion/ | N/A     | Hetzner           | [~vern](https://vern.cc)                 |
| http://vernaqj2qr2pijpgvf3od6ssc3ulz3nv52gwr3hba5l6humuzmgq.b32.i2p/      | N/A     | Hetzner           | [~vern](https://vern.cc)                 |
| https://medium.hostux.net                                                 | France  | Gandi             | [hostux](https://hostux.net)             |


### Automatic Installs
```
https://github.com/WhateverItWorks/Watchtower
```

### €⁠20 [Hetzner Cloud](https://hetzner.cloud/?ref=eLtKhFK70n4h)

### Deploy with Docker

```
apt install git
git clone https://github.com/WhateverItWorks/my-libmedium-docker-compose.git md
cd md
nano config/default.toml
nano docker-compose.yml
docker-compose pull
docker-compose up -d
```
http://localhost:8080


### Deploy with Dockerfile
```
docker-compose up -d --build
```

## Security Audits:

- [Internet.nl](https://internet.nl/site/md.whateveritworks.org/)
- [HSTS Preload](https://hstspreload.org/)
- [SSL Labs](https://www.ssllabs.com/ssltest/analyze.html?d=md.whateveritworks.org)
- [Security Headers](https://securityheaders.com/?q=md.whateveritworks.org&hide=on&followRedirects=on)
- [pagespeed](https://pagespeed.web.dev/)
- [webbkoll](https://webbkoll.dataskydd.net/en)
- [ImmuniWeb](https://www.immuniweb.com/ssl/md.whateveritworks.org)
- [Hardenize](https://www.hardenize.com/report/md.whateveritworks.org/)
- [Mozilla.org](https://observatory.mozilla.org/)
- [report-uri.com](https://report-uri.com/home/tools)
- [check-your-website.server-daten.de](https://check-your-website.server-daten.de/?q=md.whateveritworks.org)
- [csp-evaluator.withgoogle.com](https://csp-evaluator.withgoogle.com/)
- [OpenWPM](https://github.com/openwpm/OpenWPM)
- [privacyscore.org](https://privacyscore.org)

Inspired by [Scribe - An Alternative Medium Frontend](https://sr.ht/~edwardloveall/scribe)
