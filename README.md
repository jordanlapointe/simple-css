Simple CSS
==========

A simple set of rules for CSS development.

# Beliefs
Simple CSS belives that CSS guidelines should:
1. Be easy to teach.
2. Have few rules.
3. Make use of the latest technologies.
4. Communicate clearly.

# Rules Set
## HTML should be written like this
``` HTML
<!--==============================================
 Send Feedback Form (sff)
===============================================-->
<div class="sff-wrap">
	<form>
		<textarea class="sff-message"></textarea>
		<input class="sff-field" type="email">
		<input class="sff-send is-hidden" type="submit" value="Send message">
	</form>
</div>
```

## Styles should be be written like this
``` SCSS
/*================================================
 Send Feedback Form (sff)
==================================================
 Small form allows guests to submit feedback on
 the homepage. Near the bottom of the page.
================================================*/
.sff-wrap {
	margin: auto;
	padding: $spacing-2x;
}
.sff-message,
.sff-field {
	margin-bottom: $spacing-1x;
}
.sff-send {
	&.is-hidden {
		display: none;
	}
}
```

## A file should be included just for variables
The values entered in CSS should come from pre-defined variables, not manually typed-in each time. This keeps things consistent and more visually pleasing.

``` SCSS
/*================================================
 Variables
==================================================
 Cached values to be used throughout the project.
==================================================
 Abbreviations used:
 s = small
 m = medium
 l = large
 x = extra
================================================*/
/*== Font Sizes ==*/
$font-s:   0.75rem; // 12px
$font-m:   1rem;    // 16px
$font-l:   1.25rem; // 20px
$font-xl:  1.5rem;  // 24px
$font-xxl: 2rem;    // 32px

/*== Vertical Spacing ==*/
$spacing-half: 0.375rem; // 6px
$spacing-1x:   0.75rem;  // 12px
$spacing-2x:   1.5rem;   // 24px
$spacing-4x:   3rem;     // 48px
$spacing-8x:   6rem;     // 96px

/*== Colors ==*/
$color-primary:    #0fd8c5; // Teal
$color-secondary:  #005f69; // Dark teal
$color-grey:       #a7a9ac;
$color-grey-light: #f6f6f6;
$color-grey-dark:  #393939;
```
