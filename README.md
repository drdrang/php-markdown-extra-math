PHP Markdown Extra Math is an extension of Michel Fortin's [PHP Markdown Extra][1], a PHP script for converting text written in [Markdown][2] to HTML. The extension consist of adding support for mathematical equations written in LaTeX to be processed by Davide Cervone's [jsMath][3] system.

Here's how it works. The author, writing in Markdown, inserts inline equation like this

    where \(\alpha = (t_1 - t_0)/L\) is the rate at which the thickness increases

enclosing the math in a `\( … \)` pair, just as if writing in LaTeX. PHP Markdown Extra Math converts that to 

    where <span class="math"> \alpha = (t_1 - t_0)/L </span> is the rate at which the thickness increases

which is then converted by jsMath into

![inline math example](http://www.leancrew.com/all-this/images/math-inline-example.png)

(The example is shown as an image here because I don't know how to get jsMath working on GitHub. On a site with jsMath installed, the equation will be rendered as selectable and scalable text.)

Similarly, display Math is written like this:

    Putting this into Castigliano's equation, we get
    
    \[\Delta = \frac{\partial U^*}{\partial F} = \frac{12F}{Eb} \int_0^L \frac{x^2}{(t_0 + \alpha x)^3} dx\]

which PHP Markdown Extra Math will turn into this HTML

    <p>Putting this into the Castigliano equation, we get</p>

    <div class="math">\Delta = \frac{\partial U^*}{\partial F} = \frac{12F}{Eb} \int_0^L \frac{x^2}{(t_0 + \alpha x)^3} dx</div>  

which, in turn, will be rendered by jsMath like this:

![display math example](http://www.leancrew.com/all-this/images/math-display-example.png)


PHP Markdown Extra Math is licensed under the same terms as PHP Markdown Extra. See the License.text file.

[1]: http://michelf.com/projects/php-markdown/extra/
[2]: http://daringfireball.net/projects/markdown/
[3]: http://www.math.union.edu/~dpvc/jsMath/
