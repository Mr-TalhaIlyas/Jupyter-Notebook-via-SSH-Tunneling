# Jupyter-Notebook-via-SSH-Tunneling

You need to install termius or putty then follwo the steps in following video.

https://www.youtube.com/watch?v=RsLDwDCIDcM


## Jupyter Themes
Install jupyter themes by

```
pip install jupyterthemes
```

There are many options available in this package and you have to choose a optimized combination yourself. So, I just made two optimized and better color (dark) combination and you can just type in these and tweek them as you like.

### Theme 1

```
jt -t onedork -fs 115 -nfs 125 -tfs 115 -dfs 115 -ofs 115 -cursc r -cellw 80% -lineh 115 -altmd  -kl -T -N
```

### Theme 2
```
jt -t monokai -f roboto -fs 115 -altp -ofs 115 -dfs 11 -tfs 135 -nfs 135 -cellw 88% -kl -T -N
```

Even these might not show you the jupyter logo, saved checkpoint time and notebook name so you navigate to `.jupyter/custom/custom.css` file and find follwoing three lines and makes changes accordingly.

```
div#ipython_notebook { display: block !important; }

body > #header #header-container { display: block !important; padding-bottom: 0px; padding-top: 4px; box-sizing: border-box; -moz-box-sizing: border-box; -webkit-box-sizing: border-box; }

span.autosave_status { display: block !important; font-size: small; }
```
Simply put you are just adding the `display: block !important;` in every line to show the above missing elements in the notebook.
One drawback is that you have to follow this step everytime  you change theme.

So you can also try the following mehtod

navigate to  `.jupyterthemes/layout/notebook.less` and

remove this
`div#ipython_notebook { display: none; }`

and change
`pan.autosave_status { font-size: small; }`

