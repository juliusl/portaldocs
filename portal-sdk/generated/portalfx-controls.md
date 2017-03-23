* [Controls](#controls)
    * [Date and Time](#controls-date-and-time)
    * [Drop downs](#controls-drop-downs)
        * [Migrating from older dropdown controls](#controls-drop-downs-migrating-from-older-dropdown-controls)
    * [Editors](#controls-editors)
        * [Editor](#controls-editors-editor)
    * [Console](#controls-console)
    * [Forms](#controls-forms)
    * [Lists](#controls-lists)
    * [Grid](#controls-grid)
        * [Getting Started](#controls-grid-getting-started)
        * [Plugins](#controls-grid-plugins)
        * [Providing Data](#controls-grid-providing-data)
        * [Defining Columns](#controls-grid-defining-columns)
        * [Formatting](#controls-grid-formatting)
        * [Formatting Dates](#controls-grid-formatting-dates)
        * [Formatting Numbers](#controls-grid-formatting-numbers)
        * [Formatting Images](#controls-grid-formatting-images)
        * [Formatting Uris](#controls-grid-formatting-uris)
        * [Formatting Html](#controls-grid-formatting-html)
        * [Custom Formatting (HtmlBindings)](#controls-grid-custom-formatting-htmlbindings)
        * [Selection and Activation](#controls-grid-selection-and-activation)
        * [Sorting](#controls-grid-sorting)
        * [Filtering](#controls-grid-filtering)
        * [Editing](#controls-grid-editing)
        * [Paging](#controls-grid-paging)
        * [Grouping](#controls-grid-grouping)
        * [Hierarchical](#controls-grid-hierarchical)
        * [Context Menus](#controls-grid-context-menus)
        * [Scrolling](#controls-grid-scrolling)
        * [Reordering](#controls-grid-reordering)
        * [Dynamic Grid Definitiona](#controls-grid-dynamic-grid-definitiona)
        * [Further Resources](#controls-grid-further-resources)
    * [Helpers and Indicators](#controls-helpers-and-indicators)
    * [Visualizing Data](#controls-visualizing-data)
        * [Chart views and series views](#controls-visualizing-data-chart-views-and-series-views)
        * [Metrics](#controls-visualizing-data-metrics)
        * [Metrics rules](#controls-visualizing-data-metrics-rules)
    * [Donut chart](#controls-donut-chart)


<a name="controls"></a>
# Controls

Controls are the building blocks of your experience. They allow users to view, edit, and analyze data.

To learn more about any of our controls, click on any of the links below.

- [Button](http://aka.ms/portalfx/samples#blade/SamplesExtension/SimpleButtonInstructions/selectedItem/SimpleButtonInstructions/selectedValue/SimpleButtonInstructions)
- [Copyable Label](http://aka.ms/portalfx/samples#blade/SamplesExtension/CopyableLabelInstructions/selectedItem/CopyableLabelInstructions/selectedValue/CopyableLabelInstructions)
- [File Upload (async)](http://aka.ms/portalfx/samples#blade/SamplesExtension/AsyncFileUploadInstructions/selectedItem/AsyncFileUploadInstructions/selectedValue/AsyncFileUploadInstructions)
- [File Download Button](http://aka.ms/portalfx/samples#blade/SamplesExtension/FileDownloadButtonInstructions/selectedItem/FileDownloadButtonInstructions/selectedValue/FileDownloadButtonInstructions)
- [Text Block](https://df.onecloud.azure-test.net/?samplesExtension=true#blade/SamplesExtension/TextBlockInstructions/selectedItem/TextBlockInstructions/selectedValue/TextBlockInstructions)
- [OAuth Button](http://aka.ms/portalfx/samples#blade/SamplesExtension/OAuthButtonInstructions/selectedItem/OAuthButtonInstructions/selectedValue/OAuthButtonInstructions)
- [Splitter](http://aka.ms/portalfx/samples#blade/SamplesExtension/SplitterInstructions/selectedItem/SplitterInstructions/selectedValue/SplitterInstructions)
- [Selector](http://aka.ms/portalfx/samples#blade/SamplesExtension/SelectorInstructions/selectedItem/SelectorInstructions/selectedValue/SelectorInstructions)
- [Settings](http://aka.ms/portalfx/samples#blade/SamplesExtension/SettingsInstructions/selectedItem/SettingsInstructions/selectedValue/SettingsInstructions)
- [Single Setting](http://aka.ms/portalfx/samples#blade/SamplesExtension/SingleSettingInstructions/selectedItem/SingleSettingInstructions/selectedValue/SingleSettingInstructions)
- [Toolbar](http://aka.ms/portalfx/samples#blade/SamplesExtension/ToolbarInstructions/selectedItem/ToolbarInstructions/selectedValue/ToolbarInstructions)
- [Markdown Control](http://aka.ms/portalfx/samples#blade/SamplesExtension/MarkdownInstructions/selectedItem/MarkdownInstructions/selectedValue/MarkdownInstructions)


<a name="controls-date-and-time"></a>
## Date and Time

- [Date Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/DatePickerInstructions/selectedItem/DatePickerInstructions/selectedValue/DatePickerInstructions)
- [Date/Time Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/DateTimePickerInstructions/selectedItem/DateTimePickerInstructions/selectedValue/DateTimePickerInstructions)
- [Date/Time Range Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/DateTimeRangePickerInstructions/selectedItem/DateTimeRangePickerInstructions/selectedValue/DateTimeRangePickerInstructions)
- [Date Polyfills](http://aka.ms/portalfx/samples#blade/SamplesExtension/DatePolyFillsInstructions/selectedItem/DatePolyFillsInstructions/selectedValue/DatePolyFillsInstructions)
- [Day Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/DayPickerInstructions/selectedItem/DayPickerInstructions/selectedValue/DayPickerInstructions)
- [Duration Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/DurationPickerInstructions/selectedItem/DurationPickerInstructions/selectedValue/DurationPickerInstructions)
- [Time Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/TimePickerInstructions/selectedItem/TimePickerInstructions/selectedValue/TimePickerInstructions)

<a name="controls-drop-downs"></a>
## Drop downs
- Drop Down
	## DropDown
We've had several version of the dropdown control but have asked partners to standardize on the AMD dropdown control.
You can use it by importing the AMD module:

```
import * as DropDown from "Fx/Controls/DropDown";
```

creating the view model:

```
var dropDown = new DropDown.ViewModel(ltm, {...});
```

and then inserting it into a section or your HTML template via the pcControl binding. You can see it running
in samples extension [here](http://aka.ms/portalfx/samples#blade/SamplesExtension/DropDownInstructions/selectedItem/DropDownInstructions/selectedValue/DropDown).

<a name="controls-drop-downs-migrating-from-older-dropdown-controls"></a>
### Migrating from older dropdown controls
The biggest reason to replace usage of the older dropdown controls with the AMD dropdown is that all the features
of the other dropdowns are now present in the AMD dropdown. You can now turn on filtering or add grouping to a 
multiselect dropdown where previously adding a featuring might mean porting your code to a differen control (or 
wasn't possible depending on combination of features you were looking for). The AMD dropdown supports:

- Grouping
- Rich Templating
- Filtering 
- Custom Filtering, this also gives you a hook to replace items on keystroke.
- Multiselect
- Objects as the value

<a name="controls-editors"></a>
## Editors

- Code editor
       
<a name="controls-editors-editor"></a>
### Editor

Editor control in the FX SDK is a wrapper for the "Monaco" editor which supports various languages, syntax highligting, intellisense, real-time syntax checking and validation.

![Editor][editor-code]

<a name="controls-editors-editor-editor-basics"></a>
#### Editor Basics

To use the editor, compose a part that hosts the editor control, then use it from your extension.

You can control the behavior and features of the editor via initialization `options`.

**Step 1**: Define the Html template for your part:

`\Client\V1\Controls\Editor\Templates\EditorInstructions.html`

**Step 2**: Create a viewmodel to bind your control to. SampleEditorViewModel implements the viewmodel for the editor.

`\Client\V1\Controls\Editor\ViewModels\EditorViewModels.ts.`

```typescript

/**
* ViewModel class for the editor sample.
*/
export class SampleEditorViewModel extends MsPortalFx.ViewModels.Controls.Documents.Editor.ViewModel {
   /**
    * Editor view model constructor.
    */
   constructor(lifetimeManager: MsPortalFx.Base.LifetimeManager) {
       // Mock up sample javascript file content.
       var content =
           [
               "function test1(name, job) {",
               "    alert('Welcome ' + name + ', the ' + job);",
               "}",
               "",
               "function test2() {",
               "    var x = '', i = 0;",
               "    for (i = 0; i < 10; i++) {",
               "        if (i == 3) {",
               "            continue;",
               "        }",
               "        x = x + 'The number is ' + i;",
               "    }",
               "    document.getElementById('demo').innerHTML = x;",
               "}"
           ].join("\n");

       // Set up whether or not to show line numbers and what the tab size is in the editor.
       var options = {
               lineNumbers: false,
               tabSize: 4,
               wrappingColumn: 0
           };

       // Initialize the editor with the above content and options, as well as set the type to be JavaScript.
       super(lifetimeManager, MsPortalFx.ViewModels.Controls.Documents.Editor.ContentType.JavaScript, content, options);
   }
}

/**
* ViewModel class for the editor sample part.
*/
export class EditorInstructionsPartViewModel
   implements Def.EditorInstructionsPartViewModel.Contract {

   /**
    * View model for the editor.
    */
   public editorVM: MsPortalFx.ViewModels.Controls.Documents.Editor.Contract;

   /**
    * View model for the save button.
    */
   public saveButton: MsPortalFx.ViewModels.Controls.Forms.Button.Contract;

   /**
    * Creates a new instance of the EditorInstructionsPartViewModel class.
    *
    * @param container The view model for the part container.
    * @param initialState The initial state for the part.
    * @param dataContext The data context.
    */
   constructor(
       container: MsPortalFx.ViewModels.PartContainerContract,
       initialState: any,
       dataContext: ControlsArea.DataContext) {

       // Initialize the editor view model.  If we were getting the data from teh data context, we would pass it in here.
       this.editorVM = new SampleEditorViewModel(container);

       // Initialize the save button and wire it up such that it saves the content of the editor.
       this.saveButton = new MsPortalFx.ViewModels.Controls.Forms.Button.ViewModel(container);
       this.saveButton.click = () => {
           this.editorVM.save.execute().then(() => {
               // Here is where you would put code that is executed after any changes have been written back to the content property on the viewmodel.
           });
       };
   }
}

```

**Step 3**: Now you can consume your part from an extension by referencing it in the PDL:

`\Client\V1\Controls\Editor\Editor.pdl`

```xml

<CustomPart Name="b_EditorInstructions_part1"
            ViewModel="{ViewModel Name=EditorInstructionsPartViewModel, Module=./Editor/ViewModels/EditorViewModels}"
            InitialSize="FullWidthFitHeight"
            Template="{Html Source='Templates\\EditorInstructions.html'}" />
<PartReference Name="EditorApiReferencePart"
               InitialSize="FullWidthFitHeight"
               PartType="ModuleReferencePart">
  <PartReference.PropertyBindings>
    <Binding Property="moduleName"
             Source="{Constant MsPortalFx.ViewModels.Controls.Documents.Editor}" />
  </PartReference.PropertyBindings>
</PartReference>

```

[editor-code]: ../media/portalfx-controls/editor-code.png

<a name="controls-editors-editor-editor-with-custom-language"></a>
#### Editor with Custom Language

Custom language can be used by declaring inherited Editor control viewmodel with rules and suggestions.

**Step 1**: Define the Html template for your part:

`\Client\V1\Controls\Editor\Templates\CustomLanguageEditor.html`

**Step 2**: Create a viewmodel to bind your control to. SampleEditorViewModel implements the viewmodel for the editor.

`\Client\V1\Controls\Editor\ViewModels\CustomLanguageEditorViewModels.ts.`

/**
 * ViewModel class for the custom language editor sample part.
 */
export class CustomLanguageEditorPartViewModel {

    /**
     * View model for the editor.
     */
    public editor: Editor.ViewModel;

    /**
     * Creates a new instance of the EditorInstructionsPartViewModel class.
     *
     * @param container The view model for the part container.
     * @param initialState The initial state for the part.
     * @param dataContext The data context.
     */
    constructor(
        container: MsPortalFx.ViewModels.PartContainerContract,
        initialState: any,
        dataContext: ControlsArea.DataContext) {

        // Initialize the editor view model.  If we were getting the data from teh data context, we would pass it in here.
        this.editor = new CustomLanguageEditorViewModel(container);

        // create the initial markers
        this.updateMarkers(this.editor.content());

        // whenever the code in the editor changes process it and set the markers
        this.editor.content.subscribe(container, this.updateMarkers.bind(this));

        // perform auto save every 500ms to update markers as the user edits the text
        this.editor.autoSaveTimeout(500);
    }

    /**
     * try to match the given pattern in the provided line, if matched construct a marker for that line
     */
    private processTerm(line: string, lineIndex: number, termPattern: string, severity: MsPortalFx.ViewModels.Controls.Documents.Editor.MarkerSeverity): MsPortalFx.ViewModels.Controls.Documents.Editor.EditorMarker {

        // try to match the pattern
        var termIndex = line.indexOf(termPattern);
        if (termIndex === -1) {
            return null;
        }

        // we found the pattern in the line so we create a marker which uses the defined severity and the rest of the text
        // from the pattern location in the line to the end as the message
        return <MsPortalFx.ViewModels.Controls.Documents.Editor.EditorMarker> {
            message: line.substring(termIndex + termPattern.length),
            severity: severity,
            range: <MsPortalFx.ViewModels.Controls.Documents.Editor.EditorRange> {
                startLineNumber: lineIndex + 1,
                startColumn: termIndex + 1,
                endLineNumber: lineIndex + 1,
                endColumn: termIndex + termPattern.length + 1
            }
        };
    }

    /**
     * updates the markers according to the text content
     */
    private updateMarkers(value: string): void {

        // split the text into lines and process each to add an annotation to it
        var markers = value
            .split("\n")
            .map((line: string, index: number): MsPortalFx.ViewModels.Controls.Documents.Editor.EditorMarker => {

                var term = this.processTerm(line, index, "[error]", MsPortalFx.ViewModels.Controls.Documents.Editor.MarkerSeverity.Error);
                if (term !== null) {
                    return term;
                }

                term = this.processTerm(line, index, "[notice]", MsPortalFx.ViewModels.Controls.Documents.Editor.MarkerSeverity.Warning);
                if (term !== null) {
                    return term;
                }

                term = this.processTerm(line, index, "[info]", MsPortalFx.ViewModels.Controls.Documents.Editor.MarkerSeverity.Info);
                if (term !== null) {
                    return term;
                }

                return null;
            })
            .filter(marker => marker !== null);

        // update the markers
        this.editor.markers(markers);
    }
}

**Step 3**: Now you can consume your part from an extension by referencing it in the PDL:

`\Client\V1\Controls\Editor\Editor.pdl`

```xml
<CustomPart Name="b_EditorInstructions_part1"
                  ViewModel="{ViewModel Name=EditorInstructionsPartViewModel, Module=./Editor/ViewModels/EditorViewModels}"
                  InitialSize="FullWidthFitHeight"
                  Template="{Html Source='Templates\\EditorInstructions.html'}" />
<PartReference Name="EditorApiReferencePart"
                InitialSize="FullWidthFitHeight"
                PartType="ModuleReferencePart">
    <PartReference.PropertyBindings>
        <Binding Property="moduleName"
                Source="{Constant MsPortalFx.ViewModels.Controls.Documents.Editor}" />
    </PartReference.PropertyBindings>
</PartReference>
```

- [Diff editor](http://aka.ms/portalfx/samples#blade/SamplesExtension/DiffEditorInstructions/selectedItem/DiffEditorInstructions/selectedValue/DiffEditorInstructions)
- Console
      
<a name="controls-console"></a>
## Console
The console control provides a REPL like experience which can be used to replicate a Bash/PowerShell/Batch like experience.

![Console](../media/portalfx-controls/console-large.png)

`\SamplesExtension\Extension\Client\Controls\Console\Templates\ConsoleInstructions.html`

```html
<div data-bind='pcConsole: consoleViewModel'></div>
```

`\SamplesExtension\Extension\Client\Controls\Console\ViewModels\ConsoleViewModels.ts`

```ts
public consoleViewModel: MsPortalFx.ViewModels.Controls.Console.Contract;

constructor(container: MsPortalFx.ViewModels.PartContainerContract,
			initialState: any,
			dataContext: ControlsArea.DataContext) {

    // Initialize the console view model.
    this.consoleViewModel = new MsPortalFx.ViewModels.Controls.Console.ViewModel();

    // To get input from the user, subscribe to the command observable.
    // This is where you would parse the incomming command.
    // To show output, you can set the info, warning, success and error properties.
    this.consoleViewModel.command.subscribe(container, (s) => {
        // In this example, we are just piping back the input as an info, warning, success or error message based off of what you type in.
        switch (s) {
            case ClientResources.consoleInfo:
                this.consoleViewModel.info(s);
                break;
            case ClientResources.consoleWarning:
                this.consoleViewModel.warning(s);
                break;
            case ClientResources.consoleSuccess:
                this.consoleViewModel.success(s);
                break;
            case ClientResources.consoleError:
                this.consoleViewModel.error(s);
                break;
            default:
                this.consoleViewModel.error(s);
        }
    });

    // You can also observably set the prompt which is displayed above the > in the console.
    this.consoleViewModel.prompt = ko.observable(ClientResources.consolePrompt);
}
```


<a name="controls-forms"></a>
## Forms
- Check Box
  - [Standard Check Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/CheckBoxInstructions)
  - [Tri State Check Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/TriStateCheckBoxInstructions)
- [Custom HTML](http://aka.ms/portalfx/samples#blade/SamplesExtension/CustomFormFieldsBlade)

- Text Boxes
  - [MultiLine Text Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/MultiLineTextBoxInstructions/selectedItem/MultiLineTextBoxInstructions/selectedValue/MultiLineTextBoxInstructions)
  - [Numeric Text Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/NumericTextBoxInstructions/selectedItem/NumericTextBoxInstructions/selectedValue/NumericTextBoxInstructions)
  - [Text Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/TextBoxInstructions/selectedItem/TextBoxInstructions/selectedValue/TextBoxInstructions)
  
- [Option Picker](http://aka.ms/portalfx/samples#blade/SamplesExtension/OptionPickerInstructions/selectedItem/OptionPickerInstructions/selectedValue/OptionPickerInstructions)

- [Password Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/PasswordInstructions/selectedItem/PasswordInstructions/selectedValue/PasswordInstructions)

- [Search Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/SearchBoxBlade/selectedItem/SearchBoxBlade/selectedValue/SearchBoxBlade)

- Sliders
  - [Standard Slider](http://aka.ms/portalfx/samples#blade/SamplesExtension/SliderInstructions/selectedItem/SliderInstructions/selectedValue/SliderInstructions)
  - [Custom Value Slider](http://aka.ms/portalfx/samples#blade/SamplesExtension/SlidersInstructions/selectedItem/SlidersInstructions/selectedValue/SlidersInstructions)
  - [Range Slider](http://aka.ms/portalfx/samples#blade/SamplesExtension/RangeSliderInstructions/selectedItem/RangeSliderInstructions/selectedValue/RangeSliderInstructions)
  - [Custom Range Slider](http://aka.ms/portalfx/samples#blade/SamplesExtension/RangeSliderInstructions/selectedItem/CustomRangeSliderInstructions/selectedValue/CustomRangeSliderInstructions)

<a name="controls-lists"></a>
## Lists

- [Gallery](http://aka.ms/portalfx/samples#blade/SamplesExtension/GalleryInstructions/selectedItem/GalleryInstructions/selectedValue/GalleryInstructions)
- [List View](http://aka.ms/portalfx/samples#blade/SamplesExtension/ListViewInstructions/selectedItem/ListViewInstructions/selectedValue/ListViewInstructions)
- [Tree View](http://aka.ms/portalfx/samples#blade/SamplesExtension/TreeViewInstructions/selectedItem/TreeViewInstructions/selectedValue/TreeViewInstructions)
- [String List](http://aka.ms/portalfx/samples#blade/SamplesExtension/StringListInstructions/selectedItem/StringListInstructions/selectedValue/StringListInstructions)
- [Query Builder](http://aka.ms/portalfx/samples#blade/SamplesExtension/QueryBuilderInstructions/selectedItem/QueryBuilderInstructions/selectedValue/QueryBuilderInstructions)
- Grid
	﻿
<a name="controls-grid"></a>
## Grid

The grid control in SDK provides a rich set of features to build experiences that visualize tabular, structured data.

![Grid](../media/portalfx-controls/grid-intro.png)

From simple experiences that visualize basic lists to advanced scenarios such as virtualized hierarchical data; the grid control can be configured with different options such as multiple selection, custom formatters, grouping, filtering, sorting, paging and virtualization.

<a name="controls-grid-getting-started"></a>
### Getting Started
The Grid API is in the MsPortalFx.ViewModels.Controls.Lists.Grid namespace.
To create a grid you will need to provide data, column definitions, plugins, and options. Some of the basic implementations are provided [here](#basic-samples).

[Grid Samples][GridSamples]

<a name="controls-grid-plugins"></a>
### Plugins
There are many plugins for the grid control to add behaviors.
Grid plugins are called "extensions" in the API.
The "extension" terminology can be confusing to portal "extension" authors.
So, in this document the grid extensions will be referred to as plugins.

- [SelectableRow](#selection-and-activation) - Plugin to have selectable rows.
- [ResizableColumn]()                        - Plugin to have resizable columns.
- [SortableColumn](#sorting)                 - Plugin to have sortable columns.
- [Filterable](#filtering)                   - Plugin to have filterable rows.
- [ContextMenuShortcut](#context-menus)      - Plugin to have a shortcut to the item context menu displayed in the row.
- [Pageable](#paging)                        - Plugin to handle and display large items in sequential pages.
- [Scrollable](#scrolling)                   - Plugin to display items with virtual scrolling.
- [Groupable](#grouping)                     - Plugin to group rows by column value.
- [Hierarchical](#hierarchical)              - Plugin to display hierarchical items.
- [EditableRow](#editing)                    - Plugin to have editable rows.
- [ReorderRow](#reordering)                  - Plugin to have reorder rows.
- [RightClickableRow]()                      - Plugin to have right-clickable row.
- [Hoverable]()                              - Plugin to enable hover index communication with other parts.

Plugins are enabled in three ways.
- with bit flags passed to the ViewModel constructor.
- by default.
- as a dependency of an enabled plugin.

To enable a plugin you need to do two things.
First, you must set the appropriate bit flag when you construct the grid.
It is important that you combine the bit flags with the "|" or "+" operator. 
*A common pitfall is to use "&" which results in no plugins.*
Second, you must provide plugin options.

The following sample shows a simple method of enabling the plugins:

```typescript

// Define the grid plugins and options.
this.grid = new Grid.ViewModel<WorkItem, WorkItem>(
    container,
    null,
    Grid.Extensions.Scrollable | Grid.Extensions.Filterable | Grid.Extensions.SortableColumn,
    {
        scrollable: <Grid.ScrollableOptions<WorkItem>>{
            dataNavigator: this._navigator
        },
        filterable: <Grid.FilterableOptions>{
            // Server filter causes the grid to use the data navigator for filtering.
            serverFilter: ko.observable(true)
        },
        sortableColumn: <Grid.SortableColumnOptions<WorkItem>>{
        }
    });

```

Plugin compatibility:

![No-code Browse grid](../media/portalfx-controls/gridchart.png)

<a name="controls-grid-providing-data"></a>
### Providing Data
In the basic scenario your data is provided to the grid, throw the items param as a KnockoutObservableArray&lt;T>.
The array can be one you create or more commonly it will be the items property of a QueryView.

In virtualzation scenarios you will provide the data to the grid via a DataNavigator.
Navigators can support two data retrieval patterns.
- The first is sequential data access using continuation tokens.Sequential navigation can be enabled by the Pageable plugin.
- The second is using random data access aka skip-take. Random access navigation can be enabled by the Pageable or Scrollable plugins.

[Data Documentation](/portalfx-data.md)

<a name="controls-grid-defining-columns"></a>
### Defining Columns
Columns are defined by setting the columns property on the grid view model.
The header text of the column is declared with the name property.
Cell values for the column are determined by the itemKey property.
The itemKey specifies the name of the property on your data item.
For each data item the grid will use the itemKey to read the value.
There are many other column options that specify the formatting of the value or enable plugin specific behaviors.

```typescript

var columns: MsPortalFx.ViewModels.Controls.Lists.Grid.Column[] = [
    {
        itemKey: "name",
        name: ko.observable<string>(ClientResources.controlSampleName)
    },
    {
        itemKey: "ssnId",
        name: ko.observable<string>(ClientResources.controlSampleSsn)
    },
    {
        itemKey: "bills",
        name: ko.observable<string>(ClientResources.gridBasicGridBills)
    }
];
this.basicGridViewModel.columns = ko.observableArray<MsPortalFx.ViewModels.Controls.Lists.Grid.Column>(columns);

```

<a name="controls-grid-formatting"></a>
### Formatting
Columns are formatted using three key properties.
  - ``itemKey``: The property of your data item to display.  
  - ``format``: Optional format type from the Format enumeration. 
  - ``formatOptions``:  Optional formatter specific options.

By default values you specify with the column itemKey will be formated as text.
The text formatter does a simplistic toString conversion.
If you have an object or need more specific formatting for a date or number there are many built in formatters to use.

[Formatted Grid Sample][FormattedSample]

<a name="controls-grid-formatting-dates"></a>
### Formatting Dates
Dates are formatted using the Intl API using the current locale set by the user.
The data value of the date can be a number, string, or date.
The formatters will convert to date and then use the Intl API to convert to text.
The following formatters can be used for formatting dates:
- ShortDate: 7/18/2013
- LongDate: Thursday, July 18, 2013 
- MonthDay: July 18
- YearMonth: July, 2013
- ShortTime: 11:20 AM
- LongTime: 11:20:19 AM
- CustomDate: Any format posible using Intl date formatting

```typescript

{
    itemKey: "birthday",
    name: ko.observable<string>(ClientResources.controlSampleBirthday),
    format: MsPortalFx.ViewModels.Controls.Lists.Grid.Format.CustomDate,
    formatOptions: {
        dateFormat: {
            month: "long",
            day: "numeric",
        }
    }
},

```

You can create your on Intl option or use one of the predefined options from the ``Globalization.Intl`` namespace.

[Intl API DateTime][IntlAPIDateTime]
<a name="controls-grid-formatting-numbers"></a>
### Formatting Numbers
There is a single formatter for formatting numbers called the Number formatter.
The number formatter uses the Int API and will format to the current locale the user has set in the portal.
It is capable of formatting numbers in many ways including currency.

```typescript

{
    itemKey: "pairsOfShoes",
    name: ko.observable<string>(ClientResources.controlSamplePairsOfShoes),
    format: MsPortalFx.ViewModels.Controls.Lists.Grid.Format.Number,
    formatOptions: {
        numberFormat: { minimumFractionDigits: 1 }
    }
}

```

[Intl API Number][IntlAPINumber]

<a name="controls-grid-formatting-images"></a>
### Formatting Images
There are several formatters for displaying images in cells.
The preferred formatters are SvgIcon and SvgIconLookup.
The SvgIcon formatter allows you to display an SVG and optional text where the data value contains the SVG or an object containing the SVG and text.
The SvgIconLookup allows you to map data values to SVGs for display.  
There are two other similar formatters that use image uris instead of SVGs.
However, portal SVGs are preferred because they are themed.

<a name="controls-grid-formatting-uris"></a>
### Formatting Uris
There is a single Uri formatter that formats a data value containing a URI as a clickable link.
The data value can also be an object containing the URI, text, and target.

<a name="controls-grid-formatting-uris-formatting-text"></a>
#### Formatting Text
The default formatter for the Grid is the Text formatter.
There is also a TextLookup formatter that uses a map to convert specific data values to text.

<a name="controls-grid-formatting-html"></a>
### Formatting Html
The Html formatter allows you to display html.
The html is specified by your data values and can not include knockout data bindings.
If you need knockout bindings use the HtmBindings formatter.

<a name="controls-grid-custom-formatting-htmlbindings"></a>
### Custom Formatting (HtmlBindings)
The grid only has a single way to do custom formatting.
This is done using the HtmlBindings formatter.
With the HtmlBindings formatter you can specify an html template containing knockout bindings.
The $data object bound to the template will be in the following format where value is specified by the itemKey property and settings.item is your data item:

```
{
    value: any,
    settings: {
       item: T
    }
}
```

```typescript

{
    itemKey: "name",
    name: ko.observable<string>("{0}\\{1}".format(ClientResources.controlSampleName, ClientResources.controlSampleSmartPhone)),

    format: MsPortalFx.ViewModels.Controls.Lists.Grid.Format.HtmlBindings,
    formatOptions: {
        htmlBindingsTemplate: "<span data-bind='text: value'></span>\\<span data-bind='text: settings.item.smartPhone'></span>"
    }
},

```

<a name="controls-grid-selection-and-activation"></a>
### Selection and Activation
With the grid you can enable the SelectableRow extension that enables row selections and blade activations.
Selection and activation are seperate concepts that overlap in the grid.
Activation in the grid is displaying a blade.
Selection is the selecting of items within the grid.
Depending on your settings the act of selecting may also activate a blade.
This is done by either setting the selection option activateOnSelected to true or by setting specific columns to be activatable by defining `activatable = true`.
 
Blade activations can be homogeneous or heterogeneous.
For homogeneous blade activations you use BladeAction in PDL to specify the blade to open.
For heterogeneous blade activation you use DynamicBladeAction in PDL.
You must also implement createSelection to return a DynamicBladeSelection object per item.

[Grid Selection Sample][SelectableSample]
 
<a name="controls-grid-sorting"></a>
### Sorting
If you enable the SortableColumn plugin grid headers can be used to sort the data.
If you have a dataNavigator the sorting options will be passed to the navigator when changed and the navigator should handle the sorting -- typically by passing to the backend server as part of the query.
If you have local data in an observable items array the grid has a default sort callback that will sort the items in the array.
You can provide a custom sort for local data in the ``SortableColumnOptions sortCallback`` property.
 
For each column you can set the initial sortOrder.
You can also opt out of sorting for a column by setting ``sortable = false``;

[Grid Sorting Sample][SortableSample]
 
<a name="controls-grid-filtering"></a>
### Filtering
The grid has a Filterable row plugin that can be used for filtering.
The plugin provides a simple serch box UI that users can use to enter text.
The filtering can occur on the server or in the grid locally.
To enable filtering through the data navigator set serverFiltering to true.
Otherwise the filtering will occur in the grid on the client.

The client side filtering works as follows.
The set of properties to filter against are by default the itemkeys of all columns.
Alternatively, you can specify the set of properties to filter against usting the searchableColumns option.
For every searchable property the grid looks for a column definition.
If a column definition is found the grid looks for a filterableFormat option.
If a filterableFormat is found it isused to convert the data to value to a searchable string.
If a filterableFormat is not found the grid converts value to string using JSON.stringify and the text formatter.
The grid then searches for all the search terms in the formatted property values.
If every search term is found the item is added to the filter results.

[Grid Filtering Sample][FilterableSample]

<a name="controls-grid-editing"></a>
### Editing
The editable grid enables editing a list of data entities.
It allows for editing existing items, deleting items, and adding new items.
When a row is being edited the cells will be formatted with the ``editableFormat`` specified on the column.
When not being edited the cells are formatted with ``format`` specified in the column definition.
A row remains in the edit state until all the validators on the cells indicate the row is valid.

There are special formatters for editing that create form controls that allow data editing.
The formatters specifically for editing are 
- CheckBox
- TextBox
- MultiselectDropDown
- CheckBoxRowSelection
- DropDown

[Editable Grid Sample][EditableSample]
[All Controls in a Grid Sample][AllControlsSample]

<a name="controls-grid-paging"></a>
### Paging
The pagable plugin enables virtualization for large data sets using sequential and random access.
Alternatively, there is a scrollable plugin for random access scrolling.

For sequential data the ``type`` must be specified ``PageableType.Sequential``.
You must also supply a data navigator that supports loadByContinuationToken.
For sequential data the grid will load the first page of data and display a button for the user to load more data.

For random access data the ``type`` must be specified ``PageableType.Page``.
In addition a data navigator that supports loadBySkipTake is required.
For random access the grid will load the first page and display a pager control at the bottem that will allow the user to navigate through the data pages.

[Pageable Grid Sample][PageableSample]

<a name="controls-grid-grouping"></a>
### Grouping
The grid groupable plugin allows you to order your data into groups of rows with a group header.
To groups are determined by using the ``groupKey`` option to read the property of your data item.
Each item having the same value for the groupKey property will be in the same group.
By default the groups will be auto-generated for each unique group.
However, if you can generate and control the groups yourself through the ``groups`` property.

[Grid Grouping Sample][GroupedSample]

<a name="controls-grid-hierarchical"></a>
### Hierarchical
The hierarchical grid plugin allows you to display hierarchical data with expand and collapse of parent rows.
To display hierarchical data you must implement a hierarchy.
Hierarchies can be somewhat complicated to implement depending on your requirements.
Your hierarchy will supply the current items to display to the grid.
The hierarchy implementation is responsible for initializing and keeping track of the expanded states for all items.
The grid will notify the hierarchy when the user expands or collapses a row and the hierarchy must update the items.

Hierarchies may also support virtualization with the pagable or scrollable plugins.
For virtualization is common to create a custom data navigator that implements the hierarchy interface.
This is because the navigator will be outputing data items that exclude collapsed children.
Is is also important for virtual hierarchies to update the navigator ``metatdata totalItemCount`` on every expand/collapse to return the total items excluding collapsed children.
Updating the count lets the grid know the virtualization needs updating.

[Hierarchical Grid Sample (simplistic hierarchy that repeats)][HierarchicalSample]

[Pageable Hierarchical Grid Sample (also shows demand loading)][PageableHierarchicalSample]

[Scrollable Hierarchical Grid Sample (complicated structure and stream approach)][WorkitemScenarioSample]

<a name="controls-grid-context-menus"></a>
### Context Menus
The context menu shortcut is the ellipsis at the end of each grid row.
It enables displaying the context menu by click.
The context menu shorcut plugin is enabled by default.

To customize the context menu you must supply a ``commandGroup`` property on your grid item containg the command group you wish to display.

[Context Menu Shortcut Grid Sample][ContextMenuSample]
 
<a name="controls-grid-scrolling"></a>
### Scrolling
The scrollable grid plugin enables scrolling within the grid.
This is useful when the grid needs to fill an entire container and keep the headers at the top.
The container element must have a width and height or the scrolling will not display correctly.
The scrolling can be virtualized or non virtualized.

To fill a blade with the scrollable grid make the blade/part size ``FitToContainer``.
This will ensure the blade content area has a height and width set to the viewport size.
A scrollable grid fixture element directly in the blade will then work properly.

For virtualized scrolling you must supply a data navigator that supports loadBySkipTake.
For non-virtualized grids you do not supply a data navigator and just set the grid ``items`` property directly. 

[Scrollable Grid Sample][ScrollableSample]

<a name="controls-grid-reordering"></a>
### Reordering
The grid reorder row plugin allows users to reorder the items in the grid with drag drop.
The reordering can be automatic or handled by the extension using the ``reorderRow`` event.

[Reorderable Grid Sample][ReorderSample]

<a name="controls-grid-dynamic-grid-definitiona"></a>
### Dynamic Grid Definitiona
In some cases an extension may not know grid columns or other properties in advance.
In these sceanarios the extension author must define and create the grid at run-time.
There are several options for dynamic definition of a grid.

1. Create and add columns when data is available.  The columns property is an observable array and allows changes as needed.
2. Make the grid view model property on your part/blade observable. Instead of declaring `public grid: Grid.ViewModel<T>;` declare the grid as `public grid: KnockoutObservable<Grid.ViewModel<T>>;`. This makes your view model property observable so you can set it whenever you want.  You can also clear it by setting it to null. The template would be the same `<div data-bind="pcControl: grid"></div>`.
3. Use sections for layout.  If you are using sections you can add the grid to the section children dynamically.
4. CustomHtml control has an updatable inner viewmodel.
5. htmlTemplate binding allows you to dynamically specify both the view model and the template `<div data-bind="htmlTemplate: { data: viewModel, html: template }"></div>`

<a name="controls-grid-further-resources"></a>
### Further Resources
- [All Grid Samples][GridSamples]
- [Basic Grid Sample][BasicSample]
- [Formatted Grid Sample][FormattedSample]
- [Selectable Grid Sample][SelectableSample]
- [Context Menu Shortcut Grid Sample][ContextMenuSample]
- [Grouped Grid Sample][GroupedSample]
- [Filterable Grid Sample][FilterableSample]
- [Pageable Grid Sample][pageableSample]
- [Hierarchical Grid Sample][HierarchicalSample]
- [Scrollable Grid Sample][ScrollableSample]
- [Sortable Column Grid Sample][SortableSample]
- [Reorder Grid Sample][reorderSample]
- [Resizeable Column Grid Sample][resizableSample]
- [Editable Grid Sample][EditableSample]
- [All Controls in a Grid Sample][AllControlsSample]

[GridSamples]: http://aka.ms/portalfx/samples#blade/SamplesExtension/GridInstructions/selectedItem/GridInstructions/selectedValue/GridInstructions
[BasicSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/BasicGridInstructions
[FormattedSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/FormattedGridInstructions
[SelectableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/SelectableGridInstructions
[ContextMenuSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/ContextMenuShortcutGridInstructions
[GroupedSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/GroupedGridInstructions
[FilterableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/FilterableGridInstructions
[PageableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/PageableGridInstructions
[HierarchicalSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/HierarchicalGridInstructions
[ScrollableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/ScrollableGridInstructions
[SortableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/SortableColumnGridInstructions
[ReorderSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/ReorderGridInstructions
[ResizeableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/ResizableColumnGridInstructions
[EditableSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/EditableGridInstructions
[AllControlsSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/AllControlsGridInstructions
[PageableHierarchicalSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/PageableHierarchicalGridInstructions
[WorkitemScenarioSample]: http://aka.ms/portalfx/samples#blade/SamplesExtension/SDKMenuBlade/scenariosworkitem
[IntlAPIDateTime] https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/DateTimeFormat
[IntlAPINumber] https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NumberFormat

	
<a name="controls-helpers-and-indicators"></a>
## Helpers and Indicators

- [Docked Balloon](http://aka.ms/portalfx/samples#blade/SamplesExtension/DockedBalloonInstructions/selectedItem/DockedBalloonInstructions/selectedValue/DockedBalloonInstructions)
- [Info Box](http://aka.ms/portalfx/samples#blade/SamplesExtension/InfoBoxInstructions/selectedItem/InfoBoxInstructions/selectedValue/InfoBoxInstructions)
- [Progress Bar](http://aka.ms/portalfx/samples#blade/SamplesExtension/ProgressBarInstructions/selectedItem/ProgressBarInstructions/selectedValue/ProgressBarInstructions)

<a name="controls-visualizing-data"></a>
## Visualizing Data

- Chart
    ## Charts
Insert chart controls in your experience to allow your users to visualize and analyze their data.

[Chart](../media/portalfx-ui-concepts/chart.png)

In most cases, you will probably want to use the chart [intrinsic part](portalfx-.md). The intrinsic part is maintained by the framework and will provide you with consistent layout with the rest of the portal.

If you are using a custom part template, charts can be added with the following html:

```xml
<div data-bind='pcChart: chartVM' style='height:500px'></div>
```

<a name="controls-visualizing-data-chart-views-and-series-views"></a>
### Chart views and series views

Our charts include the following **chart view** types which can be used separately or in tandem:

* Line
* Grouped bar
* Stacked bar
* Scatter
* Area
* Stacked area 

Chart views are the high-level view type for your chart.

```ts
// Initialize the view.  This is the code that makes this chart a bar chart.
var barChartView = new MsPortalFx.ViewModels.Controls.Visualization.Chart.BarChartView<string, number>(MsPortalFx.ViewModels.Controls.Visualization.Chart.BarChartType.Grouped);
this.chartVM.views([barChartView]);
```

A sample chart viewmodel with a single chart view type can be found here:
`\Client\Controls\Chart\ViewModels\BarChartViewModels.ts`

A sample chart viewmodel with multiple chart view types can be found here:
`\Client\Controls\Chart\ViewModels\OverlayedViewChartViewModel.ts`

**Series views** are visualizations of individual data series. Series views allow you to modify the color, display name, and interaction behavior of a particular series.

By default, series views will be generated for each of the chart views and each of the data series you add to your chart. For example, let's say you added three data series, seriesA, seriesB, and seriesC to a chart that has two chart views, a bar chart view and a line chart view. Your chart would have 6 series views, a bar chart series view and a line chart series view for each series. This default behavior is ideal for simple charts, especially those with one chart view type.

In some cases you may want to do some more interesting things with series views. Perhaps instead you want seriesA and seriesB to be visualized as bars and seriesC to be visualized as a line. To achieve this behavior you will need to turn off the auto-generate behavior.

```ts
this.chartVM.autogenerateSeriesViews(false);
```

You can then create and specialize your series views however you'd like.

```ts
var lineSeriesView = new MsPortalFx.ViewModels.Controls.Visualization.Chart.LineChartSeriesView<string, number>();
lineSeriesView.seriesName("LineSeries");
lineSeriesView.cssClass("msportalfx-bgcolor-c1");

var barSeriesView = new MsPortalFx.ViewModels.Controls.Visualization.Chart.SeriesView<string, number>(MsPortalFx.ViewModels.Controls.Visualization.Chart.BarChartType.Stacked);
barSeriesView.seriesName("BarSeries");

lineChartView.seriesView([lineSeriesView]);
barChartView.seriesView([barSeriesView]);
```

A good example of using the chart's auto-generated series views functionality is:
`\Client\Controls\Chart\ViewModels\LineChartDateBasedViewModels.ts`

To see a more advanced sample where series views are created explicitly by the extension see
`\Client\Controls\Chart\ViewModels\OverlayedViewChartViewModels.ts`

<a name="controls-visualizing-data-metrics"></a>
### Metrics
Metrics are the big data call-outs that pair with our chart controls to give the user interactive peeks into their data. Metrics can be configured manually by handling chart events, calculating values, and passing information to the metrics controls or by setting up metrics rules. 

![Chart metrics](../media/portalfx-ui-concepts/chartMetrics.png)

<a name="controls-visualizing-data-metrics-rules"></a>
### Metrics rules
Metrics rules are a rule-based system that automatically hooks up metric values to different user interactions. For instance, by default (when the user is not interacting with the chart area) you may want your chart metrics to show the average value of each data series. This rule can be configured like so:

```ts
metricRule1.scope(Chart.MetricRuleScope.Default);
metricRule1_metric1.aggregationScope(Chart.MetricRuleAggregationScope.AllSeparately);
metricRule1_metric1.aggregationType(Chart.MetricRuleAggregationType.AverageY);
```

With this rule configured, when the user is not interacting with the chart area they will see one metric representing the average value of each data series on the chart.

See the following file for a full example of the metrics rules implementation:
`\Client\Controls\Chart\ViewModels\LineChartDateTimeViewModels.ts`


- Donut
  	
<a name="controls-donut-chart"></a>
## Donut chart

Donut charts are a great way to visualize proportional data.

![Donut](../media/portalfx-ui-concepts/donut.png)

Donuts can be added to your part templates with the following html:

```xml
<div data-bind='pcDonut: donutVM' style='height:500px; width:500px'></div>
```

A sample view model can be found here:

`\Client\Controls\Donut\ViewModels\DonutViewModels.ts`

Other visualization controls:

* [Chart](portalfx-controls-chart.md)

	
- Gauges
  - [Quota Gauge](http://aka.ms/portalfx/samples#blade/SamplesExtension/QuotaGaugeBlade)
  - [Single Value Gauge](http://aka.ms/portalfx/samples#blade/SamplesExtension/SingleValueGaugeBlade)
  - [Step Gauge](http://aka.ms/portalfx/samples#blade/SamplesExtension/StepGaugeBlade)
- Graphs
  - [Standard Graph](http://aka.ms/portalfx/samples#blade/SamplesExtension/graphInstructions)
  - [Custom Html Nodes](http://aka.ms/portalfx/samples#blade/SamplesExtension/graphCustomNodeInstructions)
- [Metrics](http://aka.ms/portalfx/samples#blade/SamplesExtension/MetricsInstructions/selectedItem/MetricsInstructions/selectedValue/MetricsInstructions)
- Maps
  - [Base Map](http://aka.ms/portalfx/samples#blade/SamplesExtension/BaseMapInstructions)
  - [Hexagon Layout Map](http://aka.ms/portalfx/samples#blade/SamplesExtension/HexagonMapInstructions)
- [Menu](http://aka.ms/portalfx/samples#blade/SamplesExtension/MenuInstructions/selectedItem/MenuInstructions/selectedValue/MenuInstructions)
- [Log Stream](http://aka.ms/portalfx/samples#blade/SamplesExtension/LogStreamInstructions/selectedItem/LogStreamInstructions/selectedValue/LogStreamInstructions)
- [Spec Comparison Table](http://aka.ms/portalfx/samples#blade/SamplesExtension/SpecComparisonTableInstructions/selectedItem/SpecComparisonTableInstructions/selectedValue/SpecComparisonTableInstructions)
- [Video Control](http://aka.ms/portalfx/samples#blade/SamplesExtension/VideoInstructions/selectedItem/VideoInstructions/selectedValue/VideoInstructions)
- [Legend](http://aka.ms/portalfx/samples#blade/SamplesExtension/Legend/selectedItem/Legend/selectedValue/Legend)
- [HotSpot](http://aka.ms/portalfx/samples#blade/SamplesExtension/HotSpotInstructions/selectedItem/HotSpotInstructions/selectedValue/HotSpotInstructions)
- [Video](http://aka.ms/portalfx/samples#blade/SamplesExtension/VideoInstructions/selectedItem/VideoInstructions/selectedValue/VideoInstructions)
- [Terminal Emulator](http://aka.ms/portalfx/samples#blade/SamplesExtension/TerminalEmulatorInstructionsBlade/selectedItem/TerminalEmulatorInstructionsBlade/selectedValue/TerminalEmulatorInstructionsBlade)

