# Visual Resources Guide for Git & CI/CD Training

This document provides links to high-quality visual resources and documentation that complement your BI Engineer training program. Use these for training slides, handouts, and self-paced learning.

---

## 🎯 Quick Summary: Where to Find What

| Topic | Best Resource |
|-------|---------------|
| Fabric Git Integration Overview | Microsoft Learn - Git Integration |
| Deployment Pipelines | Microsoft Learn - Deployment Pipelines |
| Branching Concepts | Atlassian Git Tutorials |
| Interactive Git Learning | Learn Git Branching |
| Diagramming Tools | Mermaid.js, draw.io |

---

## Official Microsoft Fabric Documentation (with Diagrams)

### Git Integration

**Overview of Fabric Git Integration**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration
- Contains: Architecture diagrams, supported items list, workspace-to-repo relationship visuals
- Best for: Phase 1 training, understanding the connection model

**Git Integration Process**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-integration-process
- Contains: Sync direction diagrams, permission matrices, workflow illustrations
- Best for: Understanding commit/update flow, troubleshooting sync issues

**Managing Branches in Workspaces**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/git-integration/manage-branches
- Contains: Branch-out workflow diagrams, feature workspace illustrations
- Best for: Phase 3 training on branching

**Git Source Code Format**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/git-integration/source-code-format
- Contains: Repository structure diagrams, file format examples
- Best for: Understanding what gets stored in Git

### Deployment Pipelines

**Introduction to Deployment Pipelines**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/intro-to-deployment-pipelines
- Contains: Three-stage pipeline diagrams, pairing concept visuals
- Best for: Phase 2 training fundamentals

**Getting Started with Deployment Pipelines**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/get-started-with-deployment-pipelines
- Contains: Step-by-step screenshots, pipeline creation visuals
- Best for: Hands-on training walkthroughs

**Understanding the Deployment Process**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/understand-the-deployment-process
- Contains: Content flow diagrams, dependency handling visuals
- Best for: Deeper understanding of what happens during deployment

**CI/CD Workflow Options**
- URL: https://learn.microsoft.com/en-us/fabric/cicd/manage-deployment
- Contains: Multiple workflow pattern diagrams, Git-to-deployment flow charts
- Best for: Understanding different release strategies

---

## General Git Learning Resources (with Excellent Visuals)

### Interactive Learning

**Learn Git Branching** ⭐ Highly Recommended
- URL: https://learngitbranching.js.org/
- Type: Interactive tutorial with animated visualizations
- Best for: Engineers who learn by doing; shows commits and branches animated in real-time
- Use case: Self-paced learning, team workshops

**Atlassian Git Tutorials**
- URL: https://www.atlassian.com/git/tutorials
- Contains: Well-illustrated guides on all Git concepts
- Key pages:
  - Branching: https://www.atlassian.com/git/tutorials/using-branches
  - Gitflow Workflow: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
  - Feature Branch Workflow: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
- Best for: Conceptual explanations with clear diagrams

**Git Handbook by GitHub**
- URL: https://guides.github.com/introduction/git-handbook/
- Contains: Simple visual explanations of Git fundamentals
- Best for: Absolute beginners

### Video Resources

**Git & GitHub Crash Course for Beginners** (Traversy Media)
- Platform: YouTube
- Length: ~30 minutes
- Best for: Visual learners who prefer video

**Microsoft Learn Training Modules**
- Search: "Introduction to Git" on Microsoft Learn
- URL: https://learn.microsoft.com/en-us/training/modules/intro-to-git/
- Contains: Interactive exercises within browser
- Best for: Structured learning paths

---

## Diagramming Tools for Creating Your Own Visuals

### Mermaid.js (Recommended for Git Diagrams)

**Mermaid Live Editor**
- URL: https://mermaid.live
- Use: Create and export Git workflow diagrams
- Why: Native support for gitGraph diagrams (see included diagrams file)

**Mermaid GitGraph Documentation**
- URL: https://mermaid.js.org/syntax/gitgraph.html
- Contains: Syntax guide, examples, customization options
- Best for: Creating branch/merge visualizations that match your actual workflow

### draw.io / diagrams.net

**draw.io Online Editor**
- URL: https://app.diagrams.net
- Use: General-purpose diagramming, Git workflow templates available
- Why: Free, exports to multiple formats, works offline

**Git Workflow Templates for draw.io**
- URL: https://www.drawio.com/blog/gitflow-diagram
- Contains: Step-by-step guide to creating gitflow diagrams
- Includes: Template you can customize

**GitHub Template for Git Branching Diagrams**
- URL: https://gist.github.com/bryanbraun/8c93e154a93a08794291df1fcdce6918
- Contains: Ready-to-use draw.io template
- Use: Import into draw.io and customize for your team's workflow

### Other Diagramming Options

**Gliffy** (Confluence integration)
- URL: https://www.gliffy.com
- Best for: Teams using Confluence for documentation

**Visual Paradigm Online**
- URL: https://online.visual-paradigm.com
- Contains: Git flowchart templates
- Best for: Professional-looking diagrams

---

## Microsoft Fabric Community Resources

