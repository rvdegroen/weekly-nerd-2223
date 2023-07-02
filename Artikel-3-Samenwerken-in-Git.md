# Samenwerken in Git

Chanel Mepschen heeft het in haar presentatie gehad over de samenwerking van Triple en dat zij hiervoor Git gebruiken. Ik vond dit een belangrijk onderwerp, omdat ik binnenkort tijdens mijn stage verwacht dat ik ook veel met Git (version control) moet gaan samenwerken en voor de meesterproef vond ik het ook even belangrijk om opnieuw te weten hoe het samenwerken in Git werkt. Vaak werk ik namelijk alleen, maar ik verwacht dat ik in de toekomst juist veel moet samenwerken met dit systeem, vandaar dat ik me hierin wilde verdiepen. De rest zal ik in het engels schrijven, omdat de meeste bronnen in het engels zijn geschreven.

# What is version control?

Version control is a system in which you can go back to previous versions of your project (source: https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control). There are localized version control systems, centralized version control systems and distributed version control systems.

## Local version control

Local version control systems typically are on your computer. If your computer crashes, you'll probably not be able to retrieve back your work.

## Centralized version control

Centralized version control systems saves your data in a server which you can then get on your local computer. If the server goes down however, you cannot have access to your files.

## Distributed version control

Distributed version control systems are typically the most secure one, because it saves data on several places and not on one place at the time, like localized version control systems or centralized version control systems. It basically mirrors the entire repo and it's history, so you're always able to work on your project online or offline. This is also something that Git does.

# What is Git?

Git is a free open-resource version control software that programmers can use. It enables you to commit and push changes to your projects and lets you go back to previous versions of your project if needed. It is also used as a tool for collaboration. Git thinks differently about data than other version control software, because it "stores data as snapshots of the project over time" as git.scm.com explains (source: https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F), rather than "storing data as changes to a base version of each file", which is also known as `delta-based` version control.

# How do I use Git?

I basically use Git to open the folder I'm working in and then open the entire code in VsCode with `code .`. I find this easy and a good method, because I have windows and one time I messed up really badly:

I basically started coding and then decided I wanted my files in a windows folder. I dragged the folder out of my linux system, into my windows system and continued coding. When I wanted to retrieve my files back, I didn't know how to access them from the terminal (I couldn't because they weren't in my linux anymore). I manually dragged them from my windows into my Linux and something had gone terribly wrong. I don't remember in which part of the entire process it went wrong, but my entire code broke. I couldn't save it anymore and my hard work was thrown away. Never again.

# How do I use version control?

I don't know if I'll really be using Git to it's full potential, but I will say that I do see it being useful in big projects. I have learned these past few weeks about `git checkout`, the `head` and `master`, so I do know how to use it. The real question is, will I? Because alot of the times I get so confused by my own work that I rather start from scratch, however do I realize that you can't always start from scratch. For this reason I would like to use branches, just so it won't always interfere with "main" project.

## Branches

I currently made a dev branch in which I can mess around with all I want. I might get rid of it in the future, but it's just for myself so that all of my work is in one place. I'm using it by using the `git checkout dev` command.

# How to write commits?

Let’s start with why is it important to know how to write a commit? Well, if you type in your terminal `git log` you can see your commit messages. Now imagine seeing a vague commit message like: `added something`, `fixed code`, `added change`. Is it clear for you what is being said in the commit? If you want to go back to a certain commit, would you know what you can expect from the code if you see any of the above commits? Probably not. That’s why it’s important to write good commits.

## How to write a commit in 5 steps?

1. Start with the first word capitalized put a `.` at the end
2. Use an imperative mood in the commit message - what action
3. State the type of commit - is it a bugfix, update, refactor, bump, etc?
4. For the first line max 50 characters & for the body max 72
5. Go straight to the point and ask yourself: what, why, where?

## Anatomy of a commit

- `git commit -m “<message>”` = a basic commit
- `git commit -m “<title>” -m “<description>`” = a detailed commit

## Which words could you use for your commit?

- `feat` – a new feature is introduced with the changes
- `fix` – a bug fix has occurred
- `chore` – changes that do not relate to a fix or feature and don't modify src or test files (for example updating dependencies)
- `refactor` – refactored code that neither fixes a bug nor adds a feature
- `docs` – updates to documentation such as a the README or other markdown files
- `style` – changes that do not affect the meaning of the code, likely related to code formatting such as white-space, missing semi-colons, and so on.
- `test` – including new or correcting previous tests
- `perf` – performance improvements
- `ci` – continuous integration related
- `build` – changes that affect the build system or external dependencies
- `revert` – reverts a previous commit

## Examples of Good Commits

- `feat: improve performance with lazy load implementation for images`
- `chore: update npm dependency to latest version`
- `Fix bug preventing users from submitting the subscribe form`
- `Update incorrect client phone number within footer body per client request`

## Examples of Bad Commits

- `fixed bug on landing page`
- `Changed style`
- `oops`
- `I think I fixed it this time?`

# About Open Source Projects

Open source projects are projects that people can use. How people can use your work, depends on the license you have chosen for your project.

# Bronnen

- https://www.freecodecamp.org/news/git-and-github-for-beginners/
- https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control
