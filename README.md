# tomspecs-web-content

The deployed static tree of **https://tomspecs.dev**. Whatever is on `main` is live within
five minutes: bigbeast pulls it (`tomspecs-web-content-pull.timer`, `git pull --ff-only`,
user `www-deploy`) into `/srv/www/tomspecs.dev`, served by Apache (`Use StaticSite tomspecs.dev`).
A rewritten history makes the pull fail instead of resetting the site - publish with
ordinary commits, never force-push.

The pages are hand-written HTML: home, method, tools, get started, docs and the Impressum,
with the dark theme and the TomSpecs bear logo in `assets/`. The method page follows
`tom_specs_project_flow.md` (in `tom_ai_build`), the package list follows the release set
published on pub.dev, and the get-started commands were run against the published packages. The site
itself belongs to the **tomspecs_web** quest, which will replace them, likely with a
generated site published into this repository the way `enterprise-web-content` is.

GitHub Actions is off for this repository (no CI on al-the-bear repositories).
