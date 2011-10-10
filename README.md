<style type="text/css" media="screen">
.apa,.apa ul,.apa ol,.apa dl,.ref-apa,.ref-apa ul,.ref-apa ol,.ref-apa dl,.apa-ref,.apa-ref ul,.apa-ref ol,.apa-ref dl,.refapa,.refapa ul,.refapa ol,.refapa dl,.aparef,.aparef ul,.aparef ol,.aparef dl{padding-left:0;margin-left:0;}
.apa li,.ref-apa li,.refapa li,.apa-ref li,.aparef li{list-style-type:none;}
.apa p,.apa li,.apa dd,.ref-apa p,.ref-apa li,.ref-apa dd,.refapa p,.refapa li,.refapa dd,.apa-ref p,.apa-ref li,.apa-ref dd,.aparef p,.aparef li,.aparef dd{margin-left:2em;text-indent:-2em;margin-top:1em;margin-bottom:1em;}
</style>

So you’ve written a piece in APA Style and want to show it off online. **The problem:** When you list your references at the bottom, they don’t show *hanging-indent* style, the way APA specifies.

In two simple steps I’ll show you how to apply that **hanging-indent** to reference lists in your blog entry or web page.

✂------✂------✂------✂------✂------✂------✂------✂------✂------✂------

This works with reference lists formatted as paragraphs as well as lists \[[ordered][1], [unordered][2], or [definition][3]\] in HTML or [Markdown][][^1].

##Step 1: How to set it up

Somewhere in your blog’s entry window[^3] —or alternatively, in your blog’s CSS file— paste the following CSS code[^4]\:

    <style type="text/css" media="screen">
      .apa,.apa ul,.apa ol,.apa dl,.ref-apa,.ref-apa ul,.ref-apa ol,.ref-apa dl,.apa-ref,.apa-ref ul,.apa-ref ol,.apa-ref dl,.refapa,.refapa ul,.refapa ol,.refapa dl,.aparef,.aparef ul,.aparef ol,.aparef dl{padding-left:0;margin-left:0;}
      .apa li,.ref-apa li,.refapa li,.apa-ref li,.aparef li{list-style-type:none;}
      .apa p,.apa li,.apa dd,.ref-apa p,.ref-apa li,.ref-apa dd,.refapa p,.refapa li,.refapa dd,.apa-ref p,.apa-ref li,.apa-ref dd,.aparef p,.aparef li,.aparef dd{margin-left:2em;text-indent:-2em;margin-top:1em;margin-bottom:1em;}
    </style>

That’s it! Well, almost.

##Step 2: How to use

Wrap your references inside a `div` element and add the `apa-ref`[^2] value to its class attribute. Use the following guide as an example:

    <div class="apa-ref">
      <h2>References</h2>
      <p>Herbst-Damn, K. L., & Kulik, J. A. (2005). Volunteer support, marital status, and the survival times of terminally ill patients. <em>Health Psychology, 24</em>(1), 225-229. doi:10.1037/0278-6133.24.2.225</p>
    </div>

…if using Markdown, just add the `markdown="1"` attribute inside the `div` element, like so:

    <div class="apa-ref" markdown="1">
    ##References
    Herbst-Damn, K. L., & Kulik, J. A. (2005). Volunteer support, marital status, and the survival times of terminally ill patients. *Health Psychology, 24*(1), 225-229. doi:10.1037/0278-6133.24.2.225
    </div>

That’s all! Either of the two previous formats will output the following:

<div class="ref-apa" markdown="1">
##References
Herbst-Damn, K. L., & Kulik, J. A. (2005). Volunteer support, marital status, and the survival times of terminally ill patients. *Health Psychology, 24*(1), 225-229. doi:10.1037/0278-6133.24.2.225
</div>
  
---

Simple enough, right? Good. If you’d like to know how this works with `ol`, `ul`, or `dl` lists, keep on reading, otherwise you’re good to go!

##Other Examples
If you wrote your references as a list \[[ordered][1], [unordered][2], or [definition][3]\] that’s ok, this will work too. You follow the same rule as before and wrap your list in a `div`. Here are a few guides to make it easier to see:

<h3 id="ordered_list_reference_sample">Ordered list reference sample</h3>
Use this guide (if you’re using Markdown):

    <div class="ref-apa" markdown="1">
    ##References
    1.  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
    2.  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
    3.  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
    </div>

