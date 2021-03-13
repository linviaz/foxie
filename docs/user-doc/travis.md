  # Continuous Integration with Gitlab Travis-CI

Travis will run every time you `git push` code to github. It can be used to:

- Check your code quality automatically (autopep8).
- Automate the build, test and packaging for Python projects.
- Distribute .tar.gz and binary (single executables) from github.
- Document your code as part of github sites.


## Reference:

> The steps are better defined in "Setup Travis CI" below, this is only for reference:

- https://docs.travis-ci.com/user/getting-started/ (After step 2 - use python link below)
- https://docs.travis-ci.com/user/languages/python/


## Setup Travis CI (Basic Setup)

1. Create a new module called 'mypackage' and push it to github:
```
cookiecutter cookiecutter-template/
cd mypackage
git init
git add .
git commit -m 'Initial commit'
```

2. Create a github repository called mypackage and push to it:
```
git remote add origin git@github.com:YOURUSER/mypackage.git
git push -u origin master
```

3. In your github repository, go to *Settings > Integrations & services* and click *Add Service*. 
Select *Travis CI* from the Available Services and confirm your Github password. Click *Add Service*

4. Go to https://travis-ci.org/ and log in with your Github account. 
Go to https://travis-ci.org/profile/YOURUSER and flick the repository you want to setup for CI on.

5. Add a `.travis.yaml` file and do a git push:

```yaml
language: python

python:
    - "3.6"

install:
    - pip install .
    - pip install -r requirements.txt

script:
    - pytest

```

Check https://travis-ci.org/MYUSER/mypackage for results.


## Next session (Advanced Setup):

### Document your code and push it to github sites with `mkdocs`

### Code Coverage with pytest-cov and coveralls

### Adding build badges to README.md

### Build binaries with `pyinstaller` and release them automatically to github

### Create the final TEMPLATE and Travis documentation