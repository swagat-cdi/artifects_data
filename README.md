# Artifacts Sample Structure

This folder demonstrates a static, server-less sync package.

- Download `manifest.json` at app launch.
- Loop over `items[].files[].path` and download each file.
- Persist local `cursor` / `lastSyncAt` after successful sync.

Folder convention:

- `canvases/<category>/<canvasId>/regions.json`
- `canvases/<category>/<canvasId>/region_map.bin`

To add a new canvas:

1. Create a new folder under `canvases/<category>/<canvasId>/`
2. Add required files (`regions.json`, `region_map.bin`)
3. Append an entry in `manifest.json`
4. Bump `generatedAt`, `cursor`, and entry `updatedAt`
