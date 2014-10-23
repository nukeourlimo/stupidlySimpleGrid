stupidlySimpleGrid
=========

A very simple semnatic grid taking inspiration, or stealing, from a few good sources. You need scss for this.

  - Little to no extra markup
  - Uses box-sizing.
  - Easy to use with media queries
  - Little bits of media query and scss functions borrowed from zurb foundation - which is amazing by the way, really you should head over there if you want a markup based grid and loads of other cool stuff to make your life easier!
  - As small a css footprint as i could manage, however im sure it can be done smaller/better (maybe version 2 ay?)

What-da fuk?
----

Three simple mixins

```
rowClear()
row($clearBool, $gutter)
column($width, $padding, $centerBool)

```

Some media query goodness pinched from zurb foundation (see the _fmqs.scss)

```
$large-up, $medium-up, $small-up, $large-only, $medium-only, $small-only, etc!
```

A couple of useful queries to put in your @media I would assign them to vars which makes the media query nicer to read.

```
customRange($min, $max)
customRangeHeight($min, $max)
```

How do I use this?
----

```
<article>
    <header></header>
    <aside></aside>
</article>

$padding: 50px;
$gutter: 50px;

article {
    @include row()
}

header {
    @include column(75%);
    
    
    @media #{$small-only}{
      @include column(100%, 0px);
    }
    
    $customHeight: customRangeHeight(0px, 100px);
    
    @media #{$customHeight}{
      //do something with the custom height!
    }
}

aside {
    @include column(25%)
    
    @media #{$small-only}{
      @include column(100%, 10px);
    }
}

```


Version
----

1.3

