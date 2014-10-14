stupidlySimpleGrid
=========

A very simple semnatic grid taking inspiration, or stealing from a few good sources.

  - Little to no extra markup
  - Easy to use with media queries
  - Little bits of media query and scss functions borrowed from zurb foundation - which is amazing by the way.

What-da fuk?
----

Three simple mixins

```
rowClear()
row($clearBool, $gutter)
column($width, $padding)

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

1.1

