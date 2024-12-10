

# Latex Resume

This project uses [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension of [VSCode](https://code.visualstudio.com/) to auto-build latex files to create [resume.pdf].

## 🤔 How to run?

1. Install [VSCode](https://code.visualstudio.com/).
2. Install [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension.
3. Install [VS Code Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers).
4. Install [Docker Desktop](https://www.docker.com/products/docker-desktop).
5. Open this directory in VSCode.
6. Execute `Remote-Containers: Reopen in Container` in the VS Code Command Palette.

## ⚠️ Issues

### [✅ Fixed] Latex not auto-building on file change
**⚠️ Issue:**

[resume.pdf] was not updating when saving any file other than [resume.tex]. This made it difficult to reflect changes while editing, as I had to return to [resume.tex] and save it manually.

**✅ Fix:**

This is a known issue as mentioned in the [extensions wiki](https://github.com/James-Yu/LaTeX-Workshop/wiki/FAQ#auto-build-does-not-work-sometimes):
> Please try setting [`latex-workshop.latex.autoBuild.run`](https://github.com/James-Yu/LaTeX-Workshop/wiki/Compile#latex-workshoplatexautobuildrun) to `onSave`.
> Reload vscode to make any change in this configuration effective.

## References

Followed [Latex Workshop VSCode Extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)'s [Using Docker](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#using-docker) approach to generate pdf from latex code using docker container.

Another article describing some more options: [VS Code + Docker + LaTeX Setup](https://medium.com/@kombustor/vs-code-docker-latex-setup-f84128c6f790)

**Not Recommended Approach:**

Previously followed this article - [LaTeX + VS Code + Docker = 🚀](https://medium.com/@timju/latex-setup-with-vs-code-and-docker-612f998e1f23) and used the experimental feature of `latex-workshop.docker.image.latex`, but the extension strongly recommends not to use this method in their [wiki](https://github.com/James-Yu/latex-workshop/wiki/Install#:~:text=VS%20Code%20supports%20Docker%20with%20Remote%20%2D%20Containers.%20LaTeX%20Workshop%20works%20well%20with%20the%20extension.%20You%20can%20see%20an%20example.%20We%20strongly%20recommend%20you%20to%20use%20the%20extension%20instead%20of%20our%20following%20experimental%20feature.) and instead recommends using [this method](https://github.com/James-Yu/LaTeX-Workshop/tree/master/samples/docker).


<!-- Links -->
[resume.pdf]: ./resume.pdf
[resume.tex]: ./resume.tex
