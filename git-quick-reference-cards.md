# Quick Reference Cards: Git & CI/CD for BI Engineers

---

## Card 1: Git Vocabulary Cheat Sheet

| Term | What It Means | BI Analogy |
|------|---------------|------------|
| **Repository (Repo)** | Container holding all your workspace items and their complete history | Like a project folder that remembers every version of every file ever |
| **Commit** | A saved snapshot of your work with a description | Like "Save As" but it remembers ALL previous saves too |
| **Branch** | A parallel line of development | Like having a separate copy of the workspace to experiment in |
| **Main Branch** | The primary "blessed" version everyone builds from | The official Development workspace version |
| **Feature Branch** | Your personal workspace for a specific change | Your sandbox to build something without affecting others |
| **Pull/Sync** | Get the latest changes from the repo | Download what teammates have committed |
| **Push** | Send your committed changes to the repo | Upload your work so others can see it |
| **Merge** | Combine changes from one branch into another | Integrate your finished feature into Main |
| **Pull Request (PR)** | A formal request to merge your branch | "Please review and approve my changes" |
| **Conflict** | Two people changed the same thing differently | Git can't auto-decide which version wins |
| **Clone** | Create a local copy of a repository | Download the entire project to work with |

### Key Insight
> **Git stores snapshots, not differences.** Each commit captures the complete state of everything. Git is just smart about not duplicating unchanged items.

---

## Card 2: How to Commit Your Changes in Fabric

### Before You Start Working
```
☐ Open your workspace in Fabric
☐ Check the Source Control panel for pending updates
☐ If updates exist → Click "Update all" first
☐ Now you have the latest version → Start your work
```

### When You're Ready to Commit

**Step 1: Open Source Control**
- Click the **Source Control** icon in the workspace toolbar
- Or find it in the workspace settings menu

**Step 2: Review Your Changes**
- Items with changes show a status indicator
- Determine which changes are yours vs other developer changes

**Step 3: Select Items to Commit**
- Check the boxes next to items you want to include
- Group related changes together (one feature = one commit)
- Don't mix unrelated changes in a single commit
- Don't commit other developers' work

**Step 4: Write Your Commit Message**
- Be specific about WHAT changed and WHY
- See Card 3 for message examples

**Step 5: Click "Commit"**
- Your changes are saved to the Git repository
- Others can now see your work after they sync

### Commit Frequency Guide

