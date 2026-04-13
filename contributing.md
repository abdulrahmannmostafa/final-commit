# Contributing - Add Your Profile

Follow this exact workflow to add your info.

## 1) Fork The Repository

On GitHub, click `Fork` on the main repository.

## 2) Clone Your Fork

Clone your own fork locally:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

## 3) Create A Branch

Use a branch name that identifies your profile change:

```bash
git checkout -b add-profile-<your-name>
```

## 4) Add Your Data Files

Create your folder under `data/`:

```text
data/<your-folder>/
```

Recommended folder slug format:
- lowercase
- words separated with `-`
- example: `ahmed-elsayed-mohsen`

Create this file:

```text
data/<your-folder>/profile.json
```

Use this template:

```json
{
  "name": "Your Full Name",
  "tagline": "Short one-line intro.",
  "stack": ["Python", "C++", "React"],
  "course": "Compiler Design",
  "gp": {
    "title": "Project Name",
    "url": "https://github.com/your-user/your-repo"
  },
  "quote": "Your favorite quote.",
  "message": "A short message for future students.",
  "fun_fact": "Something fun about you.",
  "links": {
    "github": "https://github.com/your-user",
    "linkedin": "https://linkedin.com/in/your-user"
  },
  "image": "avatar.jpg"
}
```

Optional avatar:

```text
data/<your-folder>/avatar.jpg
```

If you do not provide an avatar, initials are shown automatically.

## 5) Verify Locally

Open the page  and run:
- `ls`
- `cat data/<your-folder>/profile.json`
- `grep <your name>`

## 6) Commit And Push

```bash
git add data/<your-folder>/profile.json data/<your-folder>/avatar.jpg
git commit -m "Add profile: <Your Name>"
git push origin add-profile-<your-name>
```

If you did not add an avatar, remove it from the `git add` command.

## 7) Open A Pull Request

Open a PR from your branch in your fork to the `main` branch in the upstream repository.

PR title format:
- `Add profile: Your Full Name`

PR description should include:
- your full name
- your folder slug
- confirmation that `profile.json` is valid JSON

## Important Notes

- Do not edit other contributors' folders.
- Do not edit `index.html` unless maintainers ask for it.
- Do not edit `data/index.json` manually. It is updated automatically by GitHub Actions
