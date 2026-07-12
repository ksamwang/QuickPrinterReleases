# QuickPrinter Releases

QuickPrinter public release catalog and update manifests.

GitHub Pages is published from the `main` branch `/docs` directory:

```text
docs/
├─ index.html
├─ updates/
│  └─ <channel>.json
└─ downloads/
   └─ <channel>/QuickPrinter-<Channel>-<Version>.zip
```

Packages and manifests are produced from the private QuickPrinter source repository:

```powershell
.\scripts\Publish-QuickPrinterRelease.ps1 `
    -Channel Pro `
    -Stage `
    -ReleaseRepoPath E:\SourceCode\C++\QuickPrinterReleases
```

After verifying the staged files, publish them with:

```powershell
.\scripts\Publish-QuickPrinterRelease.ps1 `
    -Channel Pro `
    -Publish `
    -ReleaseRepoPath E:\SourceCode\C++\QuickPrinterReleases
```

The update manifest contains the version, package URL, SHA-256, size and publication time for one channel. Alpha, Beta and Pro remain isolated.
