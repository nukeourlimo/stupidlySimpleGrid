stupidlySimpleGrid
=========

A very simple semnatic grid taking inspiration, or stealing from a few good sources.

  - Little to no extra markup
  - Easy to use with media queries
  - Home made, like a nice warm apple pie, dont put your todger in it though.

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
    @include column(75%)
}

aside {
    @include column(25%)
}
```


Version
----

1.0

