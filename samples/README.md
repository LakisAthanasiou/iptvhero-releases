# IPTV Hero setup file samples

Fill these in on a computer, copy them to the TV, and load them in IPTV Hero.
They save typing long keys and passwords with a remote.

**Keep filled-in files private.** They contain your passwords and keys. Don't
share or upload them, and delete them from the TV once loaded. IPTV Hero stores
the values encrypted inside the app; it does not need the files afterwards.

Save each file as plain UTF-8 text (any text editor). Keep the quotes and commas
exactly as they are — only replace the text between the quotes.

## 1. IPTV account — `test-credentials.json`

```json
{
  "name": "My IPTV account",
  "serverUrl": "http://your-provider.example:8080",
  "username": "your-username",
  "password": "your-password"
}
```

- `serverUrl`: the server address your provider gave you, starting with
  `http://` or `https://`, including the port if there is one. No username,
  password or `?…` in the address.
- `name`: any label you like.

**Load it:** copy the file into **Downloads/IPTVHero** on the TV (create the
folder if needed). In IPTV Hero choose **Add account → Load credentials from
file → Load from Downloads**. The form fills in; check it, then **Sign in**.
You can also use **Choose file** or **Choose setup folder** if your TV has a
file manager app.

## 2. Movie and series discovery (TMDB) — `service-settings.local.json`

```json
{
  "tmdb_api_key": "",
  "tmdb_read_access_token": ""
}
```

Optional. Adds posters, genres, trending titles and recommendations. Create a
free account at themoviedb.org, then open **Settings → API** to get credentials.
Fill in **exactly one** of the two fields:

- `tmdb_read_access_token` — the long "API Read Access Token" (preferred), or
- `tmdb_api_key` — the shorter "API Key".

Leave the other one as `""`.

**Load it:** **Settings → Discovery → Load TMDB setup file**, then **Choose file**
or **Choose setup folder** (the folder must contain a file with exactly this name).

## 3. Subtitles (OpenSubtitles) — `opensubtitles-settings.json`

```json
{
  "api_key": "",
  "username": "",
  "password": ""
}
```

Optional. Lets you search and download subtitles during playback. Create a
consumer API key at opensubtitles.com (account → API consumers) and put it in
`api_key` (required).

`username` and `password` are your opensubtitles.com login and are optional:
fill in **both or neither**. Without a login you get a small daily download
allowance; logging in usually raises it.

**Load it:** **Settings → Subtitles → Load OpenSubtitles setup file**, then **Choose file**
or **Choose setup folder**.

## 4. Layout and categories — `iptv-hero-config.json`

A configuration backup: Home layout, audio/subtitle languages, picture mode,
refresh interval, and which categories and channels are shown or hidden. It
contains **no** passwords, server addresses, Favorites or viewing history.

Categories and channels are matched **by name**, so this sample only helps if
your provider uses the same names. Nothing is applied until you review it.

**Load it:** sign in first and let the library finish loading. Then
**Settings → Transfer → Export / import configuration → Import configuration**, choose the
file, select the sections you want and **Apply selected sections**. Make your
own backup the same way with **Save to Downloads**.

---

Each IPTV Hero beta works for 14 days. Install new versions from
**Settings → About → Check for updates**, or from this repository's Releases.
