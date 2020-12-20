# Petricor CSS 💦

Petricor CSS is an utility library for building web interfaces. It’s build
in SASS and provides a full collection of utility classes that helps you work
faster and apply css without almost switching between css and html. It's
heavily influenced by [Tailwind CSS](https://tailwindcss.com/).

## Key concepts

### Wide collection of tiny utility classes

Detaching properties into tiny functional classes makes your code more reusable,
less dependent and portable. Having classes doing too much leads to scalable
issues in the middle-long term.

Remove the process of thinking about naming your classes or adopting
nomenclatures like **BEM**. No more abstract class names that need new modifiers
to accommodate similar looking components. You’ll know exactly what they’re
doing by just looking at them. Your components will be _self-descriptive_.


### Low specifity

As a general rule the majority of classes have a specificity as low as `0,0,1,0`.
Specificity wars with `!important` won’t bother you anymore. There are
some fewer exceptions where it does make sense to take advantage of the cascade.
For those specific cases the specificity will increase up to `0,0,2,0`.

### Made to be customized

All these utilities are generated from a single source of truth. A config file
with sass maps containing presets for spacings, colors, typography, box-shadows,
transforms, etc.

CSS authors can extend, modify, enable or disable utilities and variants.
Customizing Petricor CSS is really easy and you can do so without modifying the
core library. This way you can update to new versions without loosing your setup.
