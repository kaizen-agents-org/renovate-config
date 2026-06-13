# Kaizen Agents Renovate Configuration

This repository stores shared Renovate defaults for `kaizen-agents-org`.

Renovate uses `default.json` as the organization's default onboarding preset
when the Mend Renovate GitHub App is installed for repositories in this
organization.

## Required Setup

1. Install the Mend Renovate GitHub App for `kaizen-agents-org`:
   <https://github.com/apps/renovate/installations/new>
2. Include this repository, `renovate-config`, in the installation.
3. Include every repository that should receive dependency update PRs:
   - `builder-agent`
   - `kaizen-loop`
   - `verifier`
   - `.github`
   - `coderabbit`
4. Let Renovate open onboarding PRs and merge the ones you want enabled.

## Default Behavior

- Uses Renovate `config:recommended`.
- Creates a Dependency Dashboard issue.
- Labels Renovate PRs with `dependencies`.
- Limits PR volume to two per hour and five concurrent PRs.
- Requires dashboard approval for major updates.
- Groups routine non-major updates.
- Waits three days before npm package updates.
- Runs lockfile maintenance before 5am on Mondays.

Automerge is intentionally not enabled by default.
