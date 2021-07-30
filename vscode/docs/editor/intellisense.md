IntelliSense
============

IntelliSense is a general term for various code editing features including: code completion, parameter info, quick info, and member lists. IntelliSense features are sometimes called by other names such as “code completion”, “content assist”, and “code hinting.”

![IntelliSense demo](images/intellisense/intellisense.gif)

IntelliSense for your programming language
------------------------------------------

Visual Studio Code IntelliSense is provided for JavaScript, TypeScript, JSON, HTML, CSS, SCSS, and Less out of the box. VS Code supports word based completions for any programming language but can also be configured to have richer IntelliSense by installing a language extension.

Below are the most popular language extensions in the [Marketplace](https://marketplace.visualstudio.com/vscode). Select an extension tile below to read the description and reviews to decide which extension is best for you.

IntelliSense features
---------------------

VS Code IntelliSense features are powered by a language service. A language service provides intelligent code completions based on language semantics and an analysis of your source code. If a language service knows possible completions, the IntelliSense suggestions will pop up as you type. If you continue typing characters, the list of members (variables, methods, etc.) is filtered to only include members containing your typed characters. Pressing `kbstyle(Tab)` or `kbstyle(Enter)` will insert the selected member.

You can trigger IntelliSense in any editor window by typing `kb(editor.action.triggerSuggest)` or by typing a trigger character (such as the dot character (`kbstyle(.)`) in JavaScript).

![intellisense in package json](images/intellisense/intellisense_packagejson.gif)

> **Tip:** The suggestions widget supports CamelCase filtering, meaning you can type the letters which are upper cased in a method name to limit the suggestions. For example, “cra” will quickly bring up “createApplication”.

If you prefer, you can turn off IntelliSense while you type. See [Customizing IntelliSense](/docs/editor/intellisense.md#customizing-intellisense) below to learn how to disable or customize VS Code’s IntelliSense features.

As provided by the language service, you can see **quick info** for each method by either pressing `kb(toggleSuggestionDetails)` or clicking the info icon. The accompanying documentation for the method will now expand to the side. The expanded documentation will stay so and will update as you navigate the list. You can close this by pressing `kb(toggleSuggestionDetails)` again or by clicking on the close icon.

![quick info](images/intellisense/intellisense_docs.gif)

After choosing a method you are provided with **parameter info**.

![parameter info](images/intellisense/paramater_info.png)

When applicable, a language service will surface the underlying types in the quick info and method signatures. In the image above, you can see several `any` types. Because JavaScript is dynamic and doesn’t need or enforce types, `any` suggests that the variable can be of any type.

Types of completions
--------------------

The JavaScript code below illustrates IntelliSense completions. IntelliSense gives both inferred proposals and the global identifiers of the project. The inferred symbols are presented first, followed by the global identifiers (shown by the Word icon).

![intellisense icons](images/intellisense/intellisense_icons.png)

VS Code IntelliSense offers different types of completions, including language server suggestions, snippets, and simple word based textual completions.

<table style="width:99%;"><colgroup><col style="width: 28%" /><col style="width: 41%" /><col style="width: 28%" /></colgroup><tbody><tr class="odd"><td><img src="images/intellisense/Method_16x.svg" alt="method icon" /></td><td>Methods and Functions</td><td><code>method</code>, <code>function</code>, <code>constructor</code></td></tr><tr class="even"><td><img src="images/intellisense/Variable_16x.svg" alt="variable icon" /></td><td>Variables</td><td><code>variable</code></td></tr><tr class="odd"><td><img src="images/intellisense/Field_16x.svg" alt="field icon" /></td><td>Fields</td><td><code>field</code></td></tr><tr class="even"><td><img src="images/intellisense/symbol-parameter.svg" alt="type parameter" /></td><td>Type parameters</td><td><code>typeParameter</code></td></tr><tr class="odd"><td><img src="images/intellisense/symbol-constant.svg" alt="constant" /></td><td>Constants</td><td><code>constant</code></td></tr><tr class="even"><td><img src="images/intellisense/Class_16x.svg" alt="class" /></td><td>Classes</td><td><code>class</code></td></tr><tr class="odd"><td><img src="images/intellisense/Interface_16x.svg" alt="interface" /></td><td>Interfaces</td><td><code>interface</code></td></tr><tr class="even"><td><img src="images/intellisense/symbol-structure.svg" alt="structure" /></td><td>Structures</td><td><code>struct</code></td></tr><tr class="odd"><td><img src="images/intellisense/symbol-event.svg" alt="event" /></td><td>Events</td><td><code>event</code></td></tr><tr class="even"><td><img src="images/intellisense/symbol-operator.svg" alt="operator" /></td><td>Operators</td><td><code>operator</code></td></tr><tr class="odd"><td><img src="images/intellisense/Namespace_16x.svg" alt="module" /></td><td>Modules</td><td><code>module</code></td></tr><tr class="even"><td><img src="images/intellisense/Property_16x.svg" alt="property" /></td><td>Properties and Attributes</td><td><code>property</code></td></tr><tr class="odd"><td><img src="images/intellisense/EnumItem_16x.svg" alt="enumeration icon" /></td><td>Values and Enumerations</td><td><code>value</code>, <code>enum</code></td></tr><tr class="even"><td><img src="images/intellisense/Reference_16x.svg" alt="reference" /></td><td>References</td><td><code>reference</code></td></tr><tr class="odd"><td><img src="images/intellisense/Keyword_16x.svg" alt="keyword" /></td><td>Keywords</td><td><code>keyword</code></td></tr><tr class="even"><td><img src="images/intellisense/symbol-file.svg" alt="file" /></td><td>Files</td><td><code>file</code></td></tr><tr class="odd"><td><img src="images/intellisense/folder.svg" alt="folder" /></td><td>Folders</td><td><code>folder</code></td></tr><tr class="even"><td><img src="images/intellisense/ColorPalette_16x.svg" alt="color" /></td><td>Colors</td><td><code>color</code></td></tr><tr class="odd"><td><img src="images/intellisense/Ruler_16x.svg" alt="unit" /></td><td>Unit</td><td><code>unit</code></td></tr><tr class="even"><td><img src="images/intellisense/Snippet_16x.svg" alt="a square with ellipses forming the bottom show snippet prefix" /></td><td>Snippet prefixes</td><td><code>snippet</code></td></tr><tr class="odd"><td><img src="images/intellisense/String_16x.svg" alt="a square with letters abc word completion" /></td><td>Words</td><td><code>text</code></td></tr></tbody></table>

Customizing IntelliSense
------------------------

You can customize your IntelliSense experience in settings and key bindings.

### Settings

The settings shown below are the default settings. You can change these settings in your `settings.json` file as described in [User and Workspace Settings](/docs/getstarted/settings.md).

    {
        // Controls if quick suggestions should show up while typing
        "editor.quickSuggestions": {
            "other": true,
            "comments": false,
            "strings": false
        },

         // Controls whether suggestions should be accepted on commit characters. For example, in JavaScript, the semi-colon (`;`) can be a commit character that accepts a suggestion and types that character.
        "editor.acceptSuggestionOnCommitCharacter": true,

        // Controls if suggestions should be accepted on 'Enter' - in addition to 'Tab'. Helps to avoid ambiguity between inserting new lines or accepting suggestions. The value 'smart' means only accept a suggestion with Enter when it makes a textual change
        "editor.acceptSuggestionOnEnter": "on",

        // Controls the delay in ms after which quick suggestions will show up.
        "editor.quickSuggestionsDelay": 10,

        // Controls if suggestions should automatically show up when typing trigger characters
        "editor.suggestOnTriggerCharacters": true,

        // Controls if pressing tab inserts the best suggestion and if tab cycles through other suggestions
        "editor.tabCompletion": "off",

        // Controls whether sorting favours words that appear close to the cursor
        "editor.suggest.localityBonus": true,

        // Controls how suggestions are pre-selected when showing the suggest list
        "editor.suggestSelection": "recentlyUsed",

        // Enable word based suggestions
        "editor.wordBasedSuggestions": true,

        // Enable parameter hints
        "editor.parameterHints.enabled": true,
    }

### Tab Completion

The editor supports “tab completion” which inserts the best matching completion when pressing `kb(insertBestCompletion)`. This works regardless of the suggest widget showing or not. Also, pressing `kb(insertNextSuggestion)` after inserting a suggestions will insert the next best suggestion.

![Tab Completion](images/intellisense/tabCompletion.gif)

By default, tab completion is disabled. Use the `editor.tabCompletion` setting to enable it. These values exist:

-   `off` - (default) Tab completion is disabled.
-   `on` - Tab completion is enabled for all suggestions and repeated invocations insert the next best suggestion.
-   `onlySnippets` - Tab completion only inserts static snippets which prefix match the current line prefix.

### Locality Bonus

Sorting of suggestions depends on extension information and on how well they match the current word you are typing. In addition, you can ask the editor to boost suggestions that appear closer to the cursor position, using the `editor.suggest.localityBonus` setting.

![Sorted By Locality](images/intellisense/localitybonus.png)

In above images you can see that `count`, `context`, and `colocated` are sorted based on the scopes in which they appear (loop, function, file).

### Suggestion selection

By default, VS Code pre-selects the previously used suggestion in the suggestion list. This is very useful as you can quickly insert the same completion multiple times. If you’d like different behavior, for example, always select the top item in the suggestion list, you can use the `editor.suggestSelection` setting.

The available `editor.suggestSelection` values are:

-   `first` - Always select the top list item.
-   `recentlyUsed` - (default) The previously used item is selected unless a prefix (type to select) selects a different item.
-   `recentlyUsedByPrefix` - Select items based on previous prefixes that have completed those suggestions.

“Type to select” means that the current prefix (roughly the text left of the cursor) is used to filter and sort suggestions. When this happens and when its result differs from the result of `recentlyUsed` it will be given precedence.

When using the last option, `recentlyUsedByPrefix`, VS Code remembers which item was selected for a specific prefix (partial text). For example, if you typed `co` and then selected `console`, the next time you typed `co`, the suggestion `console` would be pre-selected. This lets you quickly map various prefixes to different suggestions, for example `co` -&gt; `console` and `con` -&gt; `const`.

### Snippets in suggestions

By default, VS Code shows snippets and completion proposals in one widget. You can control the behavior with the `editor.snippetSuggestions` setting. To remove snippets from the suggestions widget, set the value to `"none"`. If you’d like to see snippets, you can specify the order relative to suggestions; at the top (`"top"`), at the bottom (`"bottom"`), or inline ordered alphabetically (`"inline"`). The default is `"inline"`.

### Key bindings

The key bindings shown below are the default key bindings. You can change these in your `keybindings.json` file as described in [Key Bindings](/docs/getstarted/keybindings.md).

> **Note:** There are many more key bindings relating to IntelliSense. Open the **Default Keyboard Shortcuts** (**File** &gt; **Preferences** &gt; **Keyboard Shortcuts**) and search for “suggest”.

    [
        {
            "key": "ctrl+space",
            "command": "editor.action.triggerSuggest",
            "when": "editorHasCompletionItemProvider && editorTextFocus && !editorReadonly"
        },
        {
            "key": "ctrl+space",
            "command": "toggleSuggestionDetails",
            "when": "editorTextFocus && suggestWidgetVisible"
        },
        {
            "key": "ctrl+alt+space",
            "command": "toggleSuggestionFocus",
            "when": "editorTextFocus && suggestWidgetVisible"
        }
    ]

Troubleshooting
---------------

If you find IntelliSense has stopped working, the language service may not be running. Try restarting VS Code and this should solve the issue. If you are still missing IntelliSense features after installing a language extension, open an issue in the repository of the language extension.

> **Tip:** For configuring and troubleshooting JavaScript IntelliSense, see the [JavaScript documentation](/docs/languages/javascript.md#intellisense).

A particular language extension may not support all the VS Code IntelliSense features. Review the extension’s README to find out what is supported. If you think there are issues with a language extension, you can usually find the issue repository for an extension through the [VS Code Marketplace](https://marketplace.visualstudio.com/vscode). Navigate to the extension’s Details page and select the **Support** link.

Next steps
----------

IntelliSense is just one of VS Code’s powerful features. Read on to learn more:

-   [JavaScript](/docs/languages/javascript.md) - Get the most out of your JavaScript development, including configuring IntelliSense.
-   [Node.js](/docs/nodejs/nodejs-tutorial.md) - See an example of IntelliSense in action in the Node.js walkthrough.
-   [Debugging](/docs/editor/debugging.md) - Learn how to set up debugging for your application.
-   [Creating Language extensions](/api/language-extensions/programmatic-language-features.md) - Learn how to create extensions that add IntelliSense for new programming languages.

Common questions
----------------

### Why am I not getting any suggestions?

![image of IntelliSense not working](images/intellisense/intellisense_error.png)

This can be caused by a variety of reasons. First, try restarting VS Code. If the problem persists, consult the language extension’s documentation. For JavaScript specific troubleshooting, please see the [JavaScript language topic](/docs/languages/javascript.md#intellisense).

### Why am I not seeing method and variable suggestions?

![image of IntelliSense showing no useful suggestions](images/intellisense/missing_typings.png)

This issue is caused by missing type declaration (typings) files in JavaScript. You can check if a type declaration file package is available for a specific library by using the [TypeSearch](https://microsoft.github.io/TypeSearch) site. There is more information about this issue in the [JavaScript language topic](/docs/languages/javascript.md#intellisense). For other languages, please consult the extension’s documentation.