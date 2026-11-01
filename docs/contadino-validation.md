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
