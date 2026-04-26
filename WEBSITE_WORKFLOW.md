# Website Workflow

## Preview Locally

From PowerShell:

```powershell
cd "C:\Users\leona\Desktop\PHD\Website\leonardendrizzi.github.io"
bundle exec jekyll serve -w
```

Then open:

```text
http://127.0.0.1:4000/
```

For specific pages:

```text
http://127.0.0.1:4000/research/
http://127.0.0.1:4000/teaching/
```

Leave the terminal open while previewing. Stop the preview with `Ctrl+C`.

## Publish

After editing and checking the local preview:

```powershell
git status
git add .
git commit -m "Update website"
git push
```

The published site should update at:

```text
https://leonardendrizzi.github.io
```

It can take a minute or two for GitHub Pages to rebuild.

## If Git Asks About Safe Directory

If Git shows a "dubious ownership" or "safe.directory" error, run:

```powershell
git config --global --add safe.directory "C:/Users/leona/Desktop/PHD/Website/leonardendrizzi.github.io"
```

Then try the Git command again.

## Config Note

Keep `_config.yml` using the live site URL:

```yml
url: https://leonardendrizzi.github.io
baseurl: ""
```

You do not need to change this to `localhost` for local preview. `bundle exec jekyll serve -w` handles the local preview automatically.
