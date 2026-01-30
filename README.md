# RULE

Hello! If you are interested in contributing to the Rules Library for Buried Giant, you can do so in two ways.

If you have a rules issue, or an issue with the website itself, please open up an Issue. Proposed errata, as well as proposed FAQs that rest on contested logic, should be always Issues.

If you have a fix to propose, please open up a Pull Request. All of the relevant rulebooks, errata, and FAQs are contained in `rules,yml`, `errata.yml` and `faq.yml` in their game folders in `content/rules`. Here are some examples of good Pull Requests:
- An FAQ that has already been discussed and answered in an unambiguous way, either in the Github or by the community at large, but for some reason isn't in the Library.
- A clear issue in how the Library represents the reality of the product. (For example, a typo or other issue in the plaintext on the site that doesn't match the actual text on the rulebook.)
- Already-printed errata that is not reflected in the Library.

If you're interested in forking this code and using it yourself, you'll find what you need below.

## Getting Started

1. `npm i`
1. `npm run compile:rules`

## Adding/Updating a New Game or Language

1. Create/update the game and/or language in `content/app.yml`
1. Create/update a folder in `content/rules/` with the game's short name (e.g. `arcs`)
1. Create/update a folder in `content/rules/<game>/` for the version of the game rules you want to add (e.g. `p1`) - _note: printings should be `p<number>` to ensure correct ordering_
1. Create/update a folder in `content/rules/<game>/<printing>/` for the language of the rules you want to add (e.g. `en-US`)
1. Create/update the necessary YAML files (`rules.yml`, `faq.yml`) in `content/rules/<game>/<printing>/` - _note: `faq.yml` is optional, but `rules.yml` is not_
1. Create/update `appconfig.yml` in `content/rules/<game>/`
1. Create/update `errata.yml` in `content/rules/<game>/` - _note: this is optional_

If you want to make a new game available to view without populating it in the publicly accessible menu, follow all of these steps except step 1, then
view it using this URL: "https://rules.buriedgiantstudios.com/?product=XXX&locale=XXX&printing=XXX", replacing the "XXX" with the appropriate names.
