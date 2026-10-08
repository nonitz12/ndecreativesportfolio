# NDE Creatives — local learning project

## Open in VS Code
1. Install a current Node.js LTS release with npm.
2. Extract this ZIP, then open the `nde-creatives` folder in VS Code.
3. Open Terminal > New Terminal. Run:

```sh
npm install
npm run dev
```

Open the local URL printed by Astro. Leave the terminal running while editing.
Save a file to see your changes in the browser. Press Ctrl+C to stop.

Recommended VS Code extension: Astro (the official Astro language extension).

## Understand the files
- `src/pages/index.astro`: homepage content, project data, HTML, and browser interactions.
- `src/styles/global.css`: Tailwind import and custom visual styling, animation, and responsive rules.
- `public/logo.png`: your original uploaded logo, unchanged.
- `public/`: place thumbnails, videos, and other public assets here. Use `/filename` in page URLs.
- `astro.config.mjs`: Astro configuration and Tailwind integration.
- `package.json`: dependencies and available commands.
- `package-lock.json`: pins installed dependency versions; keep it.

## First small exercise
Find `Good stories.` in `src/pages/index.astro`, change the headline, and save.
Then find `--blue:#526bff` in `src/styles/global.css` to change the accent color.
Try one change at a time and watch the result.

## How the page works
The section between the opening `---` lines runs during the build. It holds
project data and imports the stylesheet. The HTML below renders the page.
The `<script>` near the bottom runs in the visitor's browser: it controls
scroll reveals, project dialogs, the motion study, and editing-stage buttons.

Tailwind is installed through its Vite plugin. Much of this version uses
custom CSS for the visual design. You can also use Tailwind utilities in HTML,
for example `class="mt-6 flex gap-4"`.

Typography uses the device's native system font; SF Pro font files are not bundled.
Icons come from Lucide. No database or login is required.

## Content still to personalize
The project card visuals are typography treatments, not actual project thumbnails.
The editing lab is an interface demo, not a real before-and-after video.
Project buttons open descriptions and link to your existing Google Drive folder.
Contact links to your Facebook profile. Replace it with your preferred contact.
Add your actual videos, thumbnails, and project descriptions next.

## Check before hosting
```sh
npm run build
npm run preview
```

`npm run build` creates the static `dist` folder. `npm run preview` lets you
inspect that production output locally. This ZIP contains no hosting identity
or credentials, so you can choose your own hosting later.

## Future updates
Apply updates file by file. Ask for the exact filename, code to replace, and
an explanation. Keep a backup or use Git before larger changes. Do not overwrite
personalized files with an entire newer ZIP unless you intend to replace them.
