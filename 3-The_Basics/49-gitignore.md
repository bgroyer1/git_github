# .gitignore

- You may have files that you want in your project folder, but do not want to be tracked/included in commits
- The .gitignore solves this
- You create a .gitignore file in the root directory, and add file names
- You just have to add the file name, not the entire path!

```git
    <filename>
    *.<filextension>
    *.jpg
    !includethis.jpg
    !
```

- the star will ignore **all** files that have a matching extension at the end
- In this example, all jpg files will be ignored
- The exclamation point serves as a "include this" for that individual file, so includethis.jpg will still be tracked, even though the rest are being ignored