# Accessibility personas - getting started with accessibility

Accessibility is a deep and complex topic. This is meant to be a very quick introduction to various types of disabilities, how disabilities can affect human-computer interaction, and some basic testing techniques. There is much more to learn than what I can provide here, but hopefully, this is a simple way to get your toes wet.

Think about disabilities and accessibility this way: People are disabled by the content not being accessible, not their physical limitations. If the content is accessible, their body's physical limitations do not matter. In other words, it's the environment and culture that disable people… not their bodies.

- **A word of encouragement**: Don't let perfection get in the way of progress. Understanding accessibility takes time and practice. Start small now, and grow your skills over time. You also do not need to be an accessibility expert.
- **A note about these personas**: The personas do not represent real people. They are generic representations of how a disability might show up in the real world, but they are also oversimplified. Not all disabilities are represented, and many people have multiple disabilities.

[Go back to the readme file to learn more about digital accessibility](README.md).

## Persona 1: Katie - Sighted keyboard-only user
Testing difficulty: 1/5.

Katie has limited control over her hands due to a car accident. Because of this, she uses assistive technologies that behave like keyboards to interact with her computer.

Why it matters: We need to ensure that sighted users with motor disabilities can use just a keyboard (no mouse) to complete their tasks. This will allow the user to use many assistive technologies to interact with the page.

How to test:

