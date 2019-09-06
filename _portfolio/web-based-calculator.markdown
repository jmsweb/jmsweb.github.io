---
layout: page
title: Web-based Calculator
description: A functional mockup of iOS calculator written with HTML, CSS, and JavaScript.
img: /assets/img/web-calculator.png
jquery: true
comments: true
date: September 3, 2019
---

Some time ago, I was wondering whether it is feasible to develop a replication of iOS calculator in web browser. So, one night my inspiration and energy were strong
enough to start being creative with native JavaScript and CSS. I had my own iPhone with calculator to study for feedback in part of design process for coding.

Few key features are left out due to time and schedule. The feature are scientific view when iPhone is in landscape mode, `AC` and `C` toggle behavior, and
backspacing digits. I'm sure there are other key features that I hadn't noticed because I don't use iOS calculator that often.

This HTML5 Table is also responsive in either Desktop and Mobile view. You could even resize the web browser or view in your mobile device and the table
would fit nicely on screen!

<link rel="stylesheet" type="text/css" href="{{ '/assets/css/web-calculator.css'}} ">
<div id="calculator-container">
    <table id="calculator-table">
        <tbody>
            <tr>
                <td colspan="4" class="screen">0</td>
            </tr>
            <tr>
                <td class="function custom-ac">AC</td>
                <td class="function">&#177;</td>
                <td class="function">&#37;</td>
                <td class="operand">&#247;</td>
            </tr>
            <tr>
                <td>7</td>
                <td>8</td>
                <td>9</td>
                <td class="operand">&#215;</td>
            </tr>
            <tr>
                <td>4</td>
                <td>5</td>
                <td>6</td>
                <td class="operand">&#45;</td>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td class="operand">&#43;</td>
            </tr>
            <tr>
                <td colspan="2" class="zero">0</td>
                <td>&#46;</td>
                <td class="operand">&#61;</td>
            </tr>
        </tbody>
    </table>
</div>
<script type="text/javascript" src="{{site.baseurl}}/assets/js/web-calculator.js"></script>

Fork and clone my repository at [Web Based Calculator](https://github.com/jmsweb/web-calculator). If there are anything that could be improved, go ahead and create
a pull request for review.
