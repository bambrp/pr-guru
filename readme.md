# PR Guru

## Introduction

*PR Guru* is a kiosk mode style single page application for displaying open pull requests on a TV, in the same vein as Stalemate and Fourth Wall.

## Usage

Open the index.html file in your browser, with a fragment identfier of the organisation/repo, semi-colon separated. e.g.

```sh
file:///$PWD/index.html#bambrp/pr-guru;ONSdigital/eq-survey-runner
```

Here the fragment identifier is `#bambrp/pr-guru;ONSdigital/eq-survey-runner`, which will retrieve open PRs for both **bambrp/pr-guru** and **ONSdigital/eq-survey-runner**.

Enter your GitHub API key into the box at the top of the page and hit return. This will be remembered in the browser's LocalStorage. Entering an empty string will dismiss the box without overwriting the existing API key.

## Limitations

If you do not provide an API key, you will be limited in how often you can make requests, and if you are going through a NAT gateway, and your IP is shared with other machines, you might hit that limitation quickly.

More caching is required- this would make deeper requests more palatable, by looking up child requests less frequently.

It needs some sort of carousel functionality, to display without user interaction, further pages of results, instead of cutting it off at one screen's worth.
