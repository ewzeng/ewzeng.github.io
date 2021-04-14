#### Notes to Self [Current]

To be able to update notes without having to update the repository, I have decided to link my notes to drive. In drive, I can update a pdf (without breaking the sharing link) by uploading a pdf of the same name. Drive also deletes version history after 30 days, so I don't have to worry about the accumulation of space. (Additionally, I can manually delete version history.)

#### Notes to Self [Deprecated]

Hosting this website on GitHub pages runs into the following problem:

- The notes will be continuously updated. However, this means I will be pushing lots of pdfs to this GitHub repo. Because GitHub tracks all history, the older versions of the notes will be stored somewhere in the repo's history, leading to a large accumulation of space.

To save space, I would like to be able to scrub older versions of my notes. I did some research, but it seems that this is somewhat difficult to do in general (GitHub seems to not always delete everything, even if it's not in the repo history).

However, because I am the only author of this repo, there is an easy hack solution. Once in a while, do this:

1. Delete this remote repository.
2. Recreate this remote repository again (use same name).
3. Delete `.git` folder in local repository. Run `git init`, `git add .` and `git commit`. 
4. Set remote of local repo to this. Then `git push` everything.