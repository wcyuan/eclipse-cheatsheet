### Table of Contents

*   [Setup](#setup)
*   [Navigating Shortcuts](#navigating)
*   [Editing Shortcuts](#editing)
*   [Icons](#icons)

* * *

<a name="setup"></a>

### Setup

*   Attach JDK instead of JRE to browse the source for core java. Go to Windows, Preferences, Java, Installed JREs and add the JDK directory instead of the JRE directory.
*   If you just have a jar or jre with no source, you can attach the source (go to Installed JREs, click edit, select the jar and click Source Attachment)
*   To attach the source for an Android app, see [here](http://code.google.com/p/adt-addons/)
*   Package Explorer - Click on the down arrow to bring up a menu, then go to Package Presentation, Hierarchical (instead of flat). Also, link it to the editor. Now you can press the minus sign to collapse everything, then click back in the editor to only see the path to the file you are editing.
*   Turn on line numbers - Window, Preferences, General, Editors, Text Editors, check Show Line Numbers
*   Whatever version control you use, you can access the commands from the Team submenu in the menu that you get when you right-click on a file.
*   If you use SVN, probably use the Subclipse plug-in, not the Subversive plug-in. Subclipse has much closer ties to Subversion itself. Subversive might have somewhat closer ties to Eclipse, for whatever it's worth. Not totally clear which is better, but [this](http://stackoverflow.com/questions/61320/svn-plugins-for-eclipse-subclipse-vs-subversive) makes Subclipse sound a bit better. For my purposes, probably either is fine. (If it's up to me, I prefer git anyway)

*   I found, by default, that SVN annotate shows up with revision numbers in a separate window. It's better to change it to "Quick Diff" mode where it highlights the side of the editor window. To turn that on, go to Preferences->Team->SVN and choose "Yes" under "Use Quick Diff annotate mode for local file annotations.

* * *

<a name="navigating"></a>

### Navigating

| Command | Key | Description |
| ------- | --- | ----------- |
| Open a file (Open Resource) | `Ctrl-Shift-R` | Find a file by pattern matching on file name |
| Open a class (Open Type) | `Ctrl-Shift-T` | Find a file by pattern matching on class name |
| Jump to definition | `F3` or `Ctrl-Click` | Highlight the word (variable name, method name, class name, etc) and press F3 to see where it is defined. Or, hold down Control while clicking on the word. If you hover over a variable while holding down Control, a little menu appears where you can go to a declaration or open a list of implementations. The Control-hover menu only appears with variable names or methods, not Class names. |
| Show Type Hierarchy | `Ctrl-T` or `F4` | Control-T shows a popup with the possible implementations of the highlighted type. Click on one to go to its code. F4 shows the same thing, but in a window on the left. |
| Find Method | `Ctrl-O` | Find a method of the current class by name. |
| Jump back to the point you last jumped to | `Alt-Left` | For example, if you've pressed F3 to find the definition of a method, you can use this to go back to the method call you had been looking at before you jumped to the definition. Works a little like the back button on a browser, except that in a browser the back button goes to the previous page while this could jump to a different point in the same file. `Alt-Right` goes forward. |
| Jump back to the point you last edited | `Ctrl-Q` |
| List uses (call hierarchy) | `Ctrl-Alt-H` | Searches all the files in the workspace for a given variable/class/etc. Shows up in the window below. |
| Scroll window without moving the cursor | `Ctrl-Up/Down` |
| Move to the next member | `Ctrl-Shift-Up/Down` |
| Select enclosing block | `Alt-Shift-Up/Down` |
| Find matching paren | `Ctrl-Shift-P` |
| See list of shortcuts | `Ctrl-Shift-L` |
| Highlight all occurrences of the selected text | `Shift-Alt-O`, or <br> **Java -> Editor -> Mark Occurrences**, or <br> `Ctrl-Shift-U` | This only works for Java, and only for certain types of strings (variable names, class names, etc), not arbitrary strings. Using control-shift-u will show a list of the matches in the search box below the editor. When occurrences are highlighted, you can see them both in the editor's text, and also as marks to the right of to the scroll bar. If you right-click on the marks next to the scroll bar, you open `Preferences` to set the color used to highlight text. Write occurrences have a different color than other occurrences. |
| Text search | `Ctrl-F` (brings up a dialog) | Searches all the files in the workspace for a given variable/class/etc. Shows up in the window below. |
| Incremental search | `Ctrl-J` (see lower right side of status bar) | Searches for text in the current file, as you type. The string you are searching for shows up in the window below. Unfortunately, this does not highlight all matches. |
| Jump to next occurrence of highlighted string | `Ctrl-K` | Sort of similar to `Ctrl-J`. It searches for the next time the highlight string appears in the file. This is a text search, not a java-syntax-aware search |
| Import existing java code into Eclipse | **File -> Import -> General -> File System** then browse to your checkout | Searches all the files in the workspace for a given variable/class/etc. Shows up in the window below. |
| Insert a breakpoint | Double-click in the editor to the left of the line of code. | Double-click again to remove the breakpoint |

* * *

<a name="editing"></a>

### Editing

| Command | Key | Description |
| ------- | --- | ----------- |
| Side-by-side editors | Click on an editor tab and drag it to the side or the top or bottom. As you drag, you'll see the outline of two windows, either side-by-side or top or bottom. That's how you put two editors side-by-side. If you want the same file on both sides, first go to Window, New Editor to create two editors with the same file. Then drag one tab to split the screen. <br> If you want to go back to one screen, you have to drag everything from one side back to the other, or you have to close everything on one side. Dragging editors is not very smooth, somehow it doesn't always work well. Also, when you open a new window, it will go on the left side by default. <br> So my typical usage is that I have one file that I want to have open, and while that is open I want to visit a bunch of other places at the same time. So I'll put that file on the right side by itself, and I'll put everything else on the left side (where new windows will appear). That way, when I want to go back to one screen, I only have one editor to move or close. |
| "Smart" word completion | `Ctrl-Space` | Based on available java methods. |
| "Dumb" word completion | `Alt-/` | Based on other words in the current file. |
| Insert line | `Shift-Enter` and `Ctrl-Shift-Enter` | Insert line below or above |
| Comment out and in | `Ctrl-/` and `Ctrl-\` |
| Move row (or selection) | `Alt-Up/Down` |
| Duplicate a row | `Ctrl-Alt-Up/Down` |
| Organize imports | `Ctrl-Shift-O` |
| Delete row | `Ctrl-D` |
| Quick fix | `Ctrl-1` | Presents some options for automatic refactoring |
| Fix indentation | `Ctrl-I` |
| Auto-format | `Ctrl-Shift-F` | May need to configure this in **Window->Preferences->Java->Code style->Formatter** |
| Generate getters and setters | **Source-&gt;Generate Getters and Setters** |

* * *

<a name="icons"></a>

### Icons

[List of icons (for Juno).](http://help.eclipse.org/juno/index.jsp?topic=/org.eclipse.jdt.doc.user/reference/ref-icons.htm)

*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/class_obj.png) Class
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/int_obj.png) Interface
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/enum_obj.png) Enum
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/field_default_obj.png) Default field
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/field_private_obj.png) Private field
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/field_protected_obj.png) Protected field
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/field_public_obj.png) Public field
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/methdef_obj.png) Default method
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/methpri_obj.png) Private method
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/methpro_obj.png) Protected method
*   ![](http://help.eclipse.org/juno/topic/org.eclipse.jdt.doc.user/images/org.eclipse.jdt.ui/obj16/methpub_obj.png) Public method

[List of icons (for Subclipse).](http://stackoverflow.com/questions/3917925/what-do-the-arrow-icons-in-subclipse-mean/3920248#3920248)
