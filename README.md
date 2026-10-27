# StudyFlow — Study Planner SaaS

StudyFlow is a student-friendly study planner project with a freemium SaaS business model. It is built as a front-end demo using HTML, CSS, and vanilla JavaScript.

## Features

- Dark, responsive productivity dashboard
- Add and delete tasks, due dates, subjects, and priorities
- Mark tasks complete and filter the task list
- Weekly study schedule with add/remove sessions
- Focus timer with 25, 45, and 60-minute presets
- Dashboard statistics and weekly study-minute chart
- Free, Plus, and Pro pricing tiers
- Simulated subscription upgrade flow (no real payments)
- Profile name and weekly goal settings
- Browser `localStorage` persistence
- PostgreSQL example schema in `database/schema.sql`

## Run locally

1. Download and unzip the project.
2. Open `index.html` in a modern browser.
3. No build step, package manager, or server is required for the demo.

For a better local development experience, use VS Code with the Live Server extension and open `index.html` through Live Server.

## SaaS model

| Plan | Price | Example limits/features |
|---|---:|---|
| Free | ₹0 | Up to 5 active tasks, 3 subjects, focus timer, basic progress |
| Plus | ₹149/month | Unlimited tasks/subjects, advanced insights, custom goals |
| Pro | ₹299/month | Plus features, exam countdowns, schedule templates, reports |

These prices are sample project assumptions, not a live offer. The current UI demonstrates plan selection only; limits are not enforced as a production backend would enforce them.

## Demo vs production

### Works in this front-end demo
- Task and schedule interactions
- Focus timer and study-minute totals
- Dashboard updates
- Browser-local persistence
- Demo plan upgrade confirmation

### Not implemented / needs a backend or provider
- Real accounts, authentication, password reset, and cross-device sync
- Server-side data storage and authorization
- Actual subscription billing, renewals, invoices, and cancellations
- Enforcement of paid plan limits
- Email reminders, push notifications, or calendar integrations
- Production security, monitoring, privacy policy, and terms

The checkout is intentionally simulated. It does not collect card data, call a payment gateway, or charge money. To launch a real paid SaaS, integrate a server-side subscription provider (for example, Razorpay or Stripe where supported), verify payment webhooks on the server, and never put secret keys in browser JavaScript.

## Suggested production architecture

- Frontend: HTML/CSS/JavaScript (or React later)
- API: Node.js + Express
- Database: PostgreSQL
- Authentication: secure server-managed sessions or a trusted auth provider
- Billing: payment provider checkout + verified webhooks
- Hosting: static frontend hosting plus a server/database host

## Database schema

`database/schema.sql` is a PostgreSQL reference schema for users, plans, subscriptions, tasks, study sessions, and focus logs. It is not connected to the browser demo.

## Sample data

The app starts with a few sample tasks and study sessions. New tasks, sessions, settings, and focus totals are stored in localStorage for that browser. Use browser developer tools to clear local storage and reset the demo.

## GitHub publishing

1. Sign in at https://github.com.
2. Click **New repository**.
3. Repository name suggestion: `studyflow-study-planner-saas`.
4. Set visibility to Public if you want to share it as a portfolio project.
5. Create the repository.
6. Upload `index.html`, `style.css`, `app.js`, `README.md`, and the `database` folder, or push the unzipped folder using Git.
7. Open **Settings → Pages**.
8. Under **Build and deployment**, choose **Deploy from a branch**.
9. Select `main` and `/ (root)`, then save.
10. After deployment finishes, the site URL is usually `https://YOUR-USERNAME.github.io/studyflow-study-planner-saas/`.

GitHub Pages hosts the front-end demo only. It does not run a Node.js API or PostgreSQL database.

## License

For educational use. Add a license file if your course or repository requires one.
