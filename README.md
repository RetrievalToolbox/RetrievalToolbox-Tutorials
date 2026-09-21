# RetrievalToolbox Tutorials

Welcome to the online tutorials for the [RetrievalToolbox](https://www.github.com/US-GHG-Center/RetrievalToolbox.jl) retrieval algorithm software library. These are a series of online tutorials for interested users of the software library. A basic level of background knowledge of atmospheric gas retrievals is expected, as these tutorials mainly guide users to how the software library is meant to be utilized. Knowledge of the Julia programming language is not necessarily required, in fact some of the tutorials have small sections in them that highlight various features and peculiarities of Julia. Thus, users who have not worked with Julia before will be made aware of potential pitfalls as well as strengths of the Julia programming language.

Head over [here](https://retrievaltoolbox.github.io/RetrievalToolbox-Tutorials/) to start learning!

## Rendering the documents

The easiest way to render the documents is to create a dedicated **conda** environment that contains the **Quarto** software, like so:

    mamba env create --name RT_tut
    mamba activate RT_tut
    mamba install quarto

On some machines, you may need to install additional software, such as `librsvg`:

    mamba install librsvg


**[Quarto](https://quarto.org)** also requires the local project environment to have all necessary Julia packages installed, since the items in the cells are evaluated during the rendering of the document:

    julia --project=. -e 'using Pkg; Pkg.instantiate()'

To render the documents then type

    quarto render

By default, the document is rendered as a webpage inside the `docs` sub-folder, that can be viewed by starting a local web-server:

    python3 -m http.server 1234

and pointing an internet browser to `localhost:1234`.