**Fabric Community Blog - Git and Workspace Strategies**
- URL: https://community.fabric.microsoft.com/t5/Fabric-platform-Community-Blog/Git-and-workspace-strategies-for-your-Microsoft-Fabric/ba-p/4848341
- Contains: Real-world diagrams, strategy recommendations
- Best for: Practical implementation guidance

**Fabric Catalyst - DevOps Guide**
- URL: https://microsoft.github.io/fabriccatalyst/docs/DevOps_Fabric_Environment_Setup/
- Contains: Step-by-step setup guides with screenshots
- Best for: Admins setting up the environment

**Kevin Chant's Fabric Deployment Pipelines Guide**
- URL: https://www.kevinrchant.com/2024/11/06/fabricators-guide-to-microsoft-fabric-deployment-pipelines/
- Contains: Practical insights, screenshots, exam-relevant content
- Best for: Detailed understanding of deployment pipelines

---

## Recommended Diagrams to Create/Obtain

Based on the training plan, you should have these visuals available:

### Phase 1 Visuals
1. ☐ **Workspace-to-Repo Connection Diagram**
   - Source: Microsoft Learn Git Integration docs
   - Shows: How workspace items map to Git repo folders

2. ☐ **Commit Workflow Diagram**
   - Source: Create in Mermaid (see included diagrams)
   - Shows: Work → Save → Commit → Push flow

3. ☐ **Snapshot vs. Delta Concept**
   - Source: Create custom or find on Atlassian
   - Shows: Each commit as complete snapshot, not just changes

4. ☐ **Source Control Panel Screenshot**
   - Source: Capture from your Fabric environment
   - Shows: Where to find Source Control, status indicators

### Phase 2 Visuals
5. ☐ **Three-Stage Pipeline Diagram**
   - Source: Microsoft Learn Deployment Pipelines docs
   - Shows: Dev → Test → Prod stages with workspaces

6. ☐ **Deployment Rules/Parameters Visual**
   - Source: Microsoft Learn or custom
   - Shows: How same model connects to different data sources per stage

7. ☐ **Paired Items Concept**
   - Source: Microsoft Learn Deployment Pipelines docs
   - Shows: How items in different stages are connected

### Phase 3 Visuals
8. ☐ **Feature Branch Workflow Diagram**
   - Source: Your existing diagram (excellent!) + Mermaid gitGraph
   - Shows: Branch from Main → Work → PR → Merge back

9. ☐ **Pull Request Lifecycle**
   - Source: Create in Mermaid (see included diagrams)
   - Shows: Create PR → Review → Feedback → Approve → Merge

10. ☐ **Conflict Resolution Flow**
    - Source: Create custom
    - Shows: When conflicts happen, decision tree for resolution

---

## Tips for Using Visuals in Training

### Do:
- ✅ Use consistent colors across all diagrams (establish a color key)
- ✅ Animate diagrams during live training (reveal steps progressively)
- ✅ Provide printable versions for reference
- ✅ Update diagrams to match YOUR actual workflow (branch names, workspace names)

### Don't:
- ❌ Overwhelm with complex diagrams on day 1
- ❌ Use generic Git diagrams without relating to Fabric context
- ❌ Show advanced branching strategies (Gitflow) when you're using simple feature branches

### Color Key Recommendation

Use consistent colors across all your diagrams:

| Element | Suggested Color | Hex Code |
|---------|-----------------|----------|
| Main Branch | Green | #228B22 |
| Feature Branch | Blue | #4169E1 |
| Development Workspace | Light Blue | #87CEEB |
| Test Workspace | Light Purple | #DDA0DD |
| Production Workspace | Light Green | #90EE90 |
| Changed/New Items | Bright Green | #90EE90 |
| Warning/Caution | Yellow/Gold | #FFD700 |

---

## Creating Training Slides

### PowerPoint/Google Slides Approach

1. **Start with your original diagram** (the one you uploaded)
   - This perfectly matches your three phases
   - Use it as the "North Star" visual

2. **Zoom into each phase**
   - Phase 1: Just the Main branch + Dev workspace portion
   - Phase 2: Add the Deployment Pipeline (Dev → Test → Prod)
   - Phase 3: Add Feature branches and workspaces

3. **Supplement with Microsoft screenshots**
   - Capture actual Fabric UI screens
   - Annotate with arrows and callouts

4. **Include Mermaid diagrams for processes**
   - Export from mermaid.live as PNG/SVG
   - Use for: commit workflow, PR lifecycle, conflict resolution

### Recommended Slide Structure per Module

```
Slide 1: Module title + learning objectives
Slide 2: Concept diagram (big picture)
Slide 3-5: Step-by-step with screenshots
Slide 6: Quick reference summary
Slide 7: Hands-on exercise instructions
```

---

## Quick Links Cheat Sheet

Copy this section into your training materials:

### Microsoft Fabric Docs
- Git Integration: https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration
- Deployment Pipelines: https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/intro-to-deployment-pipelines
- CI/CD Workflows: https://learn.microsoft.com/en-us/fabric/cicd/manage-deployment

### Learning Git
- Interactive Tutorial: https://learngitbranching.js.org/
- Atlassian Tutorials: https://www.atlassian.com/git/tutorials

### Diagramming
- Mermaid Live: https://mermaid.live
- draw.io: https://app.diagrams.net

---

*Last Updated: January 2025*
