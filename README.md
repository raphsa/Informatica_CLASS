For each change in a `.md` or `.yml` file, the following commands has to be done:

```bash
jupyter-book build .
cp -r _build/html/* docs/
git add .
git commit -m "Message"
git push origin master
```

In case of problems in correctly visualize the Jupyter Book:

```bash
touch docs/.nojekyll
git add docs/.nojekyll
git commit -m "Add .nojekyll to disable Jekyll and fix styling"
git push origin master
```