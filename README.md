# SE8-Group5-MobileApp

Version 0.4.0

Summary
- Horoscope screens added
- Tic Tac Toe game added
- Device info screens added
- Rock Paper Scissors game added

## Dependencies to install
Please install these dependencies in your expo react-native app first.

```
npm install @react-navigation/bottom-tabs
npm install @react-navigation/drawer

npx expo install @react-navigation/native
npx expo install @react-navigation/stack
npx expo install react-native-gesture-handler

npm install react-native-reanimated
npm install react-native-screens
npm install react-native-safe-area-context

npx expo install expo-battery
npx expo install expo-device
```

## Horoscope API

Horoscope API is obtained from [https://horoscope-app-api.vercel.app/](https://horoscope-app-api.vercel.app/). No API key required.


## @expo/vector-icons And react-native-vector-icons directory

Check out link below, it shows what icons are available in each icon library and how they look.
- Expo React Native app comes pre-installed with `@expo/vector-icons` dependency, which is just a wrapper around `react-native-vector-icons`, meaning contains all the icons that `react-native-vector-icons` has. 
- So you do not need to manually do a `npm install react-native-vector-icons` unless you want to do advanced customization things via the `react-native-vector-icons` dependency.

Link: https://oblador.github.io/react-native-vector-icons/

## Guide for Git Team collaboration

Youtube guide: https://www.youtube.com/watch?v=S7XpTAnSDL4
- skip to branching part


### Step-by-step walkthrough

1. Fork your own copy of the group Repo
2. Clone the forked repository `git clone https://github.com/username/repo.git`

Change to the repository directory, `cd repo`


3. Create a new branch:
`git checkout -b feature-branch` (this is a shortcut. the branch name is feature-branch here)

  Check you are on the new Branch using `git branch`.

  **General rule of thumb:** Always use `git status` or `git branch` to check you're on the new branch

4. Do your staging and commit
  - `git add -A` (to stage all new files, deleted files, and modified files. Better than git add . as that does not stage deleted files)
  - `git commit -m "your message"`


5. Publish local branch to remote and set up tracking relationship (have to do this the first time you git push on new branch):
eg. `git push --set-upstream origin features/add_MapMain` 
(above is a chained git command of `git push` and `git --set-upstream`, meaning git push is also done in this line of code)

  - Subsequently, any further git push you want to make, simply use `git push`
    - Optional:  `git push origin your-branch-name` also works.  (see below for explanation of difference)


What is upstream branch?
An upstream branch is a remote branch that your local branch tracks. upstream command pushes a local branch to the origin remote repo (eg. your forked repo), linking them, and sets local branch to track remote branch (eg. your forked repo).


6. Create a pull request on GitHub
  - Go to your forked repository on GitHub 
  - Click on "Compare & pull request"
  - Select "main" as the base branch and "feature-branch" as the compare branch
  - Click on "Create pull request"
  - Team reviews, comments, and approves
  - Once approved, you merge the pull request 


### What is difference between" git push and  git push origin your-branch-name"?

`git push` :
- If a tracking relationship has already been set up (as it is with `--set-upstream`), git push automatically pushes the current branch (eg. Joshua-Branch, the name of my branch) to its corresponding remote branch (origin/Joshua-Branch).
- This is convenient and commonly used after setting the upstream branch.

`git push origin Joshua-Branch` :
- Explicitly specifies both the remote (`origin`) and the branch (`Joshua-Branch`) to push.
- This is useful when:
- You want to push to a different branch or remote.
- No tracking relationship has been set up. 
