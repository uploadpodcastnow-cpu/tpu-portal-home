# TPU Portal Homepages

One homepage design for every TPU client. Each client's content lives in its own file in the `clients` folder.

## Each client's link (paste into Assembly once)

```
https://USERNAME.github.io/tpu-portal-home/?client=CLIENTID
```

`CLIENTID` is the file name without `.json`, so `clients/kirk.json` → `?client=kirk`.

After that, any change you save in GitHub shows up in the portal within a minute or two. There's no need to touch Assembly again.

## Editing a client

Open `clients/<name>.json` in GitHub, click the pencil icon, edit and click **Commit changes**.

| Field | What it does |
|---|---|
| `firstName`, `showName` | Used in the welcome line and on the cover placeholder |
| `coverArt` | Image path, e.g. `assets/zach-cover.jpg` (upload images to `assets/`). Leave it as `""` to show the show name instead |
| `welcome` | `title`, `lead` (bold line) and `body` text |
| `video` | `title`, `text`, `poster` image and `embedUrl` (a YouTube/Vimeo/Loom *embed* link). Use `null` for no video |
| `links` | Quick-link buttons, shown in the order listed (see below) |
| `upcoming` | `{ "date": "Dec 3", "label": "..." }` items. Use `[]` to hide the section |
| `team` | `{ "name": "...", "role": "..." }` items. Use `[]` to hide the section |

### Link options

```json
{ "label": "Files", "sub": "Episodes & assets", "icon": "folder", "open": "portal", "url": "https://thepodcastupload.myassembly.com/apps/..." }
```

- `open: "portal"`: opens that tab inside the Assembly portal. To get the URL, open the portal as the client, click the tab and copy the address bar.
- `open: "external"`: opens in a new browser tab (Riverside, Frame.io, Podbean, YouTube Studio).
- `url: ""`: the button shows but does nothing yet.
- `icon`: the name of any file in `assets/icons/` (without `.svg`). For more icons, download them from tabler.io/icons (outline style).

## Adding a new client

1. Copy an existing file in `clients/` and save it as a new name, e.g. `clients/sarah.json`.
2. Edit the content.
3. In Assembly, add the homepage embed for that client using `...?client=sarah`.

## Important

This repository is public, so anyone who finds a link can read it. Don't put passwords, private notes or financial details in these files.
