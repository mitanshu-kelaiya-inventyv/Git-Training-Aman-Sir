# Git Training - Aman Sir

## Branches in Git
Branches are an in-built feature in the Git Versioning System. Branches allow you to develop features, fix bugs, or safely experiment with new ideas in a contained area of your repository.

## Creating Branches
```bash
git branch <branch_name>

git branch feature1 # This will create a branch named 'feature1'
```

To see all branches of the current repo:

```bash
git branch  # This will display all branches
```

### Creating Branches with `git checkout`
The other command used to create branches is `git checkout`:

```bash
# Syntax
git checkout -b <branch_name>

# Example
git checkout -b feature2 # This will create a branch named 'feature2'
```

## Branching Example
![Branching Example](<Screenshot 2025-02-03 161736.png>)

- **master**: Represents the production-ready code. All changes eventually merge into `master` after thorough testing.
- **feature**: Used for developing new features or bug fixes. Allows for isolated development without affecting the stable `master` branch.
- **release**: A temporary branch created from `master` for preparing a release. It allows for final bug fixes or documentation updates before going live.
- **dev**: The primary integration branch for ongoing development. Feature branches are merged into `dev` for testing and stabilization before going to `master`.


## Pull Request
A Pull Request (PR) is a feature in version control systems like Git that allows developers to propose changes to a repository. It enables collaboration, review, and discussion before merging the changes into the main branch.

### If a Non-Collaborator Wants to Make Changes:
They need to fork the repository first:<br>
![Fork Repository](image.png)

### After Committing Updates in the Forked Repo:
The non-collaborator needs to create a pull request:<br>
![Create Pull Request](image-1.png)

### If There Are No Conflicts:
GitHub allows us to create a pull request:<br>
![No Conflicts](image-2.png)

> **Note:** Only users with write access are allowed to merge pull requests.

### On the Repository Owner's Side:
A pull request appears:<br>
<p align="center">
  <img src="image-3.png" alt="Pull Request Notification">
</p>

### Opening the Pull Request:
![Open Pull Request](image-4.png)

### The Owner Can Merge the Pull Request After Reviewing:
![Merge Pull Request](image-5.png)

### Updated Main Branch:
![Updated Main Branch](image-6.png)

## Branching Rules
Code owners can manage when a code should actually get merged into the repository.

### Setting Up Branch Rules:
In **Settings > Branches > Add Branch Ruleset**, you can add rulesets for your branches.

#### Step 1: Give a Ruleset Name
![Ruleset Name](image-8.png)

#### Step 2: Set Target Branches
Specify the branches on which you want to apply rules:<br>
![Target Branches](image-9.png)

#### Step 3: Select Required Restrictions
![Select Restrictions](image-10.png)
![More Restrictions](image-11.png)
