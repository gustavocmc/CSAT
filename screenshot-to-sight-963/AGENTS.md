<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- All CSAT data access goes through src/lib/csat-api.ts (currently demo/in-memory); swap its bodies for real backend calls without changing page code.
- Report/notification sending (Slack, Teams, e-mail) goes through src/lib/reports-api.ts adapters with a DEMO_MODE flag; pure message builders live in reports-format.ts and reuse csat-stats so numbers match the panel.
