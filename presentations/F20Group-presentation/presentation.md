---
title: "An exploratory study on user *dotfiles* management"
author: Wenhan Zhu (Cosmos)
output: beamer_presentation
---

![Customized ZSH prompt](./customize-zsh-prompt.png)

![Default ZSH prompt](./default-zsh-prompt.png)

# Definition of *dotfiles*

> User-specific application configuration is traditionally stored in so called
> **dotfiles** (files whose filename starts with a dot).
> --- ArchLinux Wiki [^1]

[^1]: https://wiki.archlinux.org/index.php/Dotfiles

# 

![Advocate for *dotfiles* sharing. [^2]](./dotfiles-are-meant-to-be-forked.png)

[^2]: https://zachholman.com/2010/08/dotfiles-are-meant-to-be-forked/

# 

![Dotfiles community on GitHub [^3]](./dotfiles-community-github.png)

[^3]: https://dotfiles.github.io/

#

![Study on software configurations](./software-configuration-paper-1.png)


# Improving user-space software development

**Improving code completion with program history** by *Romain Robbles and Michele
Lanza* ASE 2010

![Tabnine autocompletion [^4]](./tabnine-autocompletion.png)

[^4]: https://www.tabnine.com/blog/deep/


# Exploration on user *dotfiles* management

![Visual Notes on Eric S. Raymond's "The Cathedral and the Bazaar" by Giulia Forsythe](./the-cathedral-and-the-bazaar.png)
## Change in open source software community

### Previouly people would e-mail each other when they use your software

### Now more ways to communicate with developer such as gitter/slack/discord

### The silent majority

### Distributed helping (i.e., people would ask about how to use X on Stack Overflow/reddit and not neccessary the developer of the software) 

#

![dotfiles repositories on GitHub](./dotfiles-github-search.png)

# Data collection

All GitHub repos matching extactly the name `dotfiles` with the following
criteria

- 5 stars
- 5 commits in the `dotfiles` repository
- 10 commits in other repositories

Result: **3305** total *dotfiles* repositories.

# Who hosts their *dotfiles* on GitHub?

![A gorilla *vim* user](./gorilla-vim-user.png)

#

: Owners of *dotfiles* repositories

-----------------------------------------------------------------------
Occupation                                                        Count
---------------------------------------------------------------- ------
Developers                                                          79

System Admin                                                         3

Students                                                             6

Researchers                                                          3

Unknown                                                              9

Total                                                              100
-----------------------------------------------------------------------

# What files are contained in *dotfiles* repositories

![Wordcloud of files in *dotfiles*
repositories](./common-dotfiles-word-cloud.png)

#

![*dotfiles* repository repo
sizes](./boxplot_dist_repo_raw_size.png){height=300px}

#

![*dotfiles* repositories file counts](./boxplot_dist_n_files.png){height=300px}

#

![Commits in *dotfiles* repositories](./boxplot_dist_n_commits.png){height=300px}

#

![Contributors to *dotfiles*
repositories](./boxplot_contributors_dist.png){height=300px}

# Thank you! Any suggestions
