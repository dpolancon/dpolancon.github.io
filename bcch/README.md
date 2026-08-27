# bcch/ -- GENERATED, DO NOT EDIT

This directory is the published render of the BCCh regional data publication
programme. It is written by `scripts/12_deploy_site.py` in the `bcch-data-repo`
repository and is overwritten on every deploy.

Editing anything here is pointless -- the next deploy discards it -- and
dangerous, because the audit that guarantees these pages agree with the
underlying data runs against the source, not against this copy.

To change a page, change the pipeline:

    python scripts/09_build_theme_panels.py     # panels from real BCCh data
    python scripts/10_generate_site.py          # .qmd from the panels
    quarto render                               # from the site worktree
    python scripts/11_audit_site.py             # coherence checks
    python scripts/12_deploy_site.py            # this directory

Source: https://github.com/dpolancon/bcch-data-repo
