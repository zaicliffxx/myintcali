# MyInt Cali

Minimal calisthenics coaching site for [myintcali.online](https://myintcali.online).

## Local preview

Open `index.html` in a browser, or run:

```bash
npx serve .
```

## Deploy to Netlify

1. Push this folder to a GitHub repository.
2. Sign in at [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import an existing project**.
3. Connect GitHub and select the repo.
4. Build settings (defaults are fine for static HTML):
   - **Build command:** leave empty
   - **Publish directory:** `.` (root)
5. Deploy. You'll get a `*.netlify.app` URL.

## Connect myintcali.online (Namecheap)

1. In Netlify: **Site configuration** → **Domain management** → **Add a domain** → `myintcali.online`.
2. Netlify shows DNS records. In Namecheap → **Domain List** → **Manage** → **Advanced DNS**, add:

   | Type  | Host | Value                          |
   |-------|------|--------------------------------|
   | A     | `@`  | `75.2.60.5` (Netlify load balancer) |
   | CNAME | `www`| `your-site-name.netlify.app`   |

   Use the exact values Netlify shows in your dashboard if they differ.

3. Wait for DNS (often 15–60 minutes). Netlify provisions HTTPS automatically.

## Customize

- Edit copy in `index.html`
- Update email in the contact section
- Colors and fonts in `styles.css` (`:root` variables)
