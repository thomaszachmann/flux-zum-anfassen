# Flux hands-on – Companion Code

Companion code for the book **Flux hands-on** (German edition: *Flux zum Anfassen*) – GitOps for
Kubernetes with Flux: bootstrap, sources from Git to OCI, Kustomization, HelmRelease, SOPS, image
automation, notifications, multi-tenancy, CI and platform APIs with kro. Part of Thomas
Zachmann's IT Drills series.

Book page: https://itdrills.com/books/flux · German edition: https://it-trainingslager.de/buecher/flux

The code accompanies the book; explanations and exercises are in the book. You build your fleet
repo yourself as you work through the book – this repo holds its state at the end of each day for
comparison, plus the files for the competition. All keys and passwords are lab values – never use
them in production.

Tested with k3s 1.37.2, Flux 2.10.0, Helm 4.3.1, SOPS 3.13.3, age 1.3.2 and kro 0.10.0.

## Contents

- `loesung/tagNN/` – state of the fleet repo (`apps/`, `infrastructure/`, `clusters/lab/`,
  from Day 12 `tenants/`) at the end of each day, without the `gotk-*.yaml` files generated
  by `flux bootstrap`. From Day 6, `charts/` contains the notes chart.
- `loesung/tag12/team/`, `loesung/tag14/team/` – the teams' artifacts
- `loesung/pruefung/` – solutions to the final exam (Appendix B)
- `wettkampf/rundeN/` – files the rounds of Day 15 start with

The SOPS-encrypted files (`secret*.yaml`) are encrypted with a different age key than
yours, so don't compare them with `diff`.

## Quick start

```bash
git clone https://github.com/thomaszachmann/flux-zum-anfassen.git ~/flux-lab/code
diff -r ~/flux-lab/fleet/apps ~/flux-lab/code/loesung/tag02/apps
```

Details are in the book's "Day 0" chapter.

## License

Code: MIT (see LICENSE). Book text, figures and cover are not part of this repo and are not licensed.
