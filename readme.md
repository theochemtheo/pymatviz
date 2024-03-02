<h1 align="center">
<img src="https://github.com/janosh/pymatviz/raw/main/site/static/favicon.svg" alt="Logo" height="60px">
<br class="hide-in-docs">
pymatviz
</h1>

<h4 align="center" class="toc-exclude">

A toolkit for visualizations in materials informatics.

[![Tests](https://github.com/janosh/pymatviz/actions/workflows/test.yml/badge.svg)](https://github.com/janosh/pymatviz/actions/workflows/test.yml)
[![This project supports Python 3.9+](https://img.shields.io/badge/Python-3.9+-blue.svg?logo=python&logoColor=white)](https://python.org/downloads)
[![PyPI](https://img.shields.io/pypi/v/pymatviz?logo=pypi&logoColor=white)](https://pypi.org/project/pymatviz)
[![PyPI Downloads](https://img.shields.io/pypi/dm/pymatviz?logo=icloud&logoColor=white)](https://pypistats.org/packages/pymatviz)
[![Zenodo](https://img.shields.io/badge/DOI-10.5281/zenodo.10456384-blue?logo=Zenodo&logoColor=white)](https://zenodo.org/records/10456384)

</h4>

<slot name="how-to-cite">

> If you use `pymatviz` in your research, [see how to cite](#how-to-cite-pymatviz).

</slot>

## Installation

```sh
pip install pymatviz
```

## API Docs

See the [/api] page.

[/api]: https://janosh.github.io/pymatviz/api

## Usage

See the Jupyter notebooks under [`examples/`](examples) for how to use `pymatviz`. PRs with additional examples are welcome! 🙏

|                                                                                                                        |                                                                                                                                       |                                      |
| ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| [matbench_dielectric_eda.ipynb](https://github.com/janosh/pymatviz/blob/main/examples/matbench_dielectric_eda.ipynb)   | [![Open in Google Colab]](https://colab.research.google.com/github/janosh/pymatviz/blob/main/examples/matbench_dielectric_eda.ipynb)  | [![Launch Codespace]][codespace url] |
| [mp_bimodal_e_form.ipynb](https://github.com/janosh/pymatviz/blob/main/examples/mp_bimodal_e_form.ipynb)               | [![Open in Google Colab]](https://colab.research.google.com/github/janosh/pymatviz/blob/main/examples/mp_bimodal_e_form.ipynb)        | [![Launch Codespace]][codespace url] |
| [matbench_perovskites_eda.ipynb](https://github.com/janosh/pymatviz/blob/main/examples/matbench_perovskites_eda.ipynb) | [![Open in Google Colab]](https://colab.research.google.com/github/janosh/pymatviz/blob/main/examples/matbench_perovskites_eda.ipynb) | [![Launch Codespace]][codespace url] |
| [mprester_ptable.ipynb](https://github.com/janosh/pymatviz/blob/main/examples/mprester_ptable.ipynb)                   | [![Open in Google Colab]](https://colab.research.google.com/github/janosh/pymatviz/blob/main/examples/mprester_ptable.ipynb)          | [![Launch Codespace]][codespace url] |

[Open in Google Colab]: https://colab.research.google.com/assets/colab-badge.svg
[Launch Codespace]: https://img.shields.io/badge/Launch-Codespace-darkblue?logo=github
[codespace url]: https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=340898532

## Periodic Table

See [`pymatviz/ptable.py`](pymatviz/ptable.py). Heatmaps of the periodic table can be plotted both with `matplotlib` and `plotly`. `plotly` supports displaying additional data on hover or full interactivity through [Dash](https://plotly.com/dash).

| [`ptable_heatmap(compositions, log=True)`](pymatviz/ptable.py) |    [`ptable_heatmap_ratio(comps_a, comps_b)`](pymatviz/ptable.py)     |
| :------------------------------------------------------------: | :-------------------------------------------------------------------: |
|                       ![ptable-heatmap]                        |                        ![ptable-heatmap-ratio]                        |
|  [`ptable_heatmap_plotly(atomic_masses)`](pymatviz/ptable.py)  | [`ptable_heatmap_plotly(compositions, log=True)`](pymatviz/ptable.py) |
|            ![ptable-heatmap-plotly-more-hover-data]            |                     ![ptable-heatmap-plotly-log]                      |
| [`ptable_hists(data, colormap="coolwarm"`](pymatviz/ptable.py) |   [`ptable_scatters(data, colormap="coolwarm"`](pymatviz/ptable.py)   |
|                        ![ptable-hists]                         |                          ![ptable-scatters]                           |

[ptable-hists]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-hists.svg
[ptable-scatters]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-scatters.svg

## Phonons

See [`pymatviz/phonons.py`](pymatviz/phonons.py).

|           [`plot_phonon_bands(bands_dict)`](pymatviz/phonons.py)           | [`plot_phonon_dos(doses_dict)`](pymatviz/phonons.py) |
| :------------------------------------------------------------------------: | :--------------------------------------------------: |
|                              ![phonon-bands]                               |                    ![phonon-dos]                     |
| [`plot_phonon_bands_and_dos(bands_dict, doses_dict)`](pymatviz/phonons.py) |                                                      |
|                          ![phonon-bands-and-dos]                           |                                                      |

[phonon-bands]: https://github.com/janosh/pymatviz/raw/main/assets/phonon-bands-mp-2758.svg
[phonon-dos]: https://github.com/janosh/pymatviz/raw/main/assets/phonon-dos-mp-2758.svg
[phonon-bands-and-dos]: https://github.com/janosh/pymatviz/raw/main/assets/phonon-bands-and-dos-mp-2758.svg

### Dash app using `ptable_heatmap_plotly()`

See [`examples/mprester_ptable.ipynb`](https://github.com/janosh/pymatviz/blob/main/examples/mprester_ptable.ipynb).

<https://user-images.githubusercontent.com/30958850/181644052-b330f0a2-70fc-451c-8230-20d45d3af72f.mp4>

## Sunburst

See [`pymatviz/sunburst.py`](pymatviz/sunburst.py).

| [`spacegroup_sunburst([65, 134, 225, ...])`](pymatviz/sunburst.py) | [`spacegroup_sunburst(["C2/m", "P-43m", "Fm-3m", ...])`](pymatviz/sunburst.py) |
| :----------------------------------------------------------------: | :----------------------------------------------------------------------------: |
|                        ![spg-num-sunburst]                         |                             ![spg-symbol-sunburst]                             |

## Sankey

See [`pymatviz/sankey.py`](pymatviz/sankey.py).

| [`sankey_from_2_df_cols(df_perovskites)`](pymatviz/sankey.py) | [`sankey_from_2_df_cols(df_rand_ints)`](pymatviz/sankey.py) |
| :-----------------------------------------------------------: | :---------------------------------------------------------: |
|             ![sankey-spglib-vs-aflow-spacegroups]             |              ![sankey-from-2-df-cols-randints]              |

## Structure

See [`pymatviz/structure_viz.py`](pymatviz/structure_viz.py). Currently structure plotting is only supported with `matplotlib` in 2d. 3d interactive plots (probably with `plotly`) are on the road map.

| [`plot_structure_2d(mp_19017)`](pymatviz/structure_viz.py) | [`plot_structure_2d(mp_12712)`](pymatviz/structure_viz.py) |
| :--------------------------------------------------------: | :--------------------------------------------------------: |
|  ![struct-2d-mp-19017-Li4Mn0.8Fe1.6P4C1.6O16-disordered]   |        ![struct-2d-mp-12712-Hf9Zr9Pd24-disordered]         |

![matbench-phonons-structures-2d]

## Histograms

See [`pymatviz/histograms.py`](pymatviz/histograms.py).

| [`spacegroup_hist([65, 134, 225, ...], backend="matplotlib")`](pymatviz/histograms.py) | [`spacegroup_hist(["C2/m", "P-43m", "Fm-3m", ...], backend="matplotlib")`](pymatviz/histograms.py) |
| :------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------: |
|                               ![spg-num-hist-matplotlib]                               |                                   ![spg-symbol-hist-matplotlib]                                    |
|   [`spacegroup_hist([65, 134, 225, ...], backend="plotly")`](pymatviz/histograms.py)   |   [`spacegroup_hist(["C2/m", "P-43m", "Fm-3m", ...], backend="plotly")`](pymatviz/histograms.py)   |
|                                 ![spg-num-hist-plotly]                                 |                                     ![spg-symbol-hist-plotly]                                      |
|   [`elements_hist(compositions, log=True, bar_values='count')`](pymatviz/ptable.py)    |                                                                                                    |
|                                    ![elements-hist]                                    |                                                                                                    |

[spg-symbol-hist-plotly]: https://github.com/janosh/pymatviz/raw/main/assets/spg-symbol-hist-plotly.svg
[spg-num-hist-plotly]: https://github.com/janosh/pymatviz/raw/main/assets/spg-num-hist-plotly.svg
[spg-num-hist-matplotlib]: https://github.com/janosh/pymatviz/raw/main/assets/spg-num-hist-matplotlib.svg
[spg-symbol-hist-matplotlib]: https://github.com/janosh/pymatviz/raw/main/assets/spg-symbol-hist-matplotlib.svg

## Parity Plots

See [`pymatviz/parity.py`](pymatviz/parity.py).

|      [`density_scatter(xs, ys, ...)`](pymatviz/parity.py)       | [`density_scatter_with_hist(xs, ys, ...)`](pymatviz/parity.py)  |
| :-------------------------------------------------------------: | :-------------------------------------------------------------: |
|                       ![density-scatter]                        |                  ![density-scatter-with-hist]                   |
|       [`density_hexbin(xs, ys, ...)`](pymatviz/parity.py)       |  [`density_hexbin_with_hist(xs, ys, ...)`](pymatviz/parity.py)  |
|                        ![density-hexbin]                        |                   ![density-hexbin-with-hist]                   |
| [`scatter_with_err_bar(xs, ys, yerr, ...)`](pymatviz/parity.py) | [`residual_vs_actual(y_true, y_pred, ...)`](pymatviz/parity.py) |
|                     ![scatter-with-err-bar]                     |                      ![residual-vs-actual]                      |

## Uncertainty

See [`pymatviz/uncertainty.py`](pymatviz/uncertainty.py).

|       [`qq_gaussian(y_true, y_pred, y_std)`](pymatviz/uncertainty.py)       |       [`qq_gaussian(y_true, y_pred, y_std: dict)`](pymatviz/uncertainty.py)       |
| :-------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: |
|                             ![normal-prob-plot]                             |                           ![normal-prob-plot-multiple]                            |
| [`error_decay_with_uncert(y_true, y_pred, y_std)`](pymatviz/uncertainty.py) | [`error_decay_with_uncert(y_true, y_pred, y_std: dict)`](pymatviz/uncertainty.py) |
|                         ![error-decay-with-uncert]                          |                        ![error-decay-with-uncert-multiple]                        |

## Cumulative Metrics

See [`pymatviz/cumulative.py`](pymatviz/cumulative.py).

| [`cumulative_error(preds, targets)`](pymatviz/cumulative.py) | [`cumulative_residual(preds, targets)`](pymatviz/cumulative.py) |
| :----------------------------------------------------------: | :-------------------------------------------------------------: |
|                     ![cumulative-error]                      |                     ![cumulative-residual]                      |

## Classification

See [`pymatviz/relevance.py`](pymatviz/relevance.py).

| [`roc_curve(targets, proba_pos)`](pymatviz/relevance.py) | [`precision_recall_curve(targets, proba_pos)`](pymatviz/relevance.py) |
| :------------------------------------------------------: | :-------------------------------------------------------------------: |
|                       ![roc-curve]                       |                       ![precision-recall-curve]                       |

## Correlation

See [`pymatviz/correlation.py`](pymatviz/correlation.py).

| [`marchenko_pastur(corr_mat, gamma=ncols/nrows)`](pymatviz/correlation.py) | [`marchenko_pastur(corr_mat_significant_eval, gamma=ncols/nrows)`](pymatviz/correlation.py) |
| :------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------: |
|                            ![marchenko-pastur]                             |                            ![marchenko-pastur-significant-eval]                             |

[cumulative-error]: https://github.com/janosh/pymatviz/raw/main/assets/cumulative-error.svg
[cumulative-residual]: https://github.com/janosh/pymatviz/raw/main/assets/cumulative-residual.svg
[density-hexbin-with-hist]: https://github.com/janosh/pymatviz/raw/main/assets/density-hexbin-with-hist.svg
[density-hexbin]: https://github.com/janosh/pymatviz/raw/main/assets/density-hexbin.svg
[density-scatter-with-hist]: https://github.com/janosh/pymatviz/raw/main/assets/density-scatter-with-hist.svg
[density-scatter]: https://github.com/janosh/pymatviz/raw/main/assets/density-scatter.svg
[error-decay-with-uncert-multiple]: https://github.com/janosh/pymatviz/raw/main/assets/error-decay-with-uncert-multiple.svg
[error-decay-with-uncert]: https://github.com/janosh/pymatviz/raw/main/assets/error-decay-with-uncert.svg
[elements-hist]: https://github.com/janosh/pymatviz/raw/main/assets/elements-hist.svg
[marchenko-pastur-significant-eval]: https://github.com/janosh/pymatviz/raw/main/assets/marchenko-pastur-significant-eval.svg
[marchenko-pastur]: https://github.com/janosh/pymatviz/raw/main/assets/marchenko-pastur.svg
[matbench-phonons-structures-2d]: https://github.com/janosh/pymatviz/raw/main/assets/matbench-phonons-structures-2d.svg
[normal-prob-plot-multiple]: https://github.com/janosh/pymatviz/raw/main/assets/normal-prob-plot-multiple.svg
[normal-prob-plot]: https://github.com/janosh/pymatviz/raw/main/assets/normal-prob-plot.svg
[precision-recall-curve]: https://github.com/janosh/pymatviz/raw/main/assets/precision-recall-curve.svg
[ptable-heatmap-plotly-log]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-heatmap-plotly-log.svg
[ptable-heatmap-plotly-more-hover-data]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-heatmap-plotly-more-hover-data.svg
[ptable-heatmap-ratio]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-heatmap-ratio.svg
[ptable-heatmap]: https://github.com/janosh/pymatviz/raw/main/assets/ptable-heatmap.svg
[residual-vs-actual]: https://github.com/janosh/pymatviz/raw/main/assets/residual-vs-actual.svg
[roc-curve]: https://github.com/janosh/pymatviz/raw/main/assets/roc-curve.svg
[sankey-from-2-df-cols-randints]: https://github.com/janosh/pymatviz/raw/main/assets/sankey-from-2-df-cols-randints.svg
[sankey-spglib-vs-aflow-spacegroups]: https://github.com/janosh/pymatviz/raw/main/assets/sankey-spglib-vs-aflow-spacegroups.svg
[scatter-with-err-bar]: https://github.com/janosh/pymatviz/raw/main/assets/scatter-with-err-bar.svg
[spg-num-sunburst]: https://github.com/janosh/pymatviz/raw/main/assets/spg-num-sunburst.svg
[spg-symbol-sunburst]: https://github.com/janosh/pymatviz/raw/main/assets/spg-symbol-sunburst.svg
[struct-2d-mp-12712-Hf9Zr9Pd24-disordered]: https://github.com/janosh/pymatviz/raw/main/assets/struct-2d-mp-12712-Hf9Zr9Pd24-disordered.svg
[struct-2d-mp-19017-Li4Mn0.8Fe1.6P4C1.6O16-disordered]: https://github.com/janosh/pymatviz/raw/main/assets/struct-2d-mp-19017-Li4Mn0.8Fe1.6P4C1.6O16-disordered.svg

## How to cite `pymatviz`

See [`citation.cff`](citation.cff) or cite the [Zenodo record](https://zenodo.org/badge/latestdoi/340898532) using the following BibTeX entry:

```bib
@software{riebesell_pymatviz_2022,
  title = {Pymatviz: visualization toolkit for materials informatics},
  author = {Riebesell, Janosh},
  date = {2022-10-01},
  year = {2022},
  doi = {10.5281/zenodo.7486816},
  url = {https://github.com/janosh/pymatviz},
  note = {10.5281/zenodo.7486816 - https://github.com/janosh/pymatviz},
  urldate = {2023-01-01}, % optional, replace with your date of access
  version = {0.7.1}, % replace with the version you use
}
```
