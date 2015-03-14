# radiobutton widget #

A [GtkRadioButton](http://developer.gnome.org/gtk2/2.24/GtkRadioButton.html)


---


## Definition ##

```
<radiobutton tag_attr="value"...>
	<label>text</label>
	<default>state</default>
	<variable>varname</variable>
	<input>command</input>
	<input file>filename</input>
	<sensitive>state</sensitive>
	<action>activity</action>...
	<action signal="type">activity</action>...
	<action function="type">parameter</action>...
	<output file>filename</output>
</radiobutton>
```

"..." denotes acceptance of multiples of the same thing.

## Tag Attributes ##

See the [GtkRadioButton](http://developer.gnome.org/gtk2/2.24/GtkRadioButton.html#GtkRadioButton.object-hierarchy) widget and ancestor class properties.

The following custom tag attributes are available:

<a href='Hidden comment: ExportTableStart'></a>
| **Name** | **Description** | **Value** | **Since** |
|:---------|:----------------|:----------|:----------|
| space-expand | Pack widget expanding into space | `true` or `false` | 0.7.21 |
| space-fill | Pack widget filling space | `true` or `false` | 0.7.21 |
| block-function-signals | Block signal emissions from functions | `true` or `false` | 0.7.21 |
| file-monitor | Emit signal when input file(s) change | `true` or `false` | 0.8.1 |
| auto-refresh | Auto refresh when input file(s) change | `true` or `false` | 0.8.1 |
<a href='Hidden comment: ExportTableEnd'></a>

## Directives ##

Some of these may have tag attribute equivalents.

<a href='Hidden comment: ExportTableStart'></a>
| **Name** | **Description** | **Contents** | **Since** |
|:---------|:----------------|:-------------|:----------|
| label | Initial text |  |  |
| default | Initial state | `true` or `false` |  |
| variable | Variable name |  |  |
| variable export="false" | Variable name, not exported to shell |  | 0.8.3 |
| input | Data input source | Shell command | 0.8.1 |
| input file | Data input source | Filename | 0.8.1 |
| sensitive | Sensitive state | `true` or `false` |  |
| action | Execute command on default signal | Shell command<sup>[1]</sup> |  |
| action | Perform function on default signal | _function_:_parameter_<sup>[1]</sup> |  |
| action signal="_type_" | Execute command on signal | Shell command<sup>[1]</sup> |  |
| action signal="_type_" | Perform function on signal | _function_:_parameter_<sup>[1]</sup> |  |
| action function="_type_" | Perform function on default signal | _parameter_<sup>[1]</sup> | 0.8.3 |
| action condition="_type_" | Execute command on default signal conditionally | Shell command<sup>[1]</sup> | 0.8.3 |
| action condition="_type_" | Perform function on default signal conditionally | _function_:_parameter_<sup>[1]</sup> | 0.8.3 |
| action signal="_type_" condition="_type_" | Execute command on signal conditionally | Shell command<sup>[1]</sup> | 0.8.3 |
| action signal="_type_" condition="_type_" | Perform function on signal conditionally | _function_:_parameter_<sup>[1]</sup> | 0.8.3 |
| action function="_type_" condition="_type_" | Perform function on default signal conditionally | _parameter_<sup>[1]</sup> | 0.8.3 |
| output file | Data output target | Filename | 0.8.1 |
<a href='Hidden comment: ExportTableEnd'></a>

## Signals ##

The default signal is "[toggled](http://developer.gnome.org/gtk2/2.24/GtkToggleButton.html#GtkToggleButton-toggled)", emitted when the state is changed.

The "file-changed" signal is emitted if file-monitor is true and the input file being monitored has changed.

The following signals are connected-up for all widgets:

[button-press-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-button-press-event), [button-release-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-button-release-event), [configure-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-configure-event), [enter-notify-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-enter-notify-event), [leave-notify-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-leave-notify-event), [focus-in-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-focus-in-event), [focus-out-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-focus-out-event), [hide](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-hide), [show](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-show), [realize](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-realize), [key-press-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-key-press-event), [key-release-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-key-release-event), [map-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-map-event), [unmap-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-unmap-event)

## Functions ##

The following functions can be performed upon this widget by any widget capable of emitting signals:

<a href='Hidden comment: ExportTableStart'></a>
| **Type** | **Description** | **Parameter** | **Since** |
|:---------|:----------------|:--------------|:----------|
| enable | Sensitise widget | Variable name |  |
| disable | Desensitise widget | Variable name |  |
| show | Show widget | Variable name | 0.8.1 |
| hide | Hide widget | Variable name | 0.8.1 |
| activate | Activate widget | Variable name | 0.8.1 |
| grabfocus | Grab input focus | Variable name | 0.8.1 |
| refresh | Reload input data | Variable name | 0.8.1 |
| save | Save widget data | Variable name | 0.8.1 |
| clear | Remove all widget data | Variable name | 0.8.1 |
<a href='Hidden comment: ExportTableEnd'></a>

The following general functions can be performed by any widget capable of emitting signals:

<a href='Hidden comment: ExportTableStart'></a>
| **Type** | **Description** | **Parameter** | **Since** |
|:---------|:----------------|:--------------|:----------|
| break | Break out of actions list | None | 0.8.3 |
| command | Execute command | Shell command |  |
| exit | Exit dialog | A value for the `EXIT` variable |  |
| closewindow | Close dialog | Variable name |  |
| launch | Launch dialog | Variable name |  |
| presentwindow | [Present](http://developer.gnome.org/gtk2/2.24/GtkWindow.html#gtk-window-present) dialog | Variable name | 0.8.1 |
<a href='Hidden comment: ExportTableEnd'></a>

## Conditions ##

The following conditions can be used within the condition attribute of action directives:

<a href='Hidden comment: ExportTableStart'></a>
| **Type** | **Description** | **Argument** | **Since** |
|:---------|:----------------|:-------------|:----------|
| active\_is\_true(_argument_) | Active state of toggle widget | Variable name | 0.8.3 |
| active\_is\_false(_argument_) | Active state of toggle widget | Variable name | 0.8.3 |
| command\_is\_true(_argument_) | Output of shell command | Shell command | 0.8.3 |
| command\_is\_false(_argument_) | Output of shell command | Shell command | 0.8.3 |
| file\_is\_true(_argument_) | Contents of a file | Filename | 0.8.3 |
| file\_is\_false(_argument_) | Contents of a file | Filename | 0.8.3 |
| sensitive\_is\_true(_argument_) | Sensitive state of widget | Variable name | 0.8.3 |
| sensitive\_is\_false(_argument_) | Sensitive state of widget | Variable name | 0.8.3 |
| visible\_is\_true(_argument_) | Visible state of widget | Variable name | 0.8.3 |
| visible\_is\_false(_argument_) | Visible state of widget | Variable name | 0.8.3 |
<a href='Hidden comment: ExportTableEnd'></a>

true means "true", "yes" or a non-zero value, false means "false", "no" or zero, therefore the shell command is expected to echo one of these values to stdout.

## Notes ##

1. This widget's actions can be conditionally executed (based upon its active state) by prepending its contents with `if true` or `if false` although 0.8.3 introduced a dedicated condition attribute which may be more suitable.


---