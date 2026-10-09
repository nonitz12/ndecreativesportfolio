# Adding work to a category

1. Put a web-ready MP4 in `public/projects/videos/`.
2. Put its thumbnail in `public/projects/thumbnails/`.
3. Put a short muted MP4 preview in `public/projects/previews/`.
4. Add an entry to `src/data/works.ts` with its title, duration, three URLs, and
   `category`: `films`, `reels`, or `motion`. The `films` category is labeled
   “Long-form” in the interface. The same carousel displays only
   the videos in the selected category.

Edit category introductions and contact links in `src/data/portfolio.ts`.
To add graphic designs, place images in `public/projects/designs/` and add
their title, image URL, and descriptive alt text to `graphicWorks` in that file.
The Graphic Design page renders those images as a gallery; clicking opens
the full image. Empty collections show a short coming-soon message.
The Works dock icon opens the Google Drive URL defined in `src/pages/index.astro`.

The initial grouping is provisional: Edits 01–02 are Motion Graphics and
Edits 03–04 are Long-form. Change their categories when needed.

URLs start with `/projects/`, not `/public/projects/`. Use simple filenames
such as `event-film.mp4`; avoid `#`, which has a special meaning in URLs.

The current entries are matched by number from the original Desktop `projects`
folder. Replace `Edit 01` through `Edit 04` with your real project titles.
The website uses 1080p H.264/AAC copies with fast-start metadata, and separate
six-second silent previews. Your source videos were not changed.

The gallery loads thumbnails first. Hovering a card can load its small preview;
clicking loads the full video. Leaving the player stops and unloads it.
Full videos are served with the site, so check your host's file-size and storage
limits before deployment. External direct MP4 URLs can also go in `works.ts`.
