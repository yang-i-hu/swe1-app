# Tools and frameworks used for development

## Django
- Tutorial: https://docs.djangoproject.com/en/5.0/intro/tutorial01/

## AWS Elastic Beanstalk Deployment 
- Tutorial: https://testdriven.io/blog/django-elastic-beanstalk/

## Code format and style
### black:
format the codes
- https://github.com/psf/black
- Note that black can be used with “--check” to validate a source tree without reformatting it

### flack8
check code styles
https://flake8.pycqa.org/en/latest/

- By default flake8 might conflict with black. Consider adding a rule to a .flake8 file to set the maximum line length accepted by flake to 88 to match black
- For other more specific disagreements between black and flake8 you can line-by-line input comments that enables flake8 to ignore a particular warning. These look like “# noqa: ”

```
#.flake8
[flake8]
max-line-length = 88
```

### display badges
#### Travis CI Build Status Badge
- Go to travis-ci.com and click on the build status badge next to the repository name
####  Coveralls Code Coverage Badge



## CI/CD
### Travis CI
- Configure Travis CI to automatically run your build on push/pull requests to github
https://docs.travis-ci.com/user/tutorials/tutorials-overview/
- Deploy the app to AWS EB upon successful completion of the tests following this guide:  https://docs.travis-ci.com/user/deployment/elasticbeanstalk/

## Test suite code coverage
### coverage
- https://coverage.readthedocs.io/

### coveralls
- https://coveralls.io/
- https://pypi.org/project/coveralls/
- Add COVERALLS REPO TOKEN to Travis CI enviornment variables.
- Use coverage.py to run your test suite and use coveralls to report the code coverage of those tests