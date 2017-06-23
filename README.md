https://stackoverflow.com/questions/21692880/uiscrollview-with-sticky-footer-uiview-and-dynamic-height-content

# UIScrollView with sticky footer UIView and dynamic height content

Challenge time!

Imagine we have 2 content views:

UIView with dynamically height content (expandable UITextView) = RED
UIView as a footer = BLUE
This content is inside a UIScrollView = GEEN

How should I structure and handle the constraints with auto-layout to archive all the following cases?

I am thinking next basic structure to start with:

- UIScrollView (with always bounce vertically)
    - UIView - Container
       - UIView - DynamicHeightContent
       - UIView - Sticky Footer
Keyboard handling should be done by code watching notifications UIKeyboardWillShowNotification and UIKeyboardWillHideNotification. We can chose to set the keyboard's end frame height to Container UIView bottom pin constraint or to the UIScrollView bottom contentInset.

Now, the tricky part is the sticky footer.

How we make sure the sticky footer UIView stays at the bottom if there is more screen available than the whole Container View?
How do we know the available screen space when the keyboard is shown/hidden? we'll surely need it.
Is is it right this structure I purpose?
Thank you.

Case recreation
