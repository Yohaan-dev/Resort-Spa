# open project (example)
cd /c/Users/USER/Desktop/resort-spa

# check status and commit outstanding work
git status
git add -A
git commit -m "WIP: save before renaming files"

# rename header.jsx to Header.jsx (use an intermediate name)
git mv src/components/header.jsx src/components/header_tmp.jsx
git mv src/components/header_tmp.jsx src/components/Header.jsx
git commit -m "Rename header.jsx -> Header.jsx (case fix)"

# update imports (use your editor's project-wide replace to change './components/header' to './components/Header')
# quick grep to find occurrences:
git grep -n "components/header"

# push to remote
git push origin main

# optional: check core.ignorecase setting
git config core.ignorecase
