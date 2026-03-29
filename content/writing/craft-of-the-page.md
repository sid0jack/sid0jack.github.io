---
title: "The craft of the page"
date: 2026-03-20
tags: ["design", "web"]
---

Every design choice on a page is a small argument about what matters. The background color says *this is the kind of place you're in*. The typeface says *this is how seriously we take the words*. The measure — the width of a line of text — says *we thought about how your eyes move*.

This post exists to exercise every design element on the site.

## Typography and prose

Body text is set in Literata at 18px with a line-height of 1.7. The measure is capped at 68 characters — wide enough to read comfortably, narrow enough that your eyes don't lose their place on the return sweep.

**Bold text** and *italic text* work as you'd expect. Links look [like this](/colophon/) and change color on hover.

> The details are not the details. They make the design.
>
> — Charles Eames

Lists work too:

- Dark backgrounds reduce eye strain at night
- Warm off-whites are easier to read than pure white on dark
- Accent colors should be used sparingly

And ordered lists:

1. Choose a typeface that matches the tone
2. Set a comfortable measure
3. Let the content breathe

---

## Code

Inline code looks like `fn main()` — a subtle background distinguishes it from prose.

Here's a block of Rust:

```rust
fn fibonacci(n: u64) -> u64 {
    match n {
        0 => 0,
        1 => 1,
        _ => fibonacci(n - 1) + fibonacci(n - 2),
    }
}

fn main() {
    for i in 0..10 {
        println!("fib({}) = {}", i, fibonacci(i));
    }
}
```

And some Go for contrast:

```go
package main

import "fmt"

func fibonacci(n int) int {
    if n <= 1 {
        return n
    }
    return fibonacci(n-1) + fibonacci(n-2)
}

func main() {
    for i := range 10 {
        fmt.Printf("fib(%d) = %d\n", i, fibonacci(i))
    }
}
```

Code blocks show the language in the top-right corner. Hover to reveal the copy button.

## Interjections

These are the signature element — character asides that break up long technical prose.

{{< bear >}}
If you're building a blog, start with the writing. The design can come later. A Markdown file in a Git repo is a perfectly good blog.
{{< /bear >}}

Margin notes are for brief asides that complement the main text:

{{< margin >}}
The term "measure" comes from traditional typesetting. Robert Bringhurst's *The Elements of Typographic Style* recommends 45–75 characters per line.
{{< /margin >}}

And caution blocks for things the reader should be careful about:

{{< caution >}}
Self-hosting fonts means you're responsible for subsetting. Shipping a full-weight variable font when you only need Regular and Bold wastes bandwidth and slows first paint.
{{< /caution >}}

## Headings at every level

### Third level

This is text under an h3. It's useful for subsections within a larger topic.

#### Fourth level

Rarely needed, but styled for completeness.

---

That's every element. The goal is a page that feels *designed* without feeling *decorated* — every choice in service of readability.
