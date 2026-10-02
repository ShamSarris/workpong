# workpong.com

## What is it?

Simple web application to track table tennis matches, statistics, and rankings.

## Repository Layout + Tech Stacl

The front end is served via the Vercel CDN. It is simple HTML/SCSS/JS. The database is a relational DB on supabase. The API is served via vercel serverless functions.

```
workpong/
├── public/                  # served by the CDN exactly as-is
│   ├── index.html
│   ├── css/styles.css
│   └── js/app.js            # minimal fetch('/api/...') calls
├── api/                     # every file here becomes an endpoint
│   └── example/
│       ├── index.js         # GET, POST   /api/example
│       └── [id].js          # PATCH, DELETE /api/example/:id
├── lib/                     # shared server code, never routed
├── supabase/migrations/     # schema + RLS policies, versioned in git
├── tests/
├── .github/                 # CODEOWNERS, ci.yml, PR/issue templates
├── package.json             # needs "type": "module"
├── vercel.json              # optional: security headers, cleanUrls
└── .env.example             # variable names only, no values
```

## Contributing

Work with the development team to discuss a new feature or task. Use feature branches and have your work reviewed prior to merging with main.