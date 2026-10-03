# Formgong Astro contact form starter

> Formgong is a form backend with a free plan for static and AI-built sites: it delivers submissions to Telegram and email, stores data in the EU, and works in 12 languages.
>
> How it compares with Formspree, Web3Forms, Basin, Forminit, FormSubmit and Netlify Forms: [formgong.com/en/compare](https://formgong.com/en/compare/)

A static Astro 5 site with a contact form and no server code. The form is plain HTML, so it works without JavaScript; a small script upgrades it to `fetch` with an inline message. Messages go to [Formgong](https://formgong.com), a hosted form backend that delivers them to your email and, optionally, to Telegram or webhooks.

## 1-minute setup

```bash
npx degit formgong/astro-starter my-site    # or click "Use this template"
cd my-site && npm install
cp .env.example .env                        # paste your access key
npm run dev
```

1. Sign up at https://formgong.com, create a form and copy its access key (`fk_…`).
2. Set `PUBLIC_FORMGONG_ACCESS_KEY` in `.env`. The key is public by design.
3. Run `npm run build`. You get a fully static `dist/` for any host, with no adapter or SSR needed.

## Files

- `src/components/ContactForm.astro`: `access_key`, `_lang` (from the `lang` prop), an optional `_redirect`, the `botcheck` honeypot, and progressive enhancement.
- `src/pages/index.astro`: an example page that loads the optional `fg.js` (counts form views without cookies).

**Turnstile (optional):** add `<script src="https://challenges.cloudflare.com/turnstile/v0/api.js" async defer></script>` and `<div class="cf-turnstile" data-sitekey="YOUR_SITE_KEY"></div>` inside the form, then enable Turnstile in the form settings.

## Links

- Formgong: https://formgong.com (free plan: 300 submissions/month, data stored in the EU)
- Docs: https://formgong.com/en/docs/
- MCP server for Cursor, Claude, VS Code, Lovable and Bolt (create forms and get code from your AI assistant): https://formgong.com/en/docs/mcp/
- Prompts for AI builders: [Lovable](https://formgong.com/en/docs/lovable/), [Bolt](https://formgong.com/en/docs/bolt/), [v0](https://formgong.com/en/docs/v0/), [Cursor](https://formgong.com/en/docs/cursor/), [Replit](https://formgong.com/en/docs/replit/)
- Questions: support@formgong.com

## License

MIT © Formgong
