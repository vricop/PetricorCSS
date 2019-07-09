# /utils

This folder contains helper mixins for generating all the css utilitiy classes.
The majority of this mixins make use of the `_config.scss` file where default
settings are set. These can be extended and/or overwritten by css authors.

## @mixin: bundle-responsive-utilities

```scss
/*
  $breakpoint <map>
  @content <css-rules-collection>
*/
@include bundle-responsive-utilities($breakpoint) {
  @content;
}
```

Bundles every utility class into its corresponding mediaquery without duplicating
`@media` rule declarations. This reduces file size considerably. The
`$breakpoint` parameter takes a map of breakpoints. Default breakpoints are set
in the `$breakpoints` map defined in `_config.scss`. `@cotent` will contain a
collection of css rules passed as a content block into the mixin.

## @mixin: generate-variants-with-config

```scss
/*
  $utility-config <map>
  $utility-variants <list>
  $screen <map>
  @content <css-rule>
*/
@include generate-variants-with-config(
  $utility-config,
  $utility-variants,
  $screen
) {
  @content;
}
```

Generates utility variants that are configurable via `_config.scss`.
`$utility-config` takes a map with a key-value pair for a given utility.
`$utility-variants` takes a list of variants stored in `$variants` map defined
in `_config.scss`. `@cotent` will contain a css rule passed as a content block
into the mixin.

## @mixin: generate-variants

```scss
/*
  $utlity-variants <list>
  $screen <map>
  @content <css-rule>
*/
@include generate-variants($utility-variants, $screen) {
  @content;
}
```

Generates utility variants that aren't configurable. These variants are the same
as above. `@cotent` will contain a css rule passed as a content block into the
mixin.

## @mixin: mediaquery

```scss
/*
  $min <map>
  $max <map>
  @content <css-rules-collection>
*/
@include mediaquery($min, $max) {
  @content;
}
```

Generates a mediaquery based on the arguments passed. If both `$min` and `$max`
a combined mediaquery will be created:

```scss
@media (min-width: 640px) and (max-width: 768px) {
  /* Utilities here */
}
```

If only `$min` is passed, then:

```scss
@media (min-width: 640px) {
  /* Utilities here */
}
```

...and last if only `$max` is passed the next mediaquery will be generated:

```scss
@media (max-width: 768px) {
  /* Utilities here */
}
```
