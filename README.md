# Quarto listing search and sort issue

Sometimes when using a "listing" the sort and search functionality doesn't always behave
as expected. The unexpected behavior is non-deterministic


## How I created this repo

1. Create the project
   ```
   quarto create-project demo-sort-issue --type=website
   ```
1. Change the `index.qmd` to a "table"-type listing
1. Create the `items` dir and populate with 4 markdown files with numbered titles
1. Remove `about.qmd`


## How to reproduce this issue

1. `quarto preview`
1. In your browser on the index page, try searching for `1`, `2`, `3`, and `4`
   separately.
1. At least one of these searches will not actually cause any filtering. If this doesn't
   happen, delete `.quarto` and `_site` directories and start over. Each time, the
   behavior may be different. E.g. the first time searching for `1` may be ineffective,
   and next time searching for `4` may be ineffective. You may also observe issues with
   sorting, e.g. item number 3 displaying before item number 4.
