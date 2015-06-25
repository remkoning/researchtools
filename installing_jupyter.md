# Installing Jupyter

For data munging JSON, text, and HTML python --- and especially iPython notebooks -- is fantastic. They allow you to quickly iterate on your code, see results inline, and push you to document as you write.  However, `R`'s package ecosystem and focus on statistics and econometrics means we can't only live in python when doing data analysis.  While RMarkdown is one option you can now use ipython notebooks with `R` as the underlying kernal!  Or Julia if you want!  While the naming is murky now, the new project is known as jupytr (**Ju**lia **Pyt**hon **R**), https://jupyter.org/.

Installing jupytr on a mac can be a pain but the web has come the rescue, check out the blog post here: http://www.michaelpacer.com/maths/r-kernel-for-ipython-notebook

However, these instructions may fail if you have already installed iPython (they did for me, I to an error about egg-links and more).  To avoid upgrade problems use virtualenv to create a fresh evnironment to install iptyhon in (I did `virtualenv jupyter_env`).  After creating a new environment, use source `source jupyter_env/bin/activate` to activate the environment then install ipython notebooks using `pip install ipython[notebook]`.  The first time you launch ipython notebook it may call the global python installation.  To fix this type `hash -r` into terminal to clear out your termninal's cache.  Then the notebook should work with `R` after you follow the instructions in the blog post above.

Now when you want to run the jupytr notebooks just `source jupyter_env/bin/activate; ipython notebook` and you should be up and running.
