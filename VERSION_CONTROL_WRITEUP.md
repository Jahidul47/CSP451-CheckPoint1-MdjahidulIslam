# Version Control Systems: Understanding Git and GitHub

## Introduction to Version Control

Version control systems (VCS) record and manage changes to a project's files over
time. They keep a complete, navigable history of every modification, so a team
always knows what changed, when it changed, and who made the change. This safety
net is essential in modern software development, where many people edit the same
codebase and every mistake must be reversible.

## How Version Control Tracks Changes

Git tracks work as a series of snapshots. Each snapshot is a **commit** that captures
the state of the project at one moment. Alongside the file contents, every commit
stores metadata: the author and committer, a timestamp, the parent commit(s), and a
descriptive message. Git then computes a unique **SHA-1 hash** (for example,
`a1b2c3d`) that identifies the commit and guarantees its integrity. Because each
commit points back to its parent, the history forms a directed acyclic graph that
Git can walk. This lets developers view a file's full history, compare any two
versions, pinpoint when a bug was introduced (`git bisect`), and understand how the
code evolved.

## Three Collaboration Benefits with Examples

### 1. Parallel Development with Branches
Branches let several people work at once without colliding. On an e-commerce team,
Developer A builds payment integration on `feature/payments`, Developer B builds
login on `feature/auth`, and each merges into `main` when ready — nobody waits on
anyone else.

### 2. Code Review and Conflict Resolution
When two people edit the same function, Git flags the conflict instead of silently
overwriting work. Pull requests add a review step: before code reaches `main`, a
teammate reads the diff, leaves comments, and approves it, which catches bugs early
and spreads knowledge across the team.

### 3. Rollback and Recovery
When a release breaks production, the team finds the bad commit and runs `git revert`
to undo it, restoring a working app in minutes. For a payments service, that
difference between a quick revert and a slow manual fix can prevent real financial
loss.

## Git's Backup and Recovery Mechanisms

Git is distributed, so every clone is a full backup of the entire history — there is
no single point of failure, and developers can work offline and sync later. Locally,
the `.git/` directory holds the object database (commits, trees, blobs, tags), the
refs that point to branches, and the repository config. Recovery tools include
`git reflog` (recover "lost" commits by replaying HEAD movements), `git reset` (move
HEAD to an earlier commit), `git revert` (create a new commit that undoes a change),
and `git fsck` (check integrity and find dangling objects). Pushing to a remote such
as GitHub adds an off-machine copy for extra redundancy.

## Difference Between Git and GitHub

Git is the version-control tool; GitHub is a hosting platform built around it.

| Aspect   | Git                      | GitHub                                  |
|----------|--------------------------|-----------------------------------------|
| Nature   | Software tool            | Web service                             |
| Runs     | Locally on your machine  | In the cloud (github.com)               |
| Offline  | Works fully offline      | Needs an internet connection            |
| Storage  | Local `.git/` directory  | Remote servers                          |
| Scope    | Version control only     | Hosting + pull requests, issues, CI/CD  |

GitHub uses Git underneath: pushing sends your local commits to GitHub's servers,
where features such as pull requests, issues, and Actions support collaboration.

## Conclusion

Git makes change tracking, parallel work, and recovery reliable, while GitHub adds a
shared home for hosting and collaboration. Together they form the backbone of modern
team software development.
