# Profile README setup

A 2020-era maximalist GitHub profile README (typing SVG, badges, stats, streak,
trophies, activity graph, contribution snake). Built for
`github.com/ibuild-ai`.

## 1. Create the special repo

1. Go to <https://github.com/new>
2. Repository name **must be exactly** `ibuild-ai` (same as your username).
3. Tick **Public**, then **Add a README file** → Create.
4. Replace the generated `README.md` with the one in this folder.

> GitHub only renders a profile README when the repo name matches the username exactly.
> Your old handles `TrippleA001` and `ibuiildaiproducts` redirect, but every widget
> must use the current handle: **`ibuild-ai`**.

## 2. Add the snake

Copy `.github/workflows/snake.yml` into the repo at the same path, commit, then:

1. **Settings → Actions → General → Workflow permissions** → select **Read and write**.
2. **Actions** tab → *Generate Snake* → **Run workflow**.

It creates an `output` branch with the two SVGs. The README already points at:

```
https://raw.githubusercontent.com/ibuild-ai/ibuild-ai/output/github-contribution-grid-snake.svg
https://raw.githubusercontent.com/ibuild-ai/ibuild-ai/output/github-contribution-grid-snake-dark.svg
```

If the snake shows as broken, the run hasn't finished yet; wait for the green check.

## 3. Verify the widgets

Open the rendered profile and check each card loads. These are third-party services
and they rate-limit or sleep:

| Widget | Service | If broken |
|---|---|---|
| Stats / top langs | `github-readme-stats.vercel.app` | Usually a cold start. Reload in a minute |
| Streak | `streak-stats.demolab.com` | Reload |
| Trophies | `github-profile-trophy.vercel.app` | Reload |
| Activity graph | `github-readme-activity-graph.vercel.app` | Reload |
| Typing | `readme-typing-svg.demolab.com` | Check the `lines=` URL encoding |
| Profile views | `komarev.com/ghpvc` | Reload |

## 4. Things to customise

- **Quote at the bottom**: your own closing line. Keep it short; it's the last thing a recruiter reads.
- **`About me` YAML block**: update `building:` as your focus shifts.
- **Featured work**: swap a card when a project changes. Each card is a `<td>`; keep the
  two-column `<tr>` structure or the table breaks.
- **Tech icons**: edit the `i=` list at `skillicons.dev` (comma-separated slugs).
- **Theme**: everything is `tokyonight`. Alternatives that fit this era: `radical`,
  `dracula`, `synthwave`, `blue-green`.

## 5. What I deliberately left out

- **WakaTime card**: needs the WakaTime app installed and a public API key in the URL.
- **Tweet/Spotify cards**: need extra services; add only if you use them.
- **Skill percentage bars**: the classic 2020 move, but they're meaningless numbers.
  The skillicons row does the same job without lying.
- **"Currently learning" marquee**: pure clutter.

## 6. Optional upgrades

- **Pinned repos:** pin exactly six: Sama, Faultline, Pick Me, Ziki, Zedu Whimsical, AfriProEdu.
  TechDojo stays unpinned; it's a credential, not a portfolio piece.
- **Repo social previews:** Settings → Social preview, upload a 1280×640 image per repo.
  This is what makes a profile look curated rather than assembled.
- **Bio field:** `Data · AI · Product. Building evidence, not certificates. Lagos 🇳🇬`