1. Use the tab key to tab through interactive controls on the page. Tab forward and backward.
   - Note: You need to enable keyboard functionality on Macs. Read [Enabling Keyboard Accessibility on a Mac in Deque Univeristy](https://dequeuniversity.com/mac/keyboard-access-mac).
2. Make sure that every interactive control is in tab order.
   - Note: some controls will contain many sub-controls, such as tab panels, date pickers, menus, etc. It's okay if the user can use arrow keys to navigate within these (but not the tab key).
3. Make sure that it is obvious which element has keyboard focus at all times (there needs to be a clear visual indicator - and the browser's default is fine!)
4. Make sure that every control can be activated/edited by just using the keyboard.
5. Make sure that keyboard focus never disappears and that it never becomes trapped.

## Persona 2: Stacie - low-vision user
Testing difficulty: 2/5.

Stacie was born with color blindness and has lost a significant amount of vision over the years due to diabetes, but does not identify as blind.

Why it matters: We need to make sure that content is easy to read for users with low vision.

How to test:

1. Use the [axe DevTools extension](https://chrome.google.com/webstore/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd) to automatically check the color contrast of text. However, this tool will not automatically catch everything and will not check the contrast of graphical objects. It does help to speed things up!
   - Ensure that the color contrast of graphical objects is sufficient. Use the Deque Color Contrast Checker to manually test and read more about the requirements. 
2. Look for any information that is conveyed by color alone. Ensure that there is supporting text and shapes, or that the information is conveyed in some other way than just color. 
   - Examples might include: 
      - Red text to indicate that a form control has an error.
      - Blue text to indicate a link in the middle of a paragraph of text (no underlines or other non-color differences between surrounding text).
   - Hint: print the page in black and white. Can you still tell what everything means?

## Persona 3: Richard - cognitive disability user
Testing difficulty 2/5.

Richard was born with ADHD and has short-term memory loss. Because of this, he tends to forget quickly and get distracted easily.

Why it matters: Cognitive disabilities are the most common form of disability, and often go undiagnosed. It's also the most diverse group of disability and can manifest in many different ways. We need to account for this diversity in our content.

How to test:

1. Ensure that the design is simple and consistent to the extent that is possible.
   - For example, is it clear and easy to figure out how to complete the task with minimal distractions?
2. Ensure that plain language is used wherever possible - avoid complex language.
3. Ensure that page titles and headings are meaningful and accurately describe their content.
4. Ensure that labels, instructions, and help text for forms are meaningful.
5. Ensure that it is clear which form fields are required, and how to fix any errors.
6. Ensure that reliance on memory, especially in long forms or processes, is minimal to the extent possible.
7. If icons are used, ensure that their meaning is obvious - consider adding text next to icons, or icon legends, so that no one has to guess.
8. Ensure that there is a way to remove or reduce motion, such as animations or auto-playing videos.

## Persona 4: Natalie - deaf user
Testing difficulty: 2/5.

Natalie has been deaf from birth. Because of this, she relies on captions for videos.

Why it matters: Deaf users will not be able to hear any audio, such as audio found in videos or used as cues. Visual alternatives to audio must be used.

1. Ensure that all videos have accurate captions.
2. Ensure that all sound cues are accompanied by a visual cue that does not depend on sound.

## Persona 5: Abe - seizures
Testing difficulty: 2/5.
Abe has photo-epileptic seizures. If the media has too many flashes of light, it can trigger a serious seizure for him and land him in the hospital.

Why it matters: Flashes of light can trigger seizures and hurt users. Avoid them at all costs.

1. Ensure that there is not a series of 3 flashes of light per second or more in any content or media. 

## Persona 6: Justin - blind screen reader user
Testing difficulty: 5/5.

Justin is legally blind and uses a screen reader to interact with his phone and computer. Even though Justin is legally blind, he still has a small amount of vision - but can only make out general shapes.

Why it matters: Screen reader software will announce more than just the text that is on the page. It will also announce what each element is (a button, link, list, table, etc.), and any relationships and structure (heading level, table cell headers, etc.). Screen readers will also announce states and properties of elements (expanded/collapsed, active, selected, etc.). A blind user needs to hear all the information that a sighted user can glean from visual hints/cues and affordances.

How to test:

1. Use automated tools like [axe DevTools](https://chrome.google.com/webstore/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd).
   - This can catch many issues but won't catch everything. 
3. Use a screen reader to verify that the experience is well-supported. There are many different screen readers, both paid and free.
   - **If you are using Windows**: start with [NVDA](https://www.nvaccess.org/download/). It's a popular free and open-source screen reader.
     - Tip: Open the Speech Viewer. Go to tools, then click 'speech viewer'. The screen reader does a lot of talking, and it can get overwhelming. This log can help you keep track of what was said.
     - Tip: Turn on Visual Highlight. Go to settings, vision, then check 'visual highlight'. This will highlight what the screen reader is reading on the page, which can be extremely helpful for new, sighted, users.
     - Tip: Print out the [Deque University screen reader reference guide for NVDA](https://dequeuniversity.com/screenreaders/nvda-keyboard-shortcuts). Review this document before opening the screen reader. The screen reader has a lot of unique commands.
   - **If you are using a Mac**: start with VoiceOver. It's free and built into the operating system.
     - You can open VoiceOver in the system's accessibility settings.
     - Tip: Print out the [Deque University screen reader reference guide for VoiceOver](https://dequeuniversity.com/screenreaders/voiceover-keyboard-shortcuts). Review this document before opening the screen reader. The screen reader has a lot of unique commands.
   - **What does "well supported" mean?** How do I know if the screen reader is saying the right thing?
     - This is what makes testing with screen readers so difficult. Each screen reader has its own quirks, commands, bugs, and opinions on how to announce things. That's okay, and expected, but it also makes it difficult to learn how to test with screen readers.
     - My general advice is: if you think something isn't working, take a pause and do some research. Don't jump to conclusions. Often just because it seems like something might be broken... it really isn't. Screen readers will often try to minimize announcements and convey information implicitly or via context. Or, you might just be testing with the wrong screen reader command. Some tips for effective research:
        - Build your own minimal prototype (just raw HTML and little to no CSS and JS), then test it with the screen reader.
        - Review the available screen reader commands - is there a specific command that may expose the information you expect?
        - Review [a11ysupport.io](https://a11ysupport.io) to see if there are known support or bugs for what you are testing. This can also help you understand what the screen reader's expectations are for given elements.
        - Look for known good implementations of similar patterns and test those with the screen reader. Unfortunately, this is somewhat scattered across the web and this info isn't always very trustworthy.
5. Ensure that videos have transcripts (the only way deaf-blind users can 'watch' videos).
6. Ensure that any auto-playing audio will stop after 3 seconds or that there is a mechanism to pause it (so that the audio doesn't interfere with the screen reader).