| Situation | Commit? |
|-----------|---------|
| Finished a logical piece of work | ✅ Yes |
| End of day, work in progress | ✅ Yes (note it's WIP in message) |
| Every tiny edit | ❌ Too frequent |
| After a week of changes | ❌ Too infrequent—commit sooner! |
| Before pulling updates from others | ✅ Yes—save your work first |

---

## Card 3: Writing Good Commit Messages

### The Formula
```
[Action] [What] [Where/Why]
```

### ✅ Good Examples for BI Work

**Semantic Model Changes**
- `Add YTD and QTD calculations to Sales model`
- `Fix incorrect join between Orders and Customers tables`
- `Add Budget vs Actual measures for Finance reporting`
- `Rename fields to match business glossary standards`
- `Optimize Sales model by removing unused columns`

**Report Changes**
- `Create Regional Sales dashboard with drill-through`
- `Fix date slicer not filtering all visuals on Executive Summary`
- `Add tooltip showing order details to Revenue chart`
- `Update company logo and apply new brand colors`

**Data Pipeline / ETL Changes**
- `Add data quality validation step for customer imports`
- `Fix timezone conversion error in timestamp processing`
- `Add incremental refresh logic to Orders pipeline`

**Work in Progress**
- `WIP: Building inventory analysis report - visuals complete`
- `WIP: Sales model restructure - measures done, relationships pending`

### ❌ Bad Examples (Avoid These)

| Bad Message | Why It's Bad |
|-------------|--------------|
| `updates` | What updates? To what? |
| `fixed stuff` | What stuff? What was broken? |
| `changes` | This says nothing |
| `asdf` or `test` | Not helpful to anyone |
| `final version` | There's never a final version |
| `v2` | Version of what? |

### Pro Tips

1. **Write in present tense**: "Add filter" not "Added filter"
2. **No period at the end**: Commit messages are titles, not sentences
3. **Keep it under 50 characters** if possible (for readability in logs)
4. **If you need more detail**: First line = summary, blank line, then longer explanation

---

## Card 4: Feature Branch Workflow Checklist

### 🚀 Starting a New Feature

```
☐ Navigate to your personal feature workspace
☐ Verify it's connected to your feature branch (not Main!)
☐ Sync/Update to get the latest from your branch
☐ Confirm: What is the goal of this feature?
```

### 💻 While Working on Your Feature

```
☐ Make changes in your feature workspace only
☐ Commit frequently with clear messages
☐ Keep commits focused (one logical change per commit)
☐ Periodically sync with Main to stay current:
    - Ask lead/admin to update your branch from Main
    - Or learn to do this yourself in Azure DevOps
```

### ✅ When Your Feature is Complete

```
☐ Final testing in your feature workspace
☐ All changes committed (nothing pending)
☐ Commit messages are clear and professional
☐ Update from Main one last time (resolve any conflicts)
☐ Create Pull Request (see Card 5)
☐ Notify reviewer(s) that PR is ready
```

### 🔍 During Review

```
☐ Respond to reviewer comments promptly
☐ Make requested changes in your feature workspace
☐ Commit the fixes (reference the feedback in message)
☐ Let reviewer know when ready for re-review
```

### 🎉 After Merge is Complete

```
☐ Verify your changes appear in Dev workspace
☐ Delete or archive your feature workspace (per team policy)
☐ Celebrate! 🎉
```

### Branch Naming Convention
Follow your team's standard. Common patterns:
- `feature/sales-ytd-calculations`
- `feature/jsmith-inventory-report`
- `bugfix/date-filter-issue`

---

## Card 5: Pull Request (PR) Creation Guide

### What's a Pull Request?
A Pull Request is your formal request to merge your feature branch into Main. It's where review and approval happen.

### Creating a PR in Azure DevOps

**Step 1: Navigate to Pull Requests**
- Go to Azure DevOps → Your Project → Repos → Pull Requests
- Click **"New Pull Request"**

**Step 2: Select Branches**
- **Source**: Your feature branch (e.g., `feature/sales-report`)
- **Target**: `main`

**Step 3: Fill Out the PR Form**

| Field | What to Write |
|-------|---------------|
| **Title** | Clear summary of the feature (similar to a commit message) |
| **Description** | See template below |
| **Reviewers** | Add required reviewers (leads, peers, Release Manager) |
| **Work Items** | Link related Azure DevOps work items if applicable |

### PR Description Template

```markdown
## Summary
Brief description of what this PR accomplishes.

## Changes Made
- Added X measure to Sales semantic model
- Created new report page for regional analysis
- Updated date table to include fiscal calendar

## Testing Done
- Verified calculations against Excel source
- Tested all slicers and filters
- Checked cross-filter behavior

## Screenshots (if applicable)
[Paste any relevant screenshots of new visuals]

## Notes for Reviewer
- Pay special attention to the YTD logic
- Connection parameter needs to be set for Test environment

## Checklist
- [ ] Changes tested in feature workspace
- [ ] Commit messages are clear
- [ ] No unintended changes included
```

### Responding to Review Feedback

| Feedback Type | Your Action |
|---------------|-------------|
| Requested change | Make the fix, commit, comment "Done" |
| Question | Answer the question in the PR comments |
| Suggestion (optional) | Decide to accept or explain why not |
| Approval | 🎉 Wait for merge or merge if you have permission |

### PR Etiquette

✅ **Do:**
- Respond to feedback within 24 hours
- Keep PR scope focused (one feature/fix per PR)
- Be open to suggestions

❌ **Don't:**
- Create PRs with dozens of unrelated changes
- Ignore reviewer comments
- Merge without required approvals

---

## Card 6: Troubleshooting Common Issues

### "I have changes but can't commit"

| Symptom | Likely Cause | Solution |
|---------|--------------|----------|
| Commit button disabled | Need to pull updates first | Click "Update all" then try again |
| "Conflict" warning | Someone else changed the same item | See conflict resolution below |
| Nothing shows as changed | Changes not saved in Fabric | Save your work in the designer first |

### "I pulled updates and my changes disappeared"

**Don't panic!** Your changes are likely in one of these places:
1. Check if changes were committed before pulling (they're safe in Git)
2. If uncommitted, check the Source Control panel for merge results
3. Ask admin to help recover from Git history if needed

### "There's a conflict"

**Step 1: Understand what conflicted**
- Azure DevOps or Fabric will show which items conflict

**Step 2: Determine the right version**
- Talk to the other person who made changes
- Decide together whose changes should "win" or how to combine

**Step 3: Resolve**
- For most BI items, you'll choose one version
- May need to manually re-apply some changes after

**Step 4: Complete the merge**
- Mark conflict as resolved
- Commit the resolution

**When to escalate:**
- You're unsure whose changes are correct
- The conflict involves complex model logic
- You've spent more than 15 minutes stuck

### "I committed to the wrong branch"

**If you haven't pushed yet:**
- Ask lead/admin for help reverting

**If you already pushed:**
- Don't panic—this is fixable
- Notify lead/admin immediately
- They can revert the commit or move changes to correct branch

### "I need to undo my last commit"

**Before pushing (local only):**
- Ask lead/admin—they can reset the branch

**After pushing:**
- Create a new commit that reverses the changes
- Or ask admin to help revert
- Don't try to "delete history"—Git doesn't work that way

---

## Card 7: Daily & Weekly Habits

### Every Day

**Start of Day (2 minutes)**
```
☐ Open your workspace
☐ Check Source Control for pending updates
☐ Pull/Update if there are changes from others
```

**Before Making Changes**
```
☐ Confirm you're in the right workspace/branch
☐ Know what you're trying to accomplish
```

**End of Day (5 minutes)**
```
☐ Commit work in progress (even if not finished)
☐ Use "WIP:" prefix if incomplete
☐ Don't leave uncommitted changes overnight
```

### Every Week

**Monday**
```
☐ Review any PRs waiting for your review
☐ Check if your feature branches need updates from Main
```

**Friday**
```
☐ Ensure all work is committed before weekend
☐ Update any in-progress PRs with status
☐ Clean up: any old feature branches to delete?
```

### Monthly

```
☐ Review your commit history—are messages clear?
☐ Retrospective: what's working, what's confusing?
☐ Share learnings with teammates
```

---

## Quick Command Reference (Azure DevOps)

*For those comfortable with the web interface, here's where to find things:*

| Action | Where to Find It |
|--------|------------------|
| View commit history | Repos → Commits |
| View branches | Repos → Branches |
| Create Pull Request | Repos → Pull Requests → New |
| View file contents | Repos → Files → Navigate to file |
| Compare branches | Repos → Branches → "..." menu → Compare |
| View PR status | Repos → Pull Requests → Active |

---

*Version 1.0 | Last Updated: January 2025*
