# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed

- Change spacing to logical properties

### Added

- Add `snap` and `scroll` utilities
- Add `animation` utilities
- Add `nth-*` customizable utilities
- Add `direction-{ltr|rtl}` utility
- Add documentation

## [1.0.0] - 2020-10-27

### Changed

- Rename `duration-{speed}` utility to `duration-{duration}{ms|s}`
- Replace `truncate-multiline` with `line-clamp` utility
- Refactor &ldquo;lobotomized owl&rdquo; variants for `margins`
- Removed configuration maps: `$padding-em`, `$padding-ch`, `column-gap-em`,
  `column-gap-ch`, `border-width-em`, `$border-radisu-em`, `$font-size-em`.
- Changed all spacing utilities to a single [$spacing configuration map](https://github.com/vricop/PetricorCSS/blob/dc2d2226a2f9df5c77eb5b129cf5aec4055e243a/_config.scss#L225)
- Fixed `font-family` utility, responsive variant was missing.
- Refactored `transform-*` utilities.
- Fixed missing variants in `non-configurable-variants`
- Refactored `align-{type}`, `justify-{type}` and `content-{type}` utilities to
  make them configurable
- Fixed `group-hover` variants not generating for the `bg-{color}` utility
- Refactored stack variants for `m{t|l}-{size}`, `border-*` to standalone
  utilities: `stack-gap-{x|y}-{size}`, `stack-rule-{x|y}-{size}`,
  `stack-rule-{color}`, `stack-rule-{style}`   
- Rename `max-h-none` to `max-h-0`

### Added

- PetricorCSS is now available as [NPM package](https://www.npmjs.com/package/petricorcss).
- Add info to `README.md`
- Add info to `CHANGELOG.md`
- Add easy author customization with the [new sass modules system](https://sass-lang.com/documentation/at-rules/use#configuring-modules).
- Add variants: `::placeholder`, `:disabled`, `:visited` and `:empty`
- Add `stack` variant for `mt-{size}`, `mb-{size}`, `border-{side}` and
  `border-{color}` utilities
- Add `sr-only` and `not-sr-only` screenreader a11ty visibility utilities
- New `link-stretch` utility helper
- Add `&group-hover:` variant. It only applies to direct children, as opposed to
  `group-hover` which applies to any element no matter how deep.
- Add `caret` utility
- Add `line-clamp` utility
- Add `font-feature-settings` utility
- Add `flex-basis` utility
- Add utilities: `grid-{rows|cols}-{n}`, `row-{span|start|end}-{n}`,
  `col-{span|start|end}-{n}`, `gap-{n}`, `{col|row}-gap-{n}`.
- Add `multilayout-colum` utilities: `col-count-{n}`, `col-rule-{style|width}`,
  `col-rule-width`, `col-rule-color`.
- Added `max-w-screen-{screen}` and `max-w-screen-none` utilities
- Added  `caption`, `thead`, `tbody`, `tfoot`, `tr`, `td` and `list-item` values
  to display utilities
- Added fixed `rem` values to `leading-{size}` utility
- `bg-{size}` utility is now configurable
- Added `shadow-xs` to `shadow-{size}` utility
- Added `place-{items|content}-{position}` utilities
- Added custom properties for colors

## [0.7.1] - 2020-01-11

### Changed

- Base reset styles refactored.

## [0.7.0] - 2020-01-07

I decided to tag this first release as v0.7.0 after publishing my personal
project on Github. I worked on this project in a local repository for a year or
so. It started as an experiment to play with functional css and it has become
something more. This project is inspired in Tailwindcss but build in SCSS.