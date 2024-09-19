# GitHub Setup

GitHub is a platform for version control and collaboration that allows you to manage and store your code repositories using Git. It enables you to collaborate on projects, track changes, and review code efficiently.

## Prerequisites
1. **Install Git**:
   - Follow the instructions to [install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your system.
2. **Create a GitHub Account**:
   - Sign up for a [GitHub account](https://github.com/) if you don't already have one.

## Cloning a Repository
To work with an existing repository, you need to clone it to your local machine:
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

## Creating a New Branch
Create a new branch to work on features or fixes without affecting the main codebase:
```bash
git checkout -b your-branch-name
```

## Committing and Pushing Changes
To save and share your changes with others:
```bash
git add .
git commit -m "Brief description of changes"
git push origin your-branch-name
```

## Creating a Pull Request
To propose changes and request that they be merged into the main codebase:
1. Navigate to the repository on GitHub.
2. Click on **"Pull Requests"** > **"New Pull Request"**.
3. Select your branch and submit the pull request.

---