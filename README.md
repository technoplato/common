# common

Stuff I use in all projects

## Efficient Workflow Commands

This repository includes several efficient workflow commands to streamline development:

### Complete Workflow in One Command

```bash
DESCRIPTION="[Task ID]: [Description]" && \
SUMMARY="[One-sentence summary]" && \
git add . && \
git commit -m "$DESCRIPTION" && \
tree -I "node_modules|.git|build|dist|.next|.expo|.DS_Store" -a > docs/agent/file-structure.txt && \
git add docs/agent/file-structure.txt && \
git commit --amend --no-edit && \
REPO_URL=$(git remote get-url origin | sed 's/\.git$//') && \
COMMIT_HASH=$(git rev-parse HEAD) && \
echo "- $(date +%Y-%m-%d): $SUMMARY [Commit](${REPO_URL}/commit/${COMMIT_HASH})" >> .cursor-updates && \
git add .cursor-updates && \
git commit -m "Update .cursor-updates with commit link" && \
git push
```

This command:

1. Commits your changes with a descriptive message
2. Updates the file structure documentation
3. Amends the commit to include the updated file structure
4. Adds an entry to the .cursor-updates file with the commit link
5. Commits the updated .cursor-updates file
6. Pushes all changes to the remote repository

See the agent-flow.mdc file for more workflow commands and documentation.
