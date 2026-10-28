# Ark News theme pages — maintainer notes

This package contains two self-contained HTML pages for Dreamweaver. Each page includes its own CSS, so neither requires a separate stylesheet or build step. The pages share the Ark News masthead, color palette, typography, footer, keyboard focus style and background treatment. Their main layouts differ: the homepage leads with one article and audio; Featured People uses portrait-led profiles with two card treatments.

## Files

- `index.html` is the homepage with the El Niño article and SoundCloud feature.
- `featuredpeople.html` is the profile index with Mayor Joe Ayala and Gregory Montoya. Its full profiles expand with native `<details>` controls and do not require JavaScript.

Each story includes a visible source panel with three linked records. The climate article links to NOAA, the Colorado Climate Center and CoCoRaHS. The Mayor Ayala profile links to City of La Junta records. The Gregory Montoya profile links to Steam product and community records. Interview quotations and personal history are attributed to the interview; external links provide context and public product or government information.

## Page map: Featured People

- `<head>` contains page metadata and all page CSS.
- `:root` defines the design tokens. Keep the values aligned with `index.html` while styles remain embedded in each file.
- `.site-header` uses the Rocky Mountains masthead image and a dark overlay.
- `.site-nav` holds the shared navigation. `aria-current="page"` marks the current page.
- `.page-intro` contains this page's title and introduction.
- `.feature-grid` creates the profile layout. The Mayor Ayala card spans seven columns; the Gregory Montoya card spans five and uses a dark treatment.
- `.story-media` contains each portrait and its caption. Keep meaningful descriptions in each image's `alt` text.
- `.story-full` contains the expandable article. Edit the matching `<details>` content; keep the `<summary>` as the visible control.
- `@media` rules stack the cards and navigation at tablet and phone widths.
- `.site-footer` contains the publication footer.

## Maintenance notes

The Dropbox masthead and portrait images, SoundCloud player and Steam link are external resources. They require an internet connection. If an image is moved into the site folder, replace its URL with a relative path such as `Images/filename.jpg`.

Navigation also links to `local.html`, `about.html` and `contact.html`, which are not included yet. The Gregory Montoya profile includes an editor's update reflecting Steam's Aug. 21, 2026 release listing; the earlier Dec. 2026 target remains attributed to the July 1 interview. Other interview statements remain attributed to their speakers and should be checked against original recordings or notes before further factual edits.
