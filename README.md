<img src="assets\imgs\fitymi_header.svg" alt="Please Let Me Merge Before I Start Crying: And Other Things I&apos;ve Said At The Git Terminal" style="max-width=&apos;100%&apos;"/>

# **Resources for Fake It Til' You Make It: Mocking Reality So Your Tests Can Run** <br>

## **About**

This repository contains supplemental resources and materials that coincide with the *"Resources for Fake It Til' You Make It: Mocking Reality So Your Tests Can Ru"* talk at [Posit::conf(2026)](https://conf.posit.co/2026/sessions/).

### Abstract
As data scientists mature in their work, many move from analysis scripts to larger codebases and packages, bringing unit testing into the workflow. For some, a handful of basic tests is enough. For others, as code grows more complex, familiar testing patterns may start to break. We’ll explore testing in isolation as a practical way to handle more challenging programming scenarios. We’ll cover the core ideas behind mocking and controlling your code’s environment while focusing on when, where, how, and why these techniques help in real projects.

*"Fake it Til' You Make It"* is intended for anyone already comfortable with unit testing who wants to explore strategies for isolating behavior, reducing test fragility, and expanding test coverage for complex systems.

<br>

This repository serves as a resource for relevant supplemental materials for those seeking to learn more about testing in isolation and mocking.

------------------------------------------------------------------------

## **Slides and Talk Recording**

The slides for *"Fake It Til' You Make It"* can be found on this repository [here](https://meghansaha.github.io/fake_it_til_you_make_it/#/title-slide).

This talk will be presented on September 16<sup>th</sup> 2026, 3:00 PM CDT in Houston, Texas United States. A recording of this talk will be available on YouTube on a later date.

------------------------------------------------------------------------

## **Supplemental Resources**

### R

**Core testing**
- [testthat](https://testthat.r-lib.org/) - the standard unit testing framework for R packages
- [R Packages (2e), Ch. 13: Testing basics](https://r-pkgs.org/testing-basics.html)
- [R Packages (2e), Ch. 14: Designing your test suite](https://r-pkgs.org/testing-design.html)
- [R Packages (2e), Ch. 15: Advanced testing techniques](https://r-pkgs.org/testing-advanced.html)

**Mocking & isolation**
- [testthat: Mocking vignette](https://testthat.r-lib.org/articles/mocking.html) - overview of testthat's native mocking approach
- [local_mocked_bindings()](https://testthat.r-lib.org/reference/local_mocked_bindings.html) - testthat's built-in function for temporarily redefining function definitions in tests
- [Maëlle Salmon - R-hub blog: Update on mocking for testing R packages (2024)](https://blog.r-hub.io/2024/03/21/mocking-new-take/) - good current-state overview of the R mocking landscape
- [httptest2: Test Helpers for ‘httr2’](https://enpiar.com/httptest2/) - An R package that makes it easier to write tests for code and packages that wrap web APIs. 
- [httptest: A Test Environment for HTTP Requests in R](https://enpiar.com/httptest2/articles/httptest2.html) - test helpers for isolating/mocking HTTP requests made with `httr2`

### Python

**Core testing**
- [pytest](https://docs.pytest.org/) - the de facto standard test runner/framework
- [unittest.mock](https://docs.python.org/3/library/unittest.mock.html) - stdlib mocking library
- [unittest.mock - getting started](https://docs.python.org/3/library/unittest.mock-examples.html) - practical `patch`/`MagicMock` examples

**Mocking & isolation**
- [pytest-mock](https://pytest-mock.readthedocs.io/) - thin pytest wrapper around `unittest.mock` (the `mocker` fixture)
- [responses](https://github.com/getsentry/responses) - mock `requests`-based HTTP calls
- [requests-mock](https://requests-mock.readthedocs.io/) - alternative HTTP mocking library for `requests`
- [vcrpy](https://github.com/kevin1024/vcrpy) - records real HTTP interactions once, replays them as fixtures ("cassettes") in tests
- [moto](https://github.com/getmoto/moto) - mocks AWS services for tests (handy for AWS-backed pipelines)

### Cross-Cutting Concepts
- [Martin Fowler: Mocks Aren't Stubs](https://martinfowler.com/articles/mocksArentStubs.html)- the canonical (A.K.A 'old') explainer on test doubles, and why "mock" gets overloaded
- [Google Testing Blog: Know Your Test Doubles](https://testing.googleblog.com/2013/07/testing-on-toilet-know-your-test-doubles.html)- short, concrete definitions of dummy/stub/spy/mock/fake
- [Software Engineering at Google, Ch. 13: Test Doubles](https://abseil.io/resources/swe-book/html/ch13.html)- deeper dive on when test doubles help vs. hurt test quality
- [London vs. Chicago (mockist vs. classicist) schools of TDD](https://chuniversiteit.nl/programming/chicago-and-london-schools-of-tdd)- useful framing for *why* people disagree about how much to mock
