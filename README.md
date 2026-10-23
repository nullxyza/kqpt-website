# KQPT marketing website

A responsive, buildless website for King, Queen, Police, Thief. Includes supplied artwork, six role introductions, Classic and Evidence mode guides, a game overview, support email, app and website privacy policy and website terms. No JavaScript or package installation required.

## Preview

Run `python -m http.server 8000` in this directory and visit http://localhost:8000.

## Host with GitHub Pages

1. Create a GitHub repository and upload this project, including `.github/workflows/pages.yml`, or push this checkout to its remote. The workflow runs on `main`; adjust it if using another branch.
2. In the repository, open **Settings → Pages → Build and deployment → Source → GitHub Actions**. This one-time setup is required before the workflow can deploy; if a run fails with `Get Pages site failed` or a 404, select **GitHub Actions** as the source and rerun it.
3. Push to `main` or manually run **Deploy GitHub Pages** from the Actions tab. The deployment supplies the public URL.

All local asset and page links are relative, so the site works at both a repository subpath and a custom domain. The workflow publishes only the public files.

## Before a production launch

- Google Play: https://play.google.com/store/apps/details?id=com.visualmagixshop.kqpt
- YouTube: https://youtu.be/TIDhH4QR_mY?si=2I1gsU1jQlgtkDnL
- Both supplied links appear in the hero and download section.
- Confirm the app's data collection, Google OAuth scopes and use of Google user data, third-party SDKs, analytics, ads, data sharing, retention, security, age audience, and deletion process. Replace the clearly marked app app and website privacy policy in `privacy.html` with an accurate policy. Remove its `noindex` metadata after review.
- The terms cover both app and website. Confirm the publisher identity and review legal wording before release.
- Support contact: visualmagix10@gmail.com.
- The supplied poster contains release and feature claims; verify they match the actual app before launch.

## Custom domain and OAuth

Configure your owned domain in GitHub Pages and add the DNS records GitHub supplies. Enable HTTPS. Follow Google's current ownership and OAuth verification instructions, then use your real homepage, privacy policy and terms URLs in Branding. Do not use `google.com` as your authorized domain. Website creation alone does not complete domain or OAuth verification.

References: [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site), [Google homepage requirements](https://support.google.com/cloud/answer/13807376?hl=en), [Google production policy compliance](https://developers.google.com/identity/protocols/oauth2/production-readiness/policy-compliance?hl=en).

## Gameplay content source

Website rules were checked against the local `police-theif-game` project: `lib/models/role.dart`, `lib/services/game_service.dart`, `lib/providers/local_game_provider.dart`, the in-app rules in `lib/screens/menu/main_menu_screen.dart`, host/join screens, and `lib/features/spy_tasks/spy_task_constants.dart`. Character artwork was copied from that project's `assets/images/` folder. This reflects the local source; confirm the published Play Store version matches before making release-specific claims.

## Legal content review — 24 October 2026

Reviewed the app's `privacy_policy.txt`, in-app privacy and terms screens, `docs/privacy-and-security-readiness.md`, dependencies, Android manifest, splash sign-in, Play Games service, and settings reset implementation. The website now covers app and website behavior, local data, camera, network discovery, secure connection credentials, Google-hosted XP leaderboard, Google Fonts, support and deletion controls.

Differences requiring app follow-up: the app still points to the Google Sites privacy URL. After this site has a public URL, update that link and the Google Play/Cloud listings to the same policy. The app's old language about opt-in sign-in is less precise than its startup sign-in attempt. Its terms contain assertions of statutory compliance, blanket consent and a Grievance Officer that were not established by the source; the website does not repeat those assertions. No app files were changed in this website task. The local project version is 1.0.3+4; this review does not confirm the shipped store binary or certify legal compliance.
