# Visual Readability
1.
The scale of text displayed on a page is incredibly important to maintaining an accessible website. At a glance, it seems that most of the text on this web page is scaled well. However, one area where we could improve this scaling is the short description for the stories. It is recommended for the text size to be between 18 to 20 pixels.

Let’s fix this! In style.css, find the .summary selector ruleset. Set the value of the font-size property to be within the recommended range.


2.
Increasing the font size made it much easier to read the summary, but it could be improved even further!

Size is important for legibility, but so is structure. The lines of our summary text seem pretty close together, which affects our ability to read it, especially if there were more lines of text.

Let’s fix this spacing between the lines by setting the line-height property to 1.5 for the .summary selector.



3.
Now that our lines are properly spaced, we can turn our attention to the spacing of each letter. Sometimes, smaller spacing between letters can cause readers with visual impairments to have a difficult time.

To remedy this, let’s increase the spacing between the individual letters of our paragraphs of the summary class to a value of 1.2.

4.
Our summaries are really shaping up nicely now, but there is more work to be done.

Now that our paragraphs have been spaced out, we can see that some of the spacing between words looks a bit off. This is due to our text alignment, which is currently set to justify. To increase the readability of the paragraphs of the summary class even more, let’s change this alignment to left.



5.
Awesome! Our paragraphs are very accessible now!

While our text looks great, you may have noticed some problems with the color contrast of certain elements on our page. Contrast is immensely important when it comes to visual readability, and it is clearly harming the readability of text on our web page.

Find the .primary-text-color ruleset and change the value of the color property to one with a more discernable contrast. You can choose any color for this, but try to make sure it has a contrast ratio of at least 3:1. Use tools like WebAIM to check the contrast of your color choice.



Contextual Readability
6.
Now that our content is visually accessible, we can augment the accessibility even further through contextual clues.

One way we can do this is by drawing attention to interactable elements. For instance, indicating to a user that an element is a link is one way to provide these clues. In fact, we have some links on this page of which the user should be aware of.

Let’s add some styling to these links on hover to indicate their purpose to the user. Find the a:hover selector ruleset and give it a color to change into when links and icons are hovered over. Additionally, change the cursor to a pointer.



7.
Great! Now our users will know what elements are links, and in a rather stylish way too.

Another area where we can add some interactive flair to improve accessibility is in our search input. Currently, clicking on the search input doesn’t really do anything. We should provide a visual clue that the search input is in focus when clicked.

Let’s accomplish this by adding a border color to the input when it is focused. Find the input:focus selector and add a solid border of 1-pixel thickness. The color of the border can be whatever you choose, but try to make sure has enough contrast.



8.
So far, every way we have provided context to elements on our web page involved color. There is another way to add more context without using colors!

You may have noticed some acronyms in the titles of our blog articles. For instance, the last article contains the acronym “CSS.” We can provide context for our readers about these acronyms using the <abbr> HTML element. Take a look at the `<h2>` elements in index.html. Provide context for all abbreviations you see in article titles.



The Unseen World
9.
Our blog looks amazing now! We have spent a lot of time focusing on these visual elements, and it shows.

There are, however, other parts of accessibility that are unseen. These are the aspects of accessibility that deal with assistive technologies such as screen readers. After all, we want to provide an amazing experience for whoever comes to our site.

One area that we can improve this unseen accessibility is with the search icon in our navigation bar. The search icon doesn’t provide any additional context for our assisted users using screen readers.

Let’s hide this icon from screen readers. In index.html, find the <span> element with class search-icon. Using an ARIA attribute, hide the <span> element from screen readers.



10.
The screen readers are thanking us already!

We should also make sure that screen readers aren’t seeing elements that are meant to be hidden from all users. If we don’t hide elements properly, it is possible for screen readers to still be able to read some visually hidden elements.

One of the links in the navigation bar, “For You”, is actually not supposed to be shown currently. Let’s hide this element from visual users and screen readers alike. Inside the .premium selector ruleset, add styles to hide the element.



# Navigability
11.
One of the last big accessibility hurdles we have to overcome now is navigability.

We want our users to navigate our blog easily, both with a mouse and alternative methods such as a keyboard or assistive technology. One way we can ensure this is by matching styles to the underlying structure of the HTML elements.

Something has gone awry in our blog—elements of the spotlight-list class are being displayed in the opposite order that they are in the HTML document. This will result in an incongruent navigation experience for users without a mouse.

Let’s correct this by reversing the order of the elements of the spotlight-list class to accurately reflect the HTML document. Make sure to make you change the order for the .spotlight-list selector in media queries as well.

12.
We have been laser-focused on the consumption of our blog on screens, but now it’s time to consider other mediums such as print.

Sometimes a user will want to print one of our blog pages. We should preserve as much of the functionality of our blog as possible for them when this happens.

One way we can do this is to ensure that information such as URLs stored as href attribute values are exposed on the printed pages. We can do this using an @media print query and targeting <a> tags.
