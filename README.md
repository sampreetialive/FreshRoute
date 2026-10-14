# FreshRoute — Perishable Intelligence

FreshRoute is a responsive MVP for smarter perishable-produce distribution planning. The repository includes a public-facing landing page and the planning workspace.

## Files

- `index.html` — responsive landing page, feature sections, workflow, impact preview, and login/sign-up demo at the bottom.
- `app.html` — FreshRoute planning workspace with Overview, Inventory, Distribution Planner, Discount Studio, Impact & Analytics, What-if Simulator, and Methodology.

## Run locally

1. Open `index.html` in a modern browser, or use VS Code with the Live Server extension.
2. Use the links to open `app.html` for the workspace.
3. Internet access is used for Google Fonts, Lucide icons, and Chart.js CDN assets in the workspace. Core planning interactions run in the browser.

## Landing page and account prototype

The landing page uses Geist Mono for headings, JetBrains Mono for interface/body text, and Space Mono for labels and metadata. It uses green for positive actions, red for urgency, and yellow for watch states. It includes responsive navigation, animated preview elements, feature cards, workflow sections, impact preview, and login/sign-up tabs at the bottom.

The login/sign-up form is a **front-end demonstration only**. It stores a demo profile in browser local storage and does not securely authenticate users. Do not enter a real or reused password. Production authentication requires a backend, secure password hashing, session management, and appropriate security controls.

## Workspace interfaces

- **Overview:** inventory metrics, alerts, dispatch priorities, destination snapshot, and baseline comparison.
- **Inventory:** add, edit, delete, search, and filter batches. Data persists in browser local storage.
- **Distribution planner:** deterministic urgency-and-margin heuristic; respects stock, destination demand/capacity, and shelf-life feasibility; provides explanations.
- **Discount studio:** editable markdown rules and at-risk batch recommendations.
- **Impact & analytics:** baseline comparison for estimated spoilage, demand fulfilment, net revenue, and constraint violations; export allocation CSV.
- **What-if simulator:** vary demand, delivery delay, transport capacity, and handling time, then rerun the planner.
- **Methodology:** model, assumptions, evaluation definitions, and limitations.

## Model limitations

- Data is simulated and intended for demonstration, not real operational decisions.
- Shelf life is an estimate and is not a food-safety guarantee.
- The allocation method is a deterministic heuristic, not a mathematically proven global optimum.
- Baseline and proposed plan use the same simulated inventory, demand, price, and cost assumptions.
- Estimated spoilage and net revenue use simplified MVP accounting assumptions; refine these with validated operational data before real use.
- Discount suggestions are rules-based estimates and do not guarantee a sale or override food-safety guidance.

## Deploy with GitHub Pages

1. Upload `index.html`, `app.html`, and `README.md` to the root of a GitHub repository.
2. Open **Settings → Pages**.
3. Under build/deployment, select **Deploy from a branch**, branch `main`, folder `/ (root)`, then save.
4. Wait for GitHub Pages to publish the site.
