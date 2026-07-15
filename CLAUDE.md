# Soothing Solutions Massage Therapy — website

Static one-page site for Mary Irvine, LMT (Carmel, Indiana). Deployed via **GitHub Pages** from the `main` branch of `maryirvine347/maryirvine347.github.io`. Custom domain: `soothingsolutionsmassagetherapy.com` (via `CNAME`).

## Structure
- `index.html` — the entire site (inline CSS + JS, no build step).
- `hero-texture.jpg` — hero background image.
- `mary-headshot.webp` — Mary's photo in the "Meet Mary Irvine" about section.
- `CNAME` — custom domain for GitHub Pages.

## Standing rule — ALWAYS commit + push, never ask
After **any** change, however small, immediately:
1. `git add` + `git commit` with a clear message.
2. `git push origin main`.
3. Confirm it goes live and actually works (the live URL is https://maryirvine347.github.io — Pages builds take ~30–60s).

**Do NOT ask "should I commit/push?" — the answer is always yes.** Pushing to `main` is what deploys the live site. This is a non-negotiable rule set by the user. Only surface something if a push or verification step *fails*.

## Notes
- No local Node or Python available; preview locally with `.claude/serve.ps1` (PowerShell static server on port 5500).
- DNS/domain was mid-transfer from Webador → Squarespace; live custom domain may lag behind pushes until that completes.

## Custom domain — RESTORED & LIVE (2026-07-15)
The Webador→Squarespace transfer **completed 2026-07-15**. The `CNAME`
(`soothingsolutionsmassagetherapy.com`) is **restored** and the domain is **verified** to the
`maryirvine347` GitHub account (Settings → Pages → Verified domains). Note: while the CNAME was
removed during the transfer, a spammer briefly **squatted** the unclaimed domain on GitHub Pages;
verifying the domain (a `_github-pages-challenge-maryirvine347` TXT record in Squarespace DNS)
kicked them off. The apex **https://soothingsolutionsmassagetherapy.com serves the site**; `www`
was still provisioning at cutover.

**Lesson:** never leave `CNAME` removed once DNS points at GitHub's IPs — an unclaimed domain can be
squatted. If Pages 404s the domain ("Site not found"), re-save the custom domain in repo
Settings → Pages (remove → re-add). Enable **"Enforce HTTPS"** once the cert issues.
Backup remains at `.claude/CNAME.bak`.
