# Bible Orbit Static Site

This folder is ready to publish with GitHub Pages for `https://bibleorbit.org/`.

## Pages

- `/` - small Bible Orbit homepage
- `/privacy/` - Google Play privacy policy URL
- `/support/` - support and account deletion contact page

## Recommended GitHub Pages setup

1. Create a public GitHub repository named `bibleorbit-site`.
2. Copy the contents of this folder into that repository root.
3. In the repository, go to `Settings -> Pages`.
4. Set `Build and deployment` to deploy from the `main` branch root.
5. Set the custom domain to `bibleorbit.org`.
6. Enable `Enforce HTTPS` after GitHub finishes issuing the certificate.

## Squarespace DNS for GitHub Pages apex domain

Keep the Resend email DNS records. Replace only the website A records for `@` with:

```text
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
```

Optional but recommended IPv6 records:

```text
AAAA  @  2606:50c0:8000::153
AAAA  @  2606:50c0:8001::153
AAAA  @  2606:50c0:8002::153
AAAA  @  2606:50c0:8003::153
```

For `www`:

```text
CNAME  www  <your-github-username>.github.io
```

After DNS and GitHub Pages finish propagating, Google Play can use:

```text
https://bibleorbit.org/privacy/
```
