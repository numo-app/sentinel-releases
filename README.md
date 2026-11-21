# Sentinel releases

*[Leer en español](#español)*

Public downloads and automatic updates for [Sentinel](https://github.com/numo-app/sentinel),
the network security app for your computer.

- **Download**: open [the latest release](https://github.com/numo-app/sentinel-releases/releases/latest)
  and run `Sentinel_x.y.z_x64-setup.exe` (Windows 10/11, 64-bit).
- **Updates**: installed copies check this repository every few hours, or right away with
  *Settings > Check for updates*. Every installer is signed, and Sentinel verifies the
  signature before installing.

## How releases get here

1. In the `sentinel` repository, on the build PC: `.\scripts\release.ps1 -Version X.Y.Z -Notes "..."`.
2. The script builds and signs the installer, writes `latest.json` and pushes them to a
   `publish/vX.Y.Z` branch here.
3. The [Publish release](.github/workflows/publish.yml) workflow creates the GitHub Release
   and deletes the branch.

The updater endpoint used by the app is
`https://github.com/numo-app/sentinel-releases/releases/latest/download/latest.json`.

---

## Español

Descargas públicas y actualizaciones automáticas de [Sentinel](https://github.com/numo-app/sentinel).

- **Descargar**: abre [la última versión](https://github.com/numo-app/sentinel-releases/releases/latest)
  y ejecuta `Sentinel_x.y.z_x64-setup.exe` (Windows 10/11, 64 bits).
- **Actualizaciones**: las copias instaladas revisan este repositorio cada pocas horas, o al
  momento con *Ajustes > Buscar actualizaciones*. Cada instalador va firmado y Sentinel
  verifica la firma antes de instalar.
- **Publicar una versión**: en el PC de compilación, dentro del repositorio `sentinel`,
  `.\scripts\release.ps1 -Version X.Y.Z -Notes "..."`.
