# Muslim Wedding Invitation Template

A responsive, static wedding invitation website built with plain HTML, CSS, and JavaScript. It needs no package installation or build step. The included names, dates, venue, coordinates, and RSVP number are placeholders; replace them before sharing your invitation.

## Features

- Animated cover and invitation details
- Configurable couple, family, ceremony, address, date, and RSVP details
- Dates and countdown derived from the event configuration
- Non-interactive OpenStreetMap map tiles with a red location marker and attribution
- Google Maps directions link
- Optional background music

## Project files

- `index.html` — page, styles, invitation configuration, and behavior
- `invitation-cover.svg` — generic cover artwork
- `invitation-details.svg` — generic details-page artwork

Keep the artwork beside `index.html`, or update its paths in the HTML if you move it. No audio file is included; add your own audio file if you enable music.

## Customize the invitation

1. Open `index.html` in a text editor.
2. Find the `invitationConfig` object near the start of the script section.
3. Replace its values with your own:
   - `bride` and `groom`: names, parent names, and addresses
   - `events`: event titles, venues, dates, and optional times
   - `location`: map destination as `latitude,longitude`, map zoom, caption, and notice
   - `countdown`: which event to count down to and its time
   - `rsvp`: WhatsApp phone number, message template, and button label
   - `music`: whether music is enabled, its filename, volume, and looping behavior
   - `page`: the invitation's headings, labels, and closing text
4. Use dates in `YYYY-MM-DD` format and times in 24-hour `HH:MM` format. Include the country code in the WhatsApp phone number, without a `+`.
5. Replace the map coordinates with the venue's latitude and longitude, separated by a comma.
6. To use different artwork, replace the SVG files while keeping their filenames, or update the paths in `index.html`. To use music, add an audio file beside `index.html` and set `music.enabled` to `true`.
7. Review all text, links, media, and location details before sharing or publishing.

## Preview locally on Windows

1. Open PowerShell in the project folder.
2. Start a local web server:

   ```powershell
   py -m http.server 8000
   ```

3. Open `http://localhost:8000` in a browser.
4. Stop the server with `Ctrl+C` when finished.

Python is only needed for this optional local preview. The deployed page itself has no build or install step.

## Pull a copy and make changes

After the repository is published, clone it with Git:

```powershell
git clone https://github.com/<owner>/<repository>.git
cd <repository>
```

Replace `<owner>` and `<repository>` with the GitHub account and repository name. To get updates after cloning:

```powershell
git pull
```

Edit `invitationConfig` and replace the artwork or music as needed. Preview the changes locally, then save them back to your fork or repository:

```powershell
git add index.html README.md invitation-cover.svg invitation-details.svg
git commit -m "Customize wedding invitation"
git push
```

Only stage files you changed. If you add an audio file, stage it too, for example with `git add background_music.mp3`.

## Publish with GitHub Pages

1. Push the project to a GitHub repository.
2. In that repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and the `/(root)` folder, then save.
5. Wait for GitHub Pages to finish deploying and open the URL shown in the Pages settings.
6. After future edits, commit and push them; GitHub Pages will deploy the update.

The map tiles and web fonts load from external services, so visitors need an internet connection to see those parts. OpenStreetMap attribution is included on the map.

## Reuse and privacy

This template uses generic placeholder information and artwork. Replace the sample values and review all media before publishing a personalized invitation; names, phone numbers, addresses, and precise coordinates may be personal information.

This repository currently has no license. Public visibility alone does not grant permission to reuse its code or media.
