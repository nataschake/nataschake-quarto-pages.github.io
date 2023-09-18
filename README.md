# Publishing Quarto RevealJS presentations at github.com using Github workflows
This repository stores Quarto RevealJs presentation created with GitHub Actions tool:
The site is live at https://nataschake.github.io/quarto-pages/

The general pipeline is described in details [here](https://quarto.org/docs/publishing/github-pages.html).
Step-by-step guide is as follows:

0. Install quarto following [instructions](https://quarto.org/docs/get-started/)
1. Clone repository `https://github.com/nataschake/quarto-pages`.
2. Change presentation.qmd to fit your needs, incl. adding images to `img` folder.
3. apply `quarto render` in the root directory. It will create docs folder with presentation.html in it.
4. Create branch `gh-pages` with

```
git checkout --orphan gh-pages
git reset --hard # make sure you've committed changes before running this!
git commit --allow-empty -m "Initialising gh-pages branch"
git push origin gh-pages
```

4. Commit presentation.qmd to branch `main`
5. apply `quarto publish gh-pages`, being in `main` branch.
6. Your site will appear at `your-repo/quarto-pages/presentation.html`

`https://nataschake.github.io/quarto-pages/` will resolve to 
`https://nataschake.github.io/quarto-pages/presentation.html#/title-slide`
