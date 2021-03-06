**Rationale**

Tweak your configuration so that you can jump from a commit message to your issue tracker. I will show the configuration for jumping to Mingle.

All our teams follow a convention of prefixing each commit message with a reference to the Mingle issue. Because of this convention, we can configure RubyMine to jump directly to the issue.

**Mechanism**

_Preferences > Version Control > Issue Navigation_ and _Add_ (using the '+' button)

In the Add Issue Navigation Link dialog specify the Issue ID regular expression and the replacement text. You can test out your regular expression by entering a sample Issue ID.

![Add Issue Navigation Link](https://github.com/amckinnell/RubyMineTips/blob/master/images/jump-to-issue-tracker.png)

The settings that do the trick where I work are:

Setting    | Value
:------    | :----
Issue ID   | ^#(\d+)[ :-].*
Issue link | http://mingle.hq.nulogy.com/projects/packmanager/cards/$1 

If you are successful you should see links when you show the commit history for a file.

![Jump from Git History](https://github.com/amckinnell/RubyMineTips/blob/master/images/jump-to-issue-tracker-from-git-history.png)


