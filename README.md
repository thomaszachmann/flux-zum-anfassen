# Flux zum Anfassen – Begleitcode

Begleitcode zum Buch **Flux zum Anfassen** – GitOps für Kubernetes mit Flux:
Bootstrap, Sources von Git bis OCI, Kustomization, HelmRelease, SOPS, Image
Automation, Notifications, Multi-Tenancy, CI und Plattform-APIs mit kro. Teil der Reihe
IT-Trainingslager von Thomas Zachmann.

Buchseite: https://it-trainingslager.de/buecher/flux

Der Code begleitet das Buch; Erklärungen und Übungen stehen im Buch. Dein Fleet-Repo
baust du im Buch selbst – hier liegt sein Stand am Ende jedes Tags zum Vergleichen und
die Dateien für den Wettkampf. Alle Schlüssel und Passwörter sind Laborwerte – nie in
Produktion verwenden.

Getestet mit k3s 1.37.2, Flux 2.10.0, Helm 4.3.1, SOPS 3.13.3, age 1.3.2 und kro 0.10.0.

## Inhalt

- `loesung/tagNN/` – Stand des Fleet-Repos (`apps/`, `infrastructure/`, `clusters/lab/`,
  ab Tag 12 `tenants/`) am Ende jedes Tags, ohne die von `flux bootstrap` erzeugten
  `gotk-*.yaml`. Ab Tag 6 liegt unter `charts/` das notes-Chart.
- `loesung/tag12/team/`, `loesung/tag14/team/` – die Artefakte der Teams
- `loesung/pruefung/` – Lösungen der Abschlussprüfung (Anhang B)
- `wettkampf/rundeN/` – Dateien, mit denen die Runden in Tag 15 beginnen

Die mit SOPS verschlüsselten Dateien (`secret*.yaml`) sind mit einem anderen
age-Schlüssel verschlüsselt als deine. Vergleiche sie deshalb nicht mit `diff`.

## Schnellstart

```bash
git clone https://github.com/thomaszachmann/flux-zum-anfassen.git ~/flux-lab/code
diff -r ~/flux-lab/fleet/apps ~/flux-lab/code/loesung/tag02/apps
```

Details stehen im Kapitel „Tag 0“ des Buchs.

## Lizenz

Code: MIT (siehe LICENSE). Buchtexte, Abbildungen und Cover sind nicht Teil dieses Repos
und nicht lizenziert.
