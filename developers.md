
## To add support for a new VCS

So, you want to extend Versioneer to support your favorite version control system? Great! Here's what to do:

* 1: `mkdir src/NEW-VCS/`
* 2: create work-alikes for everything in `src/git/`
* 3: add NEW-VCS to the loop in setup.py `generate_versioneer()`
* 4: add clauses for NEW-VCS to `src/get_versions.py`, for both the from-keywords and from-vcs sections
* 5: add `test/test_NEWVCS.py`, copying the general style of `test_git.py` but using NEWVCS instead of git.
* 6: add a line to .travis.yml to execute your `test_NEWVCS.py` upon checkins

Then file a pull request!
