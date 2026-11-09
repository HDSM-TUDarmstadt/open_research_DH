# Open Research in the Digital Humanities (Jupyter Book version)

**Read the course as a website: <https://hdsm-tudarmstadt.github.io/open_research_DH/>**

A **self-paced course** on making Digital Humanities research transparent, responsible, reproducible, and
reusable, taught through hands-on work with open **cultural-heritage data** and **Jupyter Notebooks**.
No coding experience is needed.

Created by the **Humanities Data Science and Methodology (HDSM)** group and **DisLab** at the Technical
University of Darmstadt, with support from the **HERMES** project. Course lead: **Dr Nadezhda Povroznik**.

In this version **every module is one notebook**: the videos, the task, the tutorial text, the code, the
checklist, and the reading are all on one page. The same notebooks are the website, are shown on GitHub, and
run in Jupyter Notebook or Google Colab.

## Start here

Open the website above, or [`welcome.ipynb`](welcome.ipynb), then
[Module 0 · Course introduction](00-introduction/00_first_notebook.ipynb).

## The modules

| # | Module | Notebook (the whole module) |
|---|---|---|
| 0 | Course introduction | [`00-introduction/00_first_notebook.ipynb`](00-introduction/00_first_notebook.ipynb) |
| 1 | Open Humanities: principles, values, and limits | [`01-open-humanities/01_whose_data_is_open.ipynb`](01-open-humanities/01_whose_data_is_open.ipynb) |
| 2 | Documenting as a systemic practice: the research workflow | [`02-documentation-systemic-practice/02_project_setup.ipynb`](02-documentation-systemic-practice/02_project_setup.ipynb) |
| 3 | Resources for research: finding and evaluating open data | [`03-open-data/03_build_dataset.ipynb`](03-open-data/03_build_dataset.ipynb) |
| 4 | Documenting AI in the research workflow | [`04-documenting-ai/04_filter_with_ai.ipynb`](04-documenting-ai/04_filter_with_ai.ipynb) |
| 5 | Data analysis and documentation: from preparation to interpretation | [`05-data-analysis/05_data_analysis.ipynb`](05-data-analysis/05_data_analysis.ipynb) |
| 6 | Data enhancement: authority data, linked data, and provenance (optional) | [`06-data-enhancement/06_wikidata_enhancement.ipynb`](06-data-enhancement/06_wikidata_enhancement.ipynb) |
| 7 | Reproducible research: audit, repair, and reassessment | [`07-reproducible-research/07_reproducibility_check.ipynb`](07-reproducible-research/07_reproducibility_check.ipynb) |
| 8 | Open publishing and FAIR/CARE: preparing a responsible release | [`08-open-publishing/08_prepare_publication.ipynb`](08-open-publishing/08_prepare_publication.ipynb) |
|  | Course wrap-up | [`09-wrap-up/09_wrap_up.ipynb`](09-wrap-up/09_wrap_up.ipynb) |

## What is in this repository

```
welcome.ipynb                      the start page of the website
00-introduction/ ... 09-wrap-up/   one folder per module: the module notebook, slides, templates
datasets/                          the course dataset (Van Gogh records from Europeana)
_config.yml, _toc.yml              website settings and the order of the pages
_static/                           the website's logo and colours
.github/workflows/                 the instructions GitHub follows to publish the website
requirements.txt                   the Python libraries the notebooks use
requirements-website.txt           what GitHub installs to build the website
```

## For maintainers: how the website is published

You never build the website by hand. **Every time you push to the `main` branch, GitHub builds the
website and publishes it** at <https://hdsm-tudarmstadt.github.io/open_research_DH/> (it takes about 2 to 4 minutes).

**Once, when you create the repository:**

1. On GitHub, open the repository and click **Settings** (top right, the gear icon).
2. In the left menu, click **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**. Nothing else to fill in.
4. Push (or, if the files are already there, open the **Actions** tab, click **Publish the course
 website**, then **Run workflow**).

**To see whether it worked:** open the **Actions** tab. A green tick means the website is live; a red cross
means something went wrong: click it, then click **build** to see the message.

**To preview the website on your own computer** (optional):

```bash
pip install -r requirements-website.txt
jupyter-book build .
# then open _build/html/index.html in a browser
```

**Moving the repository** (for example to the HDSM organisation): open the course folder in a code editor
such as VS Code, use *Edit > Replace in Files*, and replace `HDSM-TUDarmstadt/open_research_DH` with the new
`owner/name`, then `hdsm-tudarmstadt.github.io/open_research_DH` with `owner.github.io/name`. Commit, push, and
switch on Pages in the new repository as above.

**Adding a tutorial video later.** Modules without a tutorial video have a hidden slot in Step 3 (it does not
show on the website, in Jupyter, or on GitHub). To add one, for example the GitHub tutorial in Module 2 or the
Zenodo tutorial in Module 8, open the module notebook, find the Step 3 cell, search for
`TUTORIAL VIDEO PLACEHOLDER`, and replace that hidden comment with one line:

```markdown
### Video: [Documenting by Doing Research: GitHub and Version Control](https://clip.place/w/...)
```

## Licence and credits

- Course texts: **CC BY 4.0** (see [LICENSE-CONTENT.md](LICENSE-CONTENT.md)). Code in the notebooks:
 **MIT** (see [LICENSE](LICENSE)).
- Slides and talks by guest speakers remain the work of their authors.
- Cultural-heritage records remain subject to their source institutions' terms; the Europeana metadata is CC0.

Reuse is welcome: adapt the materials for your own teaching, and cite the course (see
[CITATION.cff](CITATION.cff)).