or this (if using HTML):

    <div class="ref-apa">
      <h2>References</h2>
      <ol>
        <li>Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., &amp; Brizee, A. (2010, May 5). <em>General format</em>. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/</li>
        <li>Wegener, D. T., &amp; Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. <em>Journal of Personality &amp; Social Psychology, 66</em>, 1034-1048.</li>
        <li>Wegener, D. T., Kerr, N. L., Fleming, M. A., &amp; Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. <em>Psychology, Public Policy, &amp; Law, 6</em>, 629-654.</li>
      </ol>
    </div>

and you’ll get this:

<div class="ref-apa" markdown="1">
##References
1.  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
2.  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
3.  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
</div>

---
<h3 id="unordered_list_reference_sample">Unordered list reference sample</h3>

Use this guide (if you’re using Markdown):

    <div class="ref-apa" markdown="1">
    ##References
    *  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
    *  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
    *  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
    </div>

or this (if using HTML):

    <div class="ref-apa">
      <h2>References</h2>
      <ul>
        <li>Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., &amp; Brizee, A. (2010, May 5). <em>General format</em>. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/</li>
        <li>Wegener, D. T., &amp; Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. <em>Journal of Personality &amp; Social Psychology, 66</em>, 1034-1048.</li>
        <li>Wegener, D. T., Kerr, N. L., Fleming, M. A., &amp; Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. <em>Psychology, Public Policy, &amp; Law, 6</em>, 629-654.</li>
      </ul>
    </div>

and you’ll get this:

<div class="ref-apa" markdown="1">
##References
*  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
*  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
*  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
</div>

---

<h3 id="definition_list_reference_sample">Definition list reference sample</h3>

Use this guide (if you’re using Markdown):

    <div class="ref-apa" markdown="1">
    References
    :  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
    :  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
    :  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
    </div>

or this (if using HTML):

    <div class="ref-apa">
      <dl>
        <dt>References</dt>
        <dd>Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., &amp; Brizee, A. (2010, May 5). <em>General format</em>. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/</dd>
        <dd>Wegener, D. T., &amp; Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. <em>Journal of Personality &amp; Social Psychology, 66</em>, 1034-1048.</dd>
        <dd>Wegener, D. T., Kerr, N. L., Fleming, M. A., &amp; Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. <em>Psychology, Public Policy, &amp; Law, 6</em>, 629-654.</dd>
      </dl>
    </div>

and you’ll get this:

<div class="ref-apa" markdown="1">
References
:  Angeli, E., Wagner, J., Lawrick, E., Moore, K., Anderson, M., Soderlund, L., & Brizee, A. (2010, May 5). _General format_. Retrieved from http://owl.english.purdue.edu/owl/resource/560/01/
:  Wegener, D. T., & Petty, R. E. (1994). Mood management across affective states: The hedonic contingency hypothesis. _Journal of Personality & Social Psychology, 66_, 1034-1048.
:  Wegener, D. T., Kerr, N. L., Fleming, M. A., & Petty, R. E. (2000). Flexible corrections of juror judgments: Implications for jury instructions. _Psychology, Public Policy, & Law, 6_, 629-654.
</div>

---

###Geek tips
If you’re formatting your lists in HTML, you don’t need to wrap your reference list in a `div`, you can simply apply the class directly to the enclosing element [`ol`,`ul`, or `dl`].

So instead of something looking like this:

    <div class="ref-apa">
      <ul>
        …
      </ul>
    </div>

you can simply add the `class="ref-ata"` to the `ul` element, like this:

    <ul class="ref-apa">
      …
    </ul>

the same applies to `ol` type lists too:

    <ol class="ref-apa">
      …
    </ol>

and

    <dl class="ref-apa">
      …
    </dl>
    
Not too hard, right? I hope you find this tutorial useful. If you have any suggestions, comments or questions, feel free to comment below.

[^1]: To write your references in Markdown format, add the `markdown="1"` attribute to the `div`, `ul`, `ol`, or `dl` enveloping element. Continue reading the tutorial for some examples.
[^2]: As an alternative to `apa-ref`, the following values work interchangeably too: `aparef`, `apa`, `ref-apa`, `refapa`.
[^3]: Make sure you’re working in the HTML View of your blog’s entry window
[^4]: Explanation for beginners\: The CSS code contains the instructions for displaying your references with the hanging indent.

*[APA]: American Psychological Association
*[CSS]: Cascading Style Sheet
*[HTML]: Hyper Text Markup Language

[Markdown]: http://daringfireball.net/projects/markdown/
[1]: #ordered_list_reference_sample
[2]: #unordered_list_reference_sample
[3]: #definition_list_reference_sample
