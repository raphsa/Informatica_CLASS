For each change in a `.md` or `.yml` file, the following commands has to be done:

```bash
jupyter-book build .
cp -r _build/html/* docs/
git add .
git commit -m "Message"
git push origin master
```