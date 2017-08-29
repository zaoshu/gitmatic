# Gitmatic 

A pragmatic git engineering toolset built upon the [git methodology](https://paincompiler.github.io/GiThodology/).

## Install  

Run:

```bash
./install
```

It will do: 

1. copy the `templates` folder which including git message\GitHub pull request and issue templates to your local/etc
2. copy toolsets related scripts to your local/bin
3. install [gitflow](https://github.com/nvie/gitflow). (optional)

## Usage


Go to your local repository then run:

```bash
gitmatic init
```

then it will guide you to:

1. Set your working email for local repository
2. Set the git message template (auto)
3. Set GitHub pull request/issue template (working on...)
4. Install git extensions for git-flow (optional)
5. Initialize git workflow settings of current repository via git-flow (optional)

## Roadmap

- [x] commit message template [eng/zh]
- [x] init function 
- [ ] GitHub pull request/issue template
- [ ] commit message template switch function 

