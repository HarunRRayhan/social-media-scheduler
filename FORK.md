# Fork-only changes

This fork of [gitroomhq/postiz-app](https://github.com/gitroomhq/postiz-app) deploys from `main` to sm.harun.dev. Everything below is ours and must survive upstream syncs (merge `upstream/main`, never force-push). Each change is marked `FORK:` in the code.

| Change | Files |
|---|---|
| No Google/Apple/Farcaster/wallet sign-in buttons | `apps/frontend/src/components/auth/login.tsx`, `register.tsx` |
| Invite-only signup: with `DISABLE_REGISTRATION=true`, a signed invite for the same email can still register | `apps/backend/src/services/auth/auth.service.ts`, `apps/frontend/src/app/(app)/auth/page.tsx` |
| Logout always shown in Settings (upstream hides it during `?onboarding`) | `apps/frontend/src/components/layout/settings.component.tsx` |

Deploy notes: Railway builds `Dockerfile.dev` (`RAILWAY_DOCKERFILE_PATH`), `DISABLE_REGISTRATION=true`.
