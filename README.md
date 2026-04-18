# howtofindaboyfriend.com

Static two-page pitch site for the screenplay **How to Find a Boyfriend**.

## Pages

| URL                                   | File                     | Notes                                               |
| ------------------------------------- | ------------------------ | --------------------------------------------------- |
| `howtofindaboyfriend.com/`            | `index.html`             | General version (no Tubi-specific quote).           |
| `howtofindaboyfriend.com/for-anjali`  | `for-anjali/index.html`  | Custom version with Anjali Sud pull quote. `noindex`. |

The `/for-anjali` URL works cleanly on every major static host because it's served as `for-anjali/index.html`.

## Deploy (any of these)

### Vercel (easiest)
```bash
npx vercel --prod
```
Then add the `howtofindaboyfriend.com` domain in the Vercel dashboard.

### Netlify
Drag-and-drop the whole folder at https://app.netlify.com/drop, or:
```bash
npx netlify deploy --prod --dir .
```

### GitHub Pages
Push to a repo, enable Pages on the main branch root. Point `howtofindaboyfriend.com` at it via a `CNAME` file.

### Cloudflare Pages
Connect the repo, build command: *(none)*, output directory: `/`.

## Local preview

```bash
python3 -m http.server 8000
```
- http://localhost:8000/
- http://localhost:8000/for-anjali/

## Notes

- The `/for-anjali` page is marked `noindex,nofollow` so it won't appear in search results — only people with the link will find it.
- Both pages share the same design system; edit colors in the `:root` block at the top of each file.
