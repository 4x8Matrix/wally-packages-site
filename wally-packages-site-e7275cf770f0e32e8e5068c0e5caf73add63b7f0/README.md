# Package Index Site

The Repository that is responsible for handling and hackily updating the documentation site for the `Package-Index` hosted on my GitHub account.

- https://github.com/4x8Matrix/Package-Index

---

## A brief overview

When a commit is made to the `Package-Index`'s Master branch, a `workflow` action is dispatched into this repository using [this workflow action](https://github.com/peter-evans/repository-dispatch).

Next, the workflows inside of this repository will call `lune moonwave-build` and the `.lune/moonwave-build` luau script will use `moonwave` to compile the latest module documentation. 

Lastly, the workflow will commit and push these changes to the Repository, from there - vercel will update the production endpoint.

## Why.. just why!?

It's both a challenge and a chaotic mess, but I love that! If anyone has a better solution to what i'd a massive hack, open up and issue and i'd be happy to discuss it!
