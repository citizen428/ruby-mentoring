In this exercise I want you to write a little DSL for XML/HTML. Look at the following client code:

    title = tag_builder("h1")
    para = tag_builder("p")
    link = tag_builder("a")
    bold = tag_builder("b")

    puts title["Test"]
    puts para["This is a paragraph"]
    puts link["A link", :href => "http://foo.com"]
    puts para[bold["Bold text with", link["a link", :href => "http://bar.com"], "inside a paragraph."]]

This is the output it produces:

    <h1>Test</h1>
    <p>This is a paragraph</p>
    <a href="http://foo.com">A link</a>
    <p><b>Bold text with <a href="http://bar.com">a link</a> inside a paragraph.</b></p>

Your challenge is implementing the `tag_builder` method used above, so you can go and build friendly HTML DSLs for your non-techy friends.
