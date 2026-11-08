# Validation

- Baseline: main 9a5c71835e052e1ec1620bf7866b89f35c5367ae, isolated branch codex/contadino-focus-story.
- Jekyll build passed with installed Ruby 3.3 and the unchanged locked dependencies. Default Ruby 4 is incompatible with commonmarker in this site's existing dependency set.
- Browser checks at 1280, 390, and 320 CSS pixels: no horizontal document overflow. Inspected desktop hero, themes and devices; phone hero, responsive History, themes, and homepage Contadino panel.
- Every product screenshot loaded. Phone History uses the dedicated iPhone capture; desktop uses Mac History.
- All local asset and navigation targets in generated Contadino HTML resolve. Original support and policy destinations preserved.
- App Store descriptions: iOS 159 words / 930 characters; macOS 162 words / 942 characters; visionOS 162 words / 936 characters. No Watch/iPhone references on Mac or Vision Pro. No Contadino+ purchase paragraph.
- git diff --check passed. These checks were completed before publication. App Store submission and subscription mutations are outside this copy and website update.

## Device bezel follow-up

- Baseline: main e6607f033bc6aa25bad0e3ad25b14473edb5035e; branch codex/contadino-device-bezels.
- iPhone, iPad, Mac, and Watch captures now use responsive CSS hardware frames. The homepage Contadino image is framed too. visionOS remains unframed.
- Source screenshot files and user-facing copy are unchanged. The History frame switches from laptop to phone along with its existing responsive image source.
- Jekyll build and git diff --check passed. Browser inspection covered desktop (1280px), phone (390px), and narrow phone (320px); no horizontal overflow, all nine product images loaded, and the homepage frame rendered correctly.
- Impeccable detector completed with advisories for existing design-token drift and intentional hardware colors/radii; its rounded-border warning refers to the laptop's physical base, not a card.
- This follow-up is PR-only. Merge and production deployment require the user's explicit approval after review.

## Settings screenshot refresh (2026-11-08)

- Baseline: main `ee05c53`; branch `codex/refresh-contadino-settings-screenshots`.
- Refreshed all nine served Contadino images from native release captures of app commit `04eb7b0d14ebd06dcdc862da24e6343d1bbb0c19`, including the Settings move in `2a024bf`. iPhone and iPad now show Settings in the tab navigation. Mac retains its platform-specific Settings window/menu, so its main window correctly has Timer and History only.
- Preserved the current page copy, CSS, image dimensions, responsive art direction, device frames, and non-overlapping hero composition. The homepage inherits the refreshed iPhone image through product metadata.
- Vision uses the previously reviewed native crop (`x=480, y=320, width=2880, height=1620`). The Mac image remains a genuine window composition over sourced Sonoma wallpaper, not a full-desktop capture. No App Store headline compositions or invented interface pixels were used.
- All nine source captures matched their SHA-256 records. All nine optimized WebP outputs round-trip to the downsampled RGBA pixels exactly. Total served image bytes decreased from 10,211,606 to 6,623,816 (35.13%). Native image dimensions and transparent hardware edges are retained.
- Baseline and final Jekyll builds passed using Ruby 3.3, Bundler, and the unchanged locked dependency set. The existing optional `faraday-retry` middleware warning is non-fatal.
- Generated homepage and Contadino page checks passed: local targets resolve, all nine new asset references exist, reserved image dimensions match the files, and no stale Contadino PNG references remain in served HTML. `git diff --check` passed.
- All nine image outputs were visually inspected. Responsive browser QA and fresh page-review screenshots are pending because the Mac is locked and automatic unlock failed. Earlier browser checks and screenshots above describe prior revisions, not this refresh. No new browser pass is claimed.
- PR-only change. No merge or production deployment.
