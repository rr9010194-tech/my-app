# Using shared-ui as a git subtree

This project uses the `shared-ui` folder as a git subtree from https://github.com/rr9010194-tech/shared.

## How to update shared-ui from the shared repo

```
git subtree pull --prefix=shared-ui https://github.com/rr9010194-tech/shared main
```

## How to push changes in shared-ui back to the shared repo

```
git subtree push --prefix=shared-ui https://github.com/rr9010194-tech/shared main
```

## How to add shared-ui as a subtree in another repo (e.g., my-app-2)

1. Remove any existing `shared-ui` folder in the target repo:
   ```
   rm -r shared-ui
   git add .
   git commit -m "Remove local shared-ui to prepare for subtree"
   ```
2. Add the subtree:
   ```
   git subtree add --prefix=shared-ui https://github.com/rr9010194-tech/shared main
   ```
3. Push changes:
   ```
   git push
   ```

## Notes
- Always commit your work before running subtree commands.
- Use the above commands to keep `shared-ui` in sync across projects.

