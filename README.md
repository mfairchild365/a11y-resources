# A curated list of digital accessibility resources

This is an opinionated list of good accessibility resources for people that want to do some self-learning about accessibility. My goal is to keep this list extremely short, so I had to make hard decisions about what to include and what to leave out. There are a lot of great resources that I'm not listing here.

Your high-level goal for standards should be to learn what sort of information each standard talks about and how they are structured so that you can use them as a reference when searching for an answer. It's impossible to memorize them all.


## What is Digital Accessibility?

* From a minimal compliance perspective: For software to be "accessible" it must be equally usable by someone with a disability as someone without a disability. Minimal compliance is usually measured by WCAG conformance. We should not stop at minimal compliance. 
* From an [inclusive design](https://inclusivedesignprinciples.org/) perspective: accessibility is about going beyond minimal complance and providing good experiences for everyone. 

## This is completely new to me

* [What the heck is WCAG?](https://www.w3.org/WAI/standards-guidelines/wcag/)
* [Give me the fundamentals](https://www.w3.org/WAI/fundamentals/accessibility-intro/)
* [What is a screen reader?](https://alistapart.com/article/semantics-to-screen-readers/)
* [Show me code examples](https://www.w3.org/WAI/tutorials/)
* [Show me more code examples](https://inclusive-components.design/)
* [Accessibility is a civil right](https://www.deque.com/blog/javascript-and-civil-rights/)
* [Evaluating Web Accessibility](https://www.w3.org/WAI/test-evaluate/)
* [I prefer to watch videos (A11ycasts with Rob Dodson)](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

## Standards

Standards can be complex and hard to read, and therefore are often only referenced as a last resort. I'd argue that they should be consulted first. They are the most authorative source of how things **should** work. Some browsers, screen readers, and assistive technology don't always provide full support for the standard, but more often then not, they trend in the direction of support. To provide the absolute best expierence for users, you will need to code to the standards (for forwards compatability), and shim any significant gaps in support (for example, that prevent access) in a way that is also forwards compatible.

* [WCAG Quick Ref](https://www.w3.org/WAI/WCAG21/quickref/) - A dynamic and easy-to-read list of WCAG success criteria (SC). WCAG is the international standard for digital accessibility, so understanding the requirements outlined in this standard is critical to meet conformance. The actual standards can be very hard to read and overwhelming, so the Quick Reference provides another way to quickly glean information. Filter by WCAG version (2.0 or 2.1), level (A, AA, or AAA), and various tags, techniques, and technologies. It also provides links to the understanding documents for each SC and links to relevant techniques.
* [Understanding WCAG 2.1](https://www.w3.org/WAI/WCAG21/Understanding/) - The success criteria in WCAG can often be vague or otherwise hard to understand. This is where the 'Understanding' documents come in. These documents detail each SC, discuss examples, describe the intent of the SC and dive into how meeting the SC benefits people with disabilities. If you ever have a question about an SC - go here first.
* [HTML](https://html.spec.whatwg.org/) - HTML is often overlooked, but it is critical for a developer to understand what is and what is not possible in HTML. The semantics (name, role, value, states, and properties) provided by HTML elements and attributes are what makes screen readers possible. For example, `<button disabled>submit</button>` is announced something like "Button, submit, disabled". Additionally, there are rules about how elements can be nested and what attributes are allowed under different circumstances. Assistive technologies like screen readers have much better support for HTML than ARIA, so reach for HTML first.
* [Using ARIA](https://www.w3.org/TR/using-aria/) - The attributes provided by the Accessible Rich Internet Applications (ARIA) standards are often overused, misunderstood, and implemented in such a way that actually worsens the user experience for people with disabilities. This 'standard' (it's more of a note) explains when to use and not use ARIA. This is a must read.
* [ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/) - ARIA is designed to be malleable and flexible so that developers can make wacky and innovative designs accessible when there isn't a native way build the design (or example, if an HTML element doesn't exist). This document details some common patterns that ARIA can help with and attempts to standardize them. It provides details on expected keyboard interactions and working examples. Check here first if you have to reach for ARIA.
* [ARIA in HTML](https://www.w3.org/TR/html-aria/) - You can't just mix ARIA with HTML willy nilly. To guarantee the best possible support with assistive technologies like screen readers, you should also adhere to the restrictions defined in this document. This document describes which ARIA roles and attributes are allowed on different HTML elements. Tools like axe test against these requirements.
* [ARIA 1.1](https://www.w3.org/TR/wai-aria-1.1/) - If all else fails and you need to roll your own, or if you need to fix something and can't correct the HTML due to silly business constraints, reach for ARIA. However, just like HTML, there are rules around when and where you can use various roles and attributes. Read this before writing any ARIA.
* [Accessible Name and Description Computation 1.1](https://www.w3.org/TR/accname-1.1/) - this standard describes how accessible names and descriptions are computed in various scenarios. This isn't something you will likely need to memorize as a developer, but is a fun deep dive and may help you understand why a screen reader is conveying a specific name or description in certain cirumstances.
* [HTML AAM](https://www.w3.org/TR/html-aam-1.0/) - The HTML Accessibility API Mappings describe how browsers should translate various HTML elements and attributes to system accessibility APIs for consumption by assistive technologies like screen readers. This isn't something most developers need to know about, but can be a fun read if you want a deep dive into how your code is translated into a screen reader experience. Note that there are other AAM documents, such as the [Core AAM](https://www.w3.org/TR/core-aam-1.2/), which focuses on ARIA mappings.

Tools
-----

* [Axe](https://www.deque.com/axe/) - Axe from Deque Systems is a free and open source automated accessibility scanning tool. Download the browser extension and audit your websites and integrate it into your unit tests and CI testing. Also, versions are available for native iOS, Android, and Windows applications.
* [Axe Pro](https://www.deque.com/axe-pro-sign-up/) - Axe Pro, also from Deque Systems is a more robust version of Axe that features guided manual checks.
* [Colour Contrast Analyser](https://developer.paciellogroup.com/resources/contrastanalyser/) - The CCA tool from The Paciello Group is the best color contrast analyzer on the market. Download, install, and use it to grab different colors from your screen (or input colors manually).
* [Microsoft Accessibility Insights for the Web](https://chrome.google.com/webstore/detail/accessibility-insights-fo/pbjjkligggfmakdaogkfomddhfmpjeni?hl=en) - this is a chrome extension that runs automated accessibility testing (via axe) and then walks you through a defined methodology for manual testing with consistent results.

## Education and General Resources

* [Deque University (paid)](https://dequeuniversity.com/) - I may be biased, but this is perhaps the best resource available. It is chock full of expert advice and perfect for self-learning. It covers everything from fundamentals, to web accessibility (basics and advanced), QA testing, Program management, PDF and document accessibility, and even mobile application accessibility. It's fairly inexpensive, and worth every penny.
* [Deque University (free screen reader reference guides)](https://dequeuniversity.com/screenreaders/) - Deque University also provides many free resources, one of which are the screen reader keyboard shortcuts and gestures. These documents are (in my opinion) critical when learning how to use a screen reader.
* [W3C Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/) - The WAI should be one of the first places you look for accessibility information. They have top-notch resources on fundamentals, policy, tutorials, testing, etc.
* [Introduction to Web Accessibility - edX course on accessibility from the W3C WAI](https://www.edx.org/course/web-accessibility-introduction)

## Effective development process

To mitigate finding defects late in the development process and costs related to remediation, accessibility should be shifted as far left in the development process as possible.

* Designs should be reviewed for accessibility before they are implemented.
* The desired assistive technology experience of the designs should be explicity planned for before development starts. See [Accessibility Informed Development (a11yBID)](https://bit.ly/a11yBID).
* Code should be tested for accessibility by developers.
* Code should be tested for accessibility by QA.
* Mechanisms should be in place to monitor accessibility and detect regressions.

## Checklists

I need to start this with a disclaimer. Accessibility is not a checklist. Everyone always asks me for a checklist, which is why I'm including this list. Everything that is in WCAG 2.1 should be on the checklist. As much as you or I might want it to be simpler than that, it just isn't. Remember that WCAG is a **minimum** requirement and doesn't cover everything. You should do acceptance testing and research with people with disabilities. Checklists are most effective when used in planning. That being said, you might find the following helpful.

* [WCAG Quick Ref](https://www.w3.org/WAI/WCAG21/quickref/) - as discussed earlier.
* [WAI: Easy Checks - A First Review of Web Accessibility](https://www.w3.org/WAI/test-evaluate/preliminary/) - a great first check for accessibility.
* [Accessibility Heuristics from Deque](https://accessibility.deque.com/accessibility-heuristics/) - this is a great "checklist" that is especially useful when reviewing designs.
* [Deque University (free) checklist. Links to courses require a subscription, but this is still helpful without a subscription. This is a great resource because it ties each checkpoint to a specific WCAG SC or marks it as a best practice.](https://dequeuniversity.com/checklists/web/)
* [Deque University (paid)](https://dequeuniversity.com/) - also includes various checklists for different team roles and provides a detailed testing methodology for WCAG 2.1.

### More lists

* [WAI: Resources](https://www.w3.org/WAI/Resources/)
* [Some accessibility resources from Scott O'Hara](https://www.scottohara.me/note/2019/05/07/resources.html)
* [My Favorite Resources for Learning Inclusive Design and Accessible Design from Jessica Ivins](https://medium.com/swlh/my-favorite-resources-for-learning-inclusive-design-and-accessibility-b8f24d5a90df?sk=626e600ce8293e2ecc94daf8a65015a9)
* [List of accessibility courses from Mike Gifford](https://github.com/mgifford/a11y-courses)

## Honorable mentions

These are great resources that don't quite fit in the other lists. I can't include everything, but here are some more resources that are worth mentioning.

* [a11ysupport.io](https://a11ysupport.io) - a tool similar to Can I Use, but for accessibility
* [The business case for accessibility](https://www.w3.org/WAI/business-case/)
* [Accessibility Axioms](https://github.com/accessibility/Axioms)
* [The different models of disability](https://www.disabled-world.com/definitions/disability-models.php)
* [Making Content Usable for People with Cognitive and Learning Disabilities](https://www.w3.org/TR/coga-usable/)
* [Law office of Lainey Feingold](https://www.lflegal.com/)
* [ADA Title III (legal news)](https://www.adatitleiii.com/)
* [Inclusive design priciples](https://inclusivedesignprinciples.org/)
* [WebAIM Screen reader survey](https://webaim.org/projects/screenreadersurvey7/)
* [Designing for accessibility and inclusion by Steven Lambert](https://www.smashingmagazine.com/2018/04/designing-accessibility-inclusion/)
* [A Hidden Market: The Purchasing Power of Working-Age Adults With Disabilities (2018)](https://www.air.org/system/files/downloads/report/Hidden-Market-Spending-Power-of-People-with-Disabilities-April-2018.pdf)
* [W3C: Cognitive accessibility user research](https://w3c.github.io/coga/user-research/)
* [Accessibility interview questions by Scott O'Hara](https://scottaohara.github.io/accessibility_interview_questions/)
* [Abelist languge - The Ableist Jar](https://ableist.is/)
* [Disability impacts all of us - infographic from the CDC](https://www.cdc.gov/ncbddd/disabilityandhealth/infographic-disability-impacts-all.html)
* [Disability Statistics](http://www.disabilitystatistics.org/)
* [How to get keyboard focus to work in Safari and Firefox on MacOS](https://www.scottohara.me/blog/2014/10/03/link-tabbing-firefox-osx.html)
* [Start Building Accessible Web Applications Today course by Marcy Sutton](https://egghead.io/courses/start-building-accessible-web-applications-today)
* [List of accessibility resources from the a11yproject, including tools, blogs, sites, books, etc.](https://a11yproject.com/resources/)
* [Contrast Grid](http://contrast-grid.eightshapes.com/?background-colors=&foreground-colors=%23FFFFFF%2C%20White%0D%0A%23F2F2F2%0D%0A%23DDDDDD%0D%0A%23CCCCCC%0D%0A%23888888%0D%0A%23404040%2C%20Charcoal%0D%0A%23000000%2C%20Black%0D%0A%232F78C5%2C%20Effective%20on%20Extremes%0D%0A%230F60B6%2C%20Effective%20on%20Lights%0D%0A%23398EEA%2C%20Ineffective%0D%0A&es-color-form__tile-size=compact)
* [Deque Color palette contrast tool](https://color-contrast-checker.deque.com/)
* [Who Can Use (color contrast tool)](https://whocanuse.com/)
* [Inclusively hiding and styling checkboxes and radio buttons - Sara Soueidan](https://www.sarasoueidan.com/blog/inclusively-hiding-and-styling-checkboxes-and-radio-buttons/)
