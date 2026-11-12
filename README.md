# tomspecs-web-content

The deployed static tree of **https://tomspecs.dev**. Whatever is on `main` is live within
five minutes: bigbeast pulls it (`tomspecs-web-content-pull.timer`, `git pull --ff-only`,
user `www-deploy`) into `/srv/www/tomspecs.dev`, served by Apache (`Use StaticSite tomspecs.dev`).
A rewritten history makes the pull fail instead of resetting the site - publish with
ordinary commits, never force-push.

The current pages (home, method, tools, Impressum; dark theme, the TomSpecs bear logo in
`assets/`) are the initial set from al_the_bear todo `tsmapex1` (2026-11-12). The site
itself belongs to the **tomspecs_web** quest, which will replace them, likely with a
generated site published into this repository the way `enterprise-web-content` is.

GitHub Actions is off for this repository (no CI on al-the-bear repositories).
