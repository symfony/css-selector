CssSelector Component
=====================

CssSelector converts CSS selectors to XPath expressions.

The component only goal is to convert CSS selectors to their XPath
equivalents:

    use Symfony\Component\CssSelector\CssSelector;

    print CssSelector::toXPath('div.item > h4 > a');

Resources
---------

This component is a port of the [Python lxml library](http://lxml.de/cssselect.html), which is copyright Infrae
and distributed under the BSD license.

Current code is a port of https://github.com/lxml/lxml/blob/master/src/lxml/cssselect.py

You can run the unit tests with the following command:
  
  phpunit
  
Limitations
---------

These applicable pseudoclasses are not yet implemented:

* :lang(language)
* :root
* *:first-of-type, *:last-of-type, *:nth-of-type, *:nth-last-of-type, *:only-of-type. All of these work when you specify an element type, but not with *
