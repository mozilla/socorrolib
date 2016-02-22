socorrolib
-----------

![Build Status](https://travis-ci.org/lonnen/socorrolib.svg)

The common library of the socorro crash reporter system.

Factoring out the common library is the first step to breaking up the mozilla/socorro monorepo, which contains multiple services as a historic quirk of Mozilla's development and deployment process.

Currently socorrolib is pinned to socorro revision: 8e9b1ca1c33f385d7c12fc844c7aa60075b33da4

Eventually this relationship will invert and socorro should use standard import tools to pin a version of socorrolib.

## running tests

```
pip install -r requirements

# all them tests
nosetests socorrolib

# with coverage
nosetests socorrolib --with-coverage --cover-html --cover-package=socorrolib

# to run a specific test
nostests socorrolib.unittest.external.test_crashstorage_base:TestCase.TestBase
```

## making a release

todo: travis automation to make a release
