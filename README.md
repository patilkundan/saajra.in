# मराठी बायोडाटा मेकर: Phase 1

The `/create-biodata` form: a fully interactive, browser-only Marathi biodata form.
No backend, auth, database, payments or PDF generation yet (those are Phase 2).

## Run

```bash
npm install
npm run dev        # http://localhost:3000  (redirects to /create-biodata)
```

Other scripts: `npm run build`, `npm run start`, `npm run lint`, `npx tsc --noEmit`.

## Structure

```
app/create-biodata/page.tsx     route
components/biodata/             form sections, photo/God-image/crop, custom headings & fields
components/ui/                  Input, Textarea, Select, RadioGroup, FieldShell, Button, Modal, ConfirmDialog
data/biodataOptions.ts          dropdown option lists (Marathi labels)
data/godImages.ts               predefined header images (swap files in public/god-images)
lib/biodata/                    defaults, Marathi labels, preview builder (hides empty fields)
lib/validation/biodataSchema.ts Zod schema for the whole form
lib/image/                      file validation, canvas crop
types/biodata.ts                BiodataData and nested types
```

## Adding real God images later

1. Put the file in `public/god-images/`.
2. Add an entry to `GOD_IMAGE_OPTIONS` in `data/godImages.ts`.

The current files are original placeholder graphics, not the reference site's artwork.
