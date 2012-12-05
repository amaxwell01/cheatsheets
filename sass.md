## Setting up responsive breakpoints
```
/* ==========================================================================
   Media Queries
   * How to use breakpoint
   * @include breakpoint(large) { width: 60%; }
   ========================================================================== */
@mixin breakpoint($point) {

    @if $point == small {
        @media (max-width: 770px) { @content; }
    }
    @else if $point == medium {
        @media (min-width: 771px) and (max-width: 1250px) { @content; }
    }
    @else if $point == large {
        @media (min-width: 1251px) { @content; }
    }
}
```

## Lighten a color
```
lighten(#BADA55, 20%);
```

## Darken a color
```
darken(#BADA55, 20%);
```
