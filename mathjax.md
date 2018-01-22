{% include mathjax.html %}
# Enabling MathJax

This site template has been pre-enabled with MathJax, so if you use this as the base of your project (removing the links to or re-writing the existing pages), you shouldn't need to do anything special to enable MathJax. Just follow the instructions below.

The most important thing to remember for using MathJax in GitHub Pages is to add a [special include](https://jekyllrb.com/docs/includes/) to the top of each page in which you will be using it. In this case, that means adding `include mathjax.html` surrounded by `{``%`   `%``}` 

This tells the browser to include the script I've put in `_includes/mathjax.html` in the home directory, which enables MathJax:

``` {% include mathjax.html %} ```

Once you do this, it's very simple to use MathJax with GitHub pages with markdown.

# Using MathJax with Markdown

Kramdown, the markdown translater this GitHub Pages site is setup to use, has special support for $$ to delimit both inline and block equations.

For example, `$$ \frac{1}{n^{2}} $$` is rendered as a block equation here:

$$ \frac{1}{n^{2}} $$


It's the same process for more complex formulae, such as 

```$$ J(\theta) = \frac{1}{2m}(\sum_{i=1}^m(h_\theta (x^{(i)}) - y^{(i)})^2 + \lambda\sum_{j=1}^n\theta^2_j) $$```

Rendered as:

$$ J(\theta) = \frac{1}{2m}(\sum_{i=1}^m(h_\theta (x^{(i)}) - y^{(i)})^2 + \lambda\sum_{j=1}^n\theta^2_j) $$

You use the same basic syntax to render `$$a^2 + b^2 = c^2$$` inline: $$a^2 + b^2 = c^2$$

You can also use different typesets or [math alphabets](http://milde.users.sourceforge.net/LUCR/Math/math-font-selection.xhtml), such as \mathbf:

$$ \mathbf{X}_{n,p} = \mathbf{A}_{n,k} \mathbf{B}_{k,p} $$

## Additional Resources

* [MathJax](http://docs.mathjax.org/en/latest/)
* [Setting up MathJax on GitHub Pages by Gianluca Casati](http://g14n.info/2014/09/math-on-github-pages/)

