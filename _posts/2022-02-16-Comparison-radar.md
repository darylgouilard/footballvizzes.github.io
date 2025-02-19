<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RadarComparing</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0px solid transparent;
  border-right: 0px solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0px solid transparent;
  border-bottom: 0px solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
	border:1px solid transparent;
  background-color: transparent;
  position: absolute;
	z-index:1;
	right:3%;
	top: 0;
	bottom: 0;
	margin: auto;
	padding: 7px 0;
	display: none;
	vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
	content: "X";
	display: block;
	width: 15px;
	height: 15px;
	text-align: center;
	color:#000;
	font-weight: normal;
	font-size: 12px;
	cursor: pointer;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
  background: inherit;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-bottom:10px;
  margin-top:0; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  font-size:36px;
  line-height:40px; }

h2.bp3-heading, .bp3-running-text h2{
  font-size:28px;
  line-height:32px; }

h3.bp3-heading, .bp3-running-text h3{
  font-size:22px;
  line-height:25px; }

h4.bp3-heading, .bp3-running-text h4{
  font-size:18px;
  line-height:21px; }

h5.bp3-heading, .bp3-running-text h5{
  font-size:16px;
  line-height:19px; }

h6.bp3-heading, .bp3-running-text h6{
  font-size:14px;
  line-height:16px; }
.bp3-ui-text{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none; }

.bp3-monospace-text{
  font-family:monospace;
  text-transform:none; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  font-size:14px;
  line-height:1.5; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15);
    margin:20px 0; }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  color:#106ba3;
  text-decoration:none; }
  a:hover{
    color:#106ba3;
    cursor:pointer;
    text-decoration:underline; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  font-size:smaller;
  padding:2px 5px; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  color:#182026;
  display:block;
  font-size:13px;
  line-height:1.4;
  margin:10px 0;
  padding:13px 15px 12px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit;
    font-size:inherit;
    padding:0; }

.bp3-running-text kbd, .bp3-key{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-family:inherit;
  font-size:12px;
  height:24px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  line-height:24px;
  min-width:24px;
  padding:3px 6px;
  vertical-align:middle; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  margin:0 0 10px;
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    font-size:40px;
    margin-right:20px;
    margin-top:0; }

.bp3-alert-contents{
  word-break:break-word; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  cursor:default;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  height:30px;
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-breadcrumbs > li{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }
    .bp3-breadcrumbs > li::after{
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 00-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 001.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      content:"";
      display:block;
      height:16px;
      margin:0 5px;
      width:16px; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    font-size:inherit;
    font-weight:inherit;
    vertical-align:baseline; }

.bp3-breadcrumbs-collapsed{
  background:#ced9e0;
  border:none;
  border-radius:3px;
  cursor:pointer;
  margin-right:2px;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    content:"";
    display:block;
    height:16px;
    width:16px; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    color:#182026;
    text-decoration:none; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  min-height:30px;
  min-width:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      background-color:#106ba3;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      background-color:#0e5a8a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      background-color:#0d8050;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      background-color:#0a6640;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      background-color:#bf7326;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      background-color:#a66321;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      background-color:#c23030;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      background-color:#a82a2a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-height:40px;
    min-width:40px;
    font-size:16px;
    padding:5px 15px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      margin:0;
      position:absolute; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button.bp3-minimal:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button.bp3-outlined{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    border:1px solid rgba(24, 32, 38, 0.2);
    -webkit-box-sizing:border-box;
            box-sizing:border-box; }
    .bp3-button.bp3-outlined:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-outlined:active, .bp3-button.bp3-outlined.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-outlined{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-outlined:hover, .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-outlined:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover, .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover, .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover, .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover, .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled:hover{
      border-color:rgba(92, 112, 128, 0.1); }
    .bp3-dark .bp3-button.bp3-outlined{
      border-color:rgba(255, 255, 255, 0.4); }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        border-color:rgba(255, 255, 255, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      border-color:rgba(16, 107, 163, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        border-color:rgba(16, 107, 163, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        border-color:rgba(72, 175, 240, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          border-color:rgba(72, 175, 240, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      border-color:rgba(13, 128, 80, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        border-color:rgba(13, 128, 80, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        border-color:rgba(61, 204, 145, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          border-color:rgba(61, 204, 145, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      border-color:rgba(191, 115, 38, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        border-color:rgba(191, 115, 38, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        border-color:rgba(255, 179, 102, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          border-color:rgba(255, 179, 102, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      border-color:rgba(194, 48, 48, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        border-color:rgba(194, 48, 48, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        border-color:rgba(255, 115, 115, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          border-color:rgba(255, 115, 115, 0.2); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    border-bottom-right-radius:0;
    border-top-right-radius:0;
    margin-right:-1px; }
  .bp3-button-group.bp3-minimal .bp3-button{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      height:100%;
      width:unset; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  font-size:14px;
  line-height:1.5;
  background-color:rgba(138, 155, 168, 0.15);
  border-radius:3px;
  padding:10px 12px 9px;
  position:relative;
  width:100%; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout .bp3-heading{
    line-height:20px;
    margin-bottom:5px;
    margin-top:0; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  opacity:0.9;
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  width:100%; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }

.bp3-dialog{
  background:#ebf1f5;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text;
  width:500px; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    background:#293742;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-dialog-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding-left:20px;
  padding-right:5px;
  z-index:30; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    background:#30404d;
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  margin:20px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-multistep-dialog-panels{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }

.bp3-multistep-dialog-left-panel{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column; }
  .bp3-dark .bp3-multistep-dialog-left-panel{
    background:#202b33; }

.bp3-multistep-dialog-right-panel{
  background-color:#f5f8fa;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  border-radius:0 0 6px 0;
  -webkit-box-flex:3;
      -ms-flex:3;
          flex:3;
  min-width:0; }
  .bp3-dark .bp3-multistep-dialog-right-panel{
    background-color:#293742;
    border-left:1px solid rgba(16, 22, 26, 0.4); }

.bp3-multistep-dialog-footer{
  background-color:#ffffff;
  border-radius:0 0 6px 0;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  padding:10px; }
  .bp3-dark .bp3-multistep-dialog-footer{
    background:#30404d;
    border-top:1px solid rgba(16, 22, 26, 0.4); }

.bp3-dialog-step-container{
  background-color:#f5f8fa;
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-dialog-step-container{
    background:#293742;
    border-bottom:1px solid rgba(16, 22, 26, 0.4); }
  .bp3-dialog-step-container.bp3-dialog-step-viewed{
    background-color:#ffffff; }
    .bp3-dark .bp3-dialog-step-container.bp3-dialog-step-viewed{
      background:#30404d; }

.bp3-dialog-step{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#f5f8fa;
  border-radius:6px;
  cursor:not-allowed;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:4px;
  padding:6px 14px; }
  .bp3-dark .bp3-dialog-step{
    background:#293742; }
  .bp3-dialog-step-viewed .bp3-dialog-step{
    background-color:#ffffff;
    cursor:pointer; }
    .bp3-dark .bp3-dialog-step-viewed .bp3-dialog-step{
      background:#30404d; }
  .bp3-dialog-step:hover{
    background-color:#f5f8fa; }
    .bp3-dark .bp3-dialog-step:hover{
      background:#293742; }

.bp3-dialog-step-icon{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:rgba(92, 112, 128, 0.6);
  border-radius:50%;
  color:#ffffff;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:25px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:25px; }
  .bp3-dark .bp3-dialog-step-icon{
    background-color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#2b95d6; }
  .bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#8a9ba8; }

.bp3-dialog-step-title{
  color:rgba(92, 112, 128, 0.6);
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  padding-left:10px; }
  .bp3-dark .bp3-dialog-step-title{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-title{
    color:#2b95d6; }
  .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
    color:#182026; }
    .bp3-dark .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
      color:#f5f8fa; }
.bp3-drawer{
  background:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    height:50%;
    left:0;
    right:0;
    top:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-bottom{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-left{
    bottom:0;
    left:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-right{
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    background:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-drawer-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding:5px;
  padding-left:20px;
  position:relative; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  overflow:auto; }

.bp3-drawer-footer{
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  padding:10px 20px;
  position:relative; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  cursor:text;
  display:inline-block;
  max-width:100%;
  position:relative;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    bottom:-3px;
    left:-3px;
    position:absolute;
    right:-3px;
    top:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  color:inherit;
  display:inherit;
  font:inherit;
  letter-spacing:inherit;
  max-width:inherit;
  min-width:inherit;
  position:relative;
  resize:none;
  text-transform:inherit;
  vertical-align:top; }

.bp3-editable-text-input{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0;
  white-space:pre-wrap;
  width:100%; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    left:0;
    position:absolute;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    border-radius:inherit;
    z-index:2; }
    .bp3-control-group .bp3-input:focus{
      border-radius:3px;
      z-index:14; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    border-radius:inherit;
    z-index:4; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-left-container,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group .bp3-select:focus-within{
    z-index:5; }
  .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:-1px; }
  .bp3-control-group:not(.bp3-vertical) > .bp3-divider:not(:first-child){
    margin-left:6px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    border-radius:0 3px 3px 0;
    margin-right:0; }
  .bp3-control-group > :only-child{
    border-radius:3px;
    margin-right:0; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group .bp3-numeric-input:not(:first-child) .bp3-input-group{
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-control-group.bp3-fill{
    width:100%; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      border-radius:3px 3px 0 0;
      margin-top:0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  cursor:pointer;
  display:block;
  margin-bottom:10px;
  position:relative;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    left:0;
    opacity:0;
    position:absolute;
    top:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    cursor:pointer;
    display:inline-block;
    font-size:16px;
    height:1em;
    margin-right:10px;
    margin-top:-3px;
    position:relative;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none;
    vertical-align:middle;
    width:1em; }
    .bp3-control .bp3-control-indicator::before{
      content:"";
      display:block;
      height:1em;
      width:1em; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    background:#d8e1e8;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-left:10px;
    margin-top:1px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 00-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0012 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:auto; }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      background:#ffffff;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      height:calc(1em - 4px);
      left:0;
      margin:2px;
      position:absolute;
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      width:calc(1em - 4px); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    font-size:0.7em;
    text-align:center; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    line-height:0;
    margin-left:0.5em;
    margin-right:1.2em;
    visibility:hidden; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    line-height:1em;
    margin-left:1.2em;
    margin-right:0.5em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    line-height:1em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    line-height:0;
    visibility:hidden; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      background:#202b33;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  cursor:pointer;
  display:inline-block;
  height:30px;
  position:relative; }
  .bp3-file-input input{
    margin:0;
    min-width:200px;
    opacity:0; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      background:rgba(206, 217, 224, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(92, 112, 128, 0.6);
        cursor:not-allowed;
        outline:none; }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        background:rgba(57, 75, 89, 0.5);
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          -webkit-box-shadow:none;
                  box-shadow:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:rgba(92, 112, 128, 0.6);
  left:0;
  padding-right:80px;
  position:absolute;
  right:0;
  top:0;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-file-upload-input::after{
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026;
    min-height:24px;
    min-width:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    border-radius:3px;
    content:"Browse";
    line-height:24px;
    margin:3px;
    position:absolute;
    right:0;
    text-align:center;
    top:0;
    width:70px; }
    .bp3-file-upload-input::after:hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-file-upload-input:active::after{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-large .bp3-file-upload-input{
    font-size:16px;
    height:40px;
    line-height:40px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-height:30px;
      min-width:30px;
      line-height:30px;
      margin:5px;
      width:85px; }
  .bp3-dark .bp3-file-upload-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        background-color:#30404d;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        background-color:#202b33;
        background-image:none;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:active::after{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    color:#5c7080;
    font-size:12px;
    margin-top:5px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      line-height:40px;
      margin:0 10px 0 0; }
    .bp3-form-group.bp3-inline label.bp3-label{
      line-height:30px;
      margin:0 10px 0 0; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-input-left-container:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-input-left-container:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-height:24px;
    min-width:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-icon{
    z-index:1; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon{
    color:#5c7080; }
    .bp3-input-group > .bp3-input-left-container > .bp3-icon:empty,
    .bp3-input-group > .bp3-icon:empty{
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-height:30px;
    min-width:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle; }
  .bp3-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-input.bp3-large{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-bottom:15px;
  margin-top:0; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    font-weight:400;
    vertical-align:top;
    width:100%; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  min-height:0;
  padding:0;
  width:30px; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  -moz-appearance:none;
  -webkit-appearance:none;
  border-radius:3px;
  height:30px;
  padding:0 25px 0 10px;
  width:100%; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  background:none;
  -webkit-box-shadow:none;
          box-shadow:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    background:rgba(167, 182, 194, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026;
    text-decoration:none; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    background:rgba(115, 134, 148, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      color:rgba(167, 182, 194, 0.6);
      cursor:not-allowed; }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  font-size:16px;
  height:40px;
  padding-right:35px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    background-color:#202b33;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  background-color:rgba(206, 217, 224, 0.5);
  -webkit-box-shadow:none;
          box-shadow:none;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  color:#5c7080;
  pointer-events:none;
  position:absolute;
  right:7px;
  top:7px; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  letter-spacing:normal;
  position:relative;
  vertical-align:middle; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    right:12px;
    top:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select option:disabled, .bp3-dark
  .bp3-select option:disabled{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    text-align:left;
    vertical-align:top; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td,
  .bp3-running-text table tfoot tr:first-child th,
  table.bp3-html-table tfoot tr:first-child th,
  .bp3-running-text table tfoot tr:first-child td,
  table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td,
  .bp3-dark .bp3-running-text table tfoot tr:first-child th,
  .bp3-running-text .bp3-dark table tfoot tr:first-child th,
  .bp3-dark table.bp3-html-table tfoot tr:first-child th,
  .bp3-dark .bp3-running-text table tfoot tr:first-child td,
  .bp3-running-text .bp3-dark table tfoot tr:first-child td,
  .bp3-dark table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-bottom:6px;
  padding-top:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td,
table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
  table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table{ }
  .bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
    background:rgba(92, 112, 128, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td,
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
      -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
              box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
    background-color:rgba(92, 112, 128, 0.3);
    cursor:pointer; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
    background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  padding-bottom:0;
  top:40px; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-left:0;
  margin-right:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  font-family:"Icons20";
  font-size:inherit;
  font-style:normal;
  font-weight:400;
  line-height:1; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagnosis::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-lab-test::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }
  .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{ }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  background:#ffffff;
  border-radius:3px;
  color:#182026;
  list-style:none;
  margin:0;
  min-width:180px;
  padding:5px;
  text-align:left; }

.bp3-menu-divider{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px; }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  color:inherit;
  line-height:20px;
  padding:5px 7px;
  text-decoration:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    color:#5c7080;
    margin-top:2px; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit !important;
    color:rgba(92, 112, 128, 0.6) !important;
    cursor:not-allowed !important;
    outline:none !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    font-size:16px;
    line-height:22px;
    padding:9px 7px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-right:10px;
      margin-top:1px; }

button.bp3-menu-item{
  background:none;
  border:none;
  text-align:left;
  width:100%; }
.bp3-menu-header{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px;
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    line-height:17px;
    margin:0;
    padding:10px 7px 0 1px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    font-size:18px;
    padding-bottom:5px;
    padding-top:15px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item{ }
  .bp3-dark .bp3-menu-item.bp3-intent-primary{
    color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-success{
    color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning{
    color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger{
    color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item::before,
  .bp3-dark .bp3-menu-item > .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item .bp3-menu-item-label{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
    background-color:rgba(138, 155, 168, 0.3); }
  .bp3-dark .bp3-menu-item.bp3-disabled{
    color:rgba(167, 182, 194, 0.6) !important; }
    .bp3-dark .bp3-menu-item.bp3-disabled::before,
    .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  background-color:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  height:50px;
  padding:0 15px;
  position:relative;
  width:100%;
  z-index:10; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    left:0;
    position:fixed;
    right:0;
    top:0; }

.bp3-navbar-heading{
  font-size:16px;
  margin-right:15px; }

.bp3-navbar-group{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px;
  margin:0 10px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:100%;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  text-align:center;
  width:100%; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  bottom:0;
  left:0;
  position:static;
  right:0;
  top:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    overflow:hidden;
    position:fixed; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    overflow:auto;
    position:fixed; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  bottom:0;
  left:0;
  position:fixed;
  right:0;
  top:0;
  opacity:1;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  z-index:20; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }
  .bp3-panel-stack-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-panel-stack2{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack2-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack2-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack2-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack2-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack2-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack2-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-view{
    background-color:#30404d; }
  .bp3-panel-stack2-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter, .bp3-panel-stack2-push .bp3-panel-stack2-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter-active, .bp3-panel-stack2-push .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter, .bp3-panel-stack2-pop .bp3-panel-stack2-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter-active, .bp3-panel-stack2-pop .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  border-radius:3px;
  display:inline-block;
  z-index:20; }
  .bp3-popover .bp3-popover-arrow{
    height:30px;
    position:absolute;
    width:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      height:20px;
      margin:5px;
      width:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-bottom:17px;
    margin-top:-17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-left:-17px;
    margin-right:17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover .bp3-popover-content{
    border-radius:3px;
    position:relative; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  border-radius:2px;
  content:"";
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg); }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  left:0;
  position:absolute;
  right:0;
  top:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  background:rgba(92, 112, 128, 0.2);
  border-radius:40px;
  display:block;
  height:8px;
  overflow:hidden;
  position:relative;
  width:100%; }
  .bp3-progress-bar .bp3-progress-meter{
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    border-radius:40px;
    height:100%;
    position:absolute;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:100%; }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  color:transparent !important;
  cursor:default;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  height:40px;
  min-width:150px;
  width:100%;
  cursor:default;
  outline:none;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    cursor:not-allowed;
    opacity:0.5; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  height:6px;
  left:0;
  right:0;
  top:5px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  height:16px;
  left:0;
  position:absolute;
  top:0;
  width:16px; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab;
    z-index:2; }
  .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    background:#bfccd6;
    -webkit-box-shadow:none;
            box-shadow:none;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    background:#5c7080;
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-slider-handle .bp3-slider-label{
    background:#394b59;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    color:#f5f8fa;
    margin-left:8px; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      background:#e1e8ed;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-bottom-right-radius:0;
    border-top-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    border-bottom-left-radius:0;
    border-top-left-radius:0;
    margin-left:8px; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  font-size:12px;
  line-height:1;
  padding:2px 5px;
  position:absolute;
  vertical-align:top; }

.bp3-slider.bp3-vertical{
  height:150px;
  min-width:40px;
  width:40px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    bottom:0;
    height:auto;
    left:5px;
    top:0;
    width:6px; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-left:0;
      margin-top:-8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      height:8px;
      margin-left:0;
      width:16px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-bottom-right-radius:3px;
      border-top-left-radius:0; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      border-bottom-left-radius:0;
      border-bottom-right-radius:0;
      border-top-left-radius:3px;
      margin-bottom:8px; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round;
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      padding:0 10px;
      width:100%; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        background-color:rgba(19, 124, 189, 0.2);
        -webkit-box-shadow:none;
                box-shadow:none; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      background-color:rgba(19, 124, 189, 0.2);
      border-radius:3px;
      bottom:0;
      height:auto;
      left:0;
      right:0;
      top:0; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  border:none;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  list-style:none;
  margin:0;
  padding:0;
  position:relative; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:#182026;
  cursor:pointer;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  font-size:14px;
  line-height:30px;
  max-width:100%;
  position:relative;
  vertical-align:top; }
  .bp3-tab a{
    color:inherit;
    display:block;
    text-decoration:none; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    background-color:transparent !important;
    -webkit-box-shadow:none !important;
            box-shadow:none !important; }
  .bp3-tab[aria-disabled="true"]{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    font-size:16px;
    line-height:40px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  left:0;
  pointer-events:none;
  position:absolute;
  top:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    background-color:#106ba3;
    bottom:0;
    height:3px;
    left:0;
    position:absolute;
    right:0; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#5c7080;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  color:#f5f8fa;
  font-size:12px;
  line-height:16px;
  max-width:100%;
  min-height:20px;
  min-width:20px;
  padding:2px 6px;
  position:relative; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-left:8px;
    padding-right:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    font-size:14px;
    line-height:20px;
    min-height:30px;
    min-width:30px;
    padding:5px 10px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-left:12px;
      padding-right:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  background:none;
  border:none;
  color:inherit;
  cursor:pointer;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin-bottom:-2px;
  margin-right:-6px !important;
  margin-top:-2px;
  opacity:0.5;
  padding:2px;
  padding-left:0; }
  .bp3-tag-remove:hover{
    background:none;
    opacity:0.8;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:0 5px 0 0; }
    .bp3-large .bp3-tag-remove:empty::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  line-height:inherit;
  min-height:30px;
  padding-left:5px;
  padding-right:0; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    color:#5c7080;
    margin-left:2px;
    margin-right:7px;
    margin-top:7px; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    margin-right:7px;
    margin-top:5px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:20px;
    width:80px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-left:5px;
      margin-top:10px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-height:30px;
      min-width:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:20px 0 0;
  max-width:500px;
  min-width:300px;
  pointer-events:all;
  position:relative !important; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-delay:50ms;
            transition-delay:50ms;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    color:#5c7080;
    margin:12px;
    margin-right:0; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    background-color:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  left:0;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none;
  right:0;
  z-index:40; }
  .bp3-toast-container.bp3-toast-container-in-portal{
    position:fixed; }
  .bp3-toast-container.bp3-toast-container-inline{
    position:absolute; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0; }
  .bp3-toast-container.bp3-toast-container-bottom{
    bottom:0;
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-exit-active ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    height:22px;
    position:absolute;
    width:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      height:14px;
      margin:4px;
      width:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-bottom:11px;
    margin-top:-11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-left:-11px;
    margin-right:11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  list-style:none;
  margin:0;
  padding-left:0; }

.bp3-tree-root{
  background-color:transparent;
  cursor:default;
  padding-left:0;
  position:relative; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:30px;
  padding-right:5px;
  width:100%; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  cursor:pointer;
  padding:7px;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  margin-right:7px;
  position:relative; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  left:calc(50% - 250px);
  top:20vh;
  width:500px;
  z-index:21; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar .bp3-input{
    background-color:transparent;
    border-radius:0; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    background-color:transparent;
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MC45NzggNTAuOTc4IiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA1MC45NzggNTAuOTc4OyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+Cgk8Zz4KCQk8cGF0aCBzdHlsZT0iZmlsbDojMDEwMDAyOyIgZD0iTTQzLjUyLDcuNDU4QzM4LjcxMSwyLjY0OCwzMi4zMDcsMCwyNS40ODksMEMxOC42NywwLDEyLjI2NiwyLjY0OCw3LjQ1OCw3LjQ1OAoJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDAKCQkJYzYuODE2LDAsMTMuMjIxLTIuNjQ4LDE4LjAyOS03LjQ1OGM0LjgwOS00LjgwOSw3LjQ1Ny0xMS4yMTIsNy40NTctMTguMDNDNTAuOTc3LDE4LjY3LDQ4LjMyOCwxMi4yNjYsNDMuNTIsNy40NTh6CgkJCSBNNDIuMTA2LDQyLjEwNWMtNC40MzIsNC40MzEtMTAuMzMyLDYuODcyLTE2LjYxNSw2Ljg3MmgtMC4wMDJjLTYuMjg1LTAuMDAxLTEyLjE4Ny0yLjQ0MS0xNi42MTctNi44NzIKCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzIKCQkJYzQuNDMxLDQuNDMxLDYuODcxLDEwLjMzMiw2Ljg3MSwxNi42MTdDNDguOTc3LDMxLjc3Miw0Ni41MzYsMzcuNjc1LDQyLjEwNiw0Mi4xMDV6Ii8+CgkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik0yMy41NzgsMzIuMjE4Yy0wLjAyMy0xLjczNCwwLjE0My0zLjA1OSwwLjQ5Ni0zLjk3MmMwLjM1My0wLjkxMywxLjExLTEuOTk3LDIuMjcyLTMuMjUzCgkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUKCQkJYzAtMS4wOTYtMC4yNi0yLjA4OC0wLjc3OS0yLjk3OWMtMC41NjUtMC44NzktMS41MDEtMS4zMzYtMi44MDYtMS4zNjljLTEuODAyLDAuMDU3LTIuOTg1LDAuNjY3LTMuNTUsMS44MzIKCQkJYy0wLjMwMSwwLjUzNS0wLjUwMywxLjE0MS0wLjYwNywxLjgxNGMtMC4xMzksMC43MDctMC4yMDcsMS40MzItMC4yMDcsMi4xNzRoLTIuOTM3Yy0wLjA5MS0yLjIwOCwwLjQwNy00LjExNCwxLjQ5My01LjcxOQoJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQoJCQljMCwxLjE0Mi0wLjEzNywyLjExMS0wLjQxLDIuOTExYy0wLjMwOSwwLjg0NS0wLjczMSwxLjU5My0xLjI2OCwyLjI0M2MtMC40OTIsMC42NS0xLjA2OCwxLjMxOC0xLjczLDIuMDAyCgkJCWMtMC42NSwwLjY5Ny0xLjMxMywxLjQ3OS0xLjk4NywyLjM0NmMtMC4yMzksMC4zNzctMC40MjksMC43NzctMC41NjUsMS4xOTljLTAuMTYsMC45NTktMC4yMTcsMS45NTEtMC4xNzEsMi45NzkKCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}
.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}
.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}
.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-border-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0px;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-warn-color0);
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px 5px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FileDialog-Checkbox {
  margin-top: 35px;
  display: flex;
  flex-direction: row;
  align-items: end;
  width: 100%;
}

.jp-FileDialog-Checkbox > label {
  flex: 1 1 auto;
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
  overflow-x: auto;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 50px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -50px; margin-right: -50px;
  padding-bottom: 50px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 50px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
  outline: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -50px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .remote-caret {
  position: relative;
  border-left: 2px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .remote-caret > div {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -2px;
  font-size: 0.95em;
  background-color: rgb(250, 129, 0);
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 3;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .remote-caret.hide-name > div {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .remote-caret:hover > div {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
  margin: 8px 12px 0px 12px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: flex-start;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0px;
  padding-right: 2px;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 40px;
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent {
  width: 72px;
  background: var(--jp-brand-color1);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent:focus-visible {
  background-color: var(--jp-brand-color0);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent
  .jp-icon3 {
  fill: white;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileBrowser-filterBox {
  padding: 0px;
  flex: 0 0 auto;
  margin: 8px 12px 0px 12px;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing:focus-visible {
  border: 1px solid var(--jp-brand-color1);
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon:before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

body[data-format='mobile'] .jp-OutputArea-child {
  flex-direction: column;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-OutputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  margin-left: var(--jp-notebook-padding);
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}

body[data-format='mobile'] .jp-InputArea {
  flex-direction: column;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
  overflow: hidden;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

body[data-format='mobile'] .jp-InputArea-editor {
  margin-left: var(--jp-notebook-padding);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-InputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

.jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
}

.jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-collapseHeadingButton {
  display: none;
}

.jp-MarkdownCell:hover .jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  position: absolute;
  right: 0;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook-render * {
  contain: none !important;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
  float: left;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt:before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body div {
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

.highlight  {
  margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.CodeMirror pre {
  margin: 0;
  padding: 0;
}

/* Using table instead of flexbox so that we can use break-inside property */
/* CSS rules under this comment should not be required anymore after we move to the JupyterLab 4.0 CSS */


.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  min-width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-OutputArea-child {
  display: table;
  width: 100%;
}

.jp-OutputPrompt {
  display: table-cell;
  vertical-align: top;
  min-width: var(--jp-cell-prompt-width);
}

body[data-format='mobile'] .jp-OutputPrompt {
  display: table-row;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  display: table-row;
}

.jp-OutputArea-output.jp-OutputArea-executeResult {
  width: 100%;
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }

  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}
</style>

<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: { 
                    automatic: true 
                    }
                }
            });
        
            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Packages used to create radar charts</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">mplsoccer</span> <span class="kn">import</span> <span class="n">Radar</span><span class="p">,</span> <span class="n">FontManager</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Load csv file from the same folder</span>
<span class="n">central_mids</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;Central mids.csv&quot;</span><span class="p">,</span> <span class="n">delimiter</span> <span class="o">=</span> <span class="s1">&#39;;&#39;</span><span class="p">)</span>

<span class="c1"># Drop non-stats columns</span>
<span class="n">central_mids_stats</span> <span class="o">=</span> <span class="n">central_mids</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Player&#39;</span><span class="p">,</span> <span class="s1">&#39;Pos&#39;</span><span class="p">,</span> <span class="s1">&#39;Squad&#39;</span><span class="p">,</span> <span class="s1">&#39;Min&#39;</span><span class="p">],</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Expected Assists</th>
      <th>Passes Completed %</th>
      <th>Completed Passes into Final third</th>
      <th>Yards Progressed From Passes</th>
      <th>Shot-Created Dribbles</th>
      <th>Successful Dribbles</th>
      <th>Successful Dribbles %</th>
      <th>Successful Pressures</th>
      <th>Interceptions</th>
      <th>Tackles Won</th>
      <th>Fouls Made</th>
      <th>Aerial Duels Won %</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.09</td>
      <td>79.6</td>
      <td>2.52</td>
      <td>312.2</td>
      <td>0.11</td>
      <td>0.92</td>
      <td>54.2</td>
      <td>3.98</td>
      <td>0.97</td>
      <td>1.29</td>
      <td>1.32</td>
      <td>34.3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.04</td>
      <td>76.8</td>
      <td>2.25</td>
      <td>258.7</td>
      <td>0.00</td>
      <td>0.17</td>
      <td>71.4</td>
      <td>4.26</td>
      <td>1.07</td>
      <td>1.49</td>
      <td>1.00</td>
      <td>38.6</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Setting up to draw the radar</span>
<span class="k">def</span> <span class="nf">radar_mosaic</span><span class="p">(</span><span class="n">radar_height</span><span class="o">=</span><span class="mf">0.915</span><span class="p">,</span> <span class="n">title_height</span><span class="o">=</span><span class="mf">0.06</span><span class="p">,</span> <span class="n">figheight</span><span class="o">=</span><span class="mi">14</span><span class="p">):</span>
   
    <span class="n">endnote_height</span> <span class="o">=</span> <span class="mi">1</span> <span class="o">-</span> <span class="n">title_height</span> <span class="o">-</span> <span class="n">radar_height</span> <span class="c1"># Determine the height of the end note</span>
    <span class="n">figwidth</span> <span class="o">=</span> <span class="n">figheight</span> <span class="o">*</span> <span class="n">radar_height</span> <span class="c1"># Determine the width of the radar</span>
    <span class="n">figure</span><span class="p">,</span> <span class="n">axes</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplot_mosaic</span><span class="p">([[</span><span class="s1">&#39;title&#39;</span><span class="p">],</span> <span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">],</span> <span class="p">[</span><span class="s1">&#39;endnote&#39;</span><span class="p">]],</span>
                                      <span class="n">gridspec_kw</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;height_ratios&#39;</span><span class="p">:</span> <span class="p">[</span><span class="n">title_height</span><span class="p">,</span> <span class="n">radar_height</span><span class="p">,</span>
                                                                     <span class="n">endnote_height</span><span class="p">],</span>
                                                   <span class="s1">&#39;bottom&#39;</span><span class="p">:</span> <span class="mi">0</span><span class="p">,</span> <span class="s1">&#39;left&#39;</span><span class="p">:</span> <span class="mi">0</span><span class="p">,</span> <span class="s1">&#39;top&#39;</span><span class="p">:</span> <span class="mi">1</span><span class="p">,</span>
                                                   <span class="s1">&#39;right&#39;</span><span class="p">:</span> <span class="mi">1</span><span class="p">,</span> <span class="s1">&#39;hspace&#39;</span><span class="p">:</span> <span class="mi">0</span><span class="p">},</span>
                                      <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="n">figwidth</span><span class="p">,</span> <span class="n">figheight</span><span class="p">))</span>
    <span class="n">axes</span><span class="p">[</span><span class="s1">&#39;title&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;off&#39;</span><span class="p">)</span>
    <span class="n">axes</span><span class="p">[</span><span class="s1">&#39;endnote&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;off&#39;</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">figure</span><span class="p">,</span> <span class="n">axes</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the stats parameters from the column names</span>
<span class="n">cm_params</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">central_mids</span><span class="o">.</span><span class="n">columns</span><span class="p">)</span>
<span class="n">cm_params</span> <span class="o">=</span> <span class="n">cm_params</span><span class="p">[</span><span class="mi">4</span><span class="p">:]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[&nbsp;]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[&#39;Expected Assists&#39;,
 &#39;Passes Completed %&#39;,
 &#39;Completed Passes into Final third&#39;,
 &#39;Yards Progressed From Passes&#39;,
 &#39;Shot-Created Dribbles&#39;,
 &#39;Successful Dribbles&#39;,
 &#39;Successful Dribbles %&#39;,
 &#39;Successful Pressures&#39;,
 &#39;Interceptions&#39;,
 &#39;Tackles Won&#39;,
 &#39;Fouls Made&#39;,
 &#39;Aerial Duels Won %&#39;]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">low</span> <span class="o">=</span> <span class="p">[</span><span class="mf">0.01</span><span class="p">,</span> <span class="mf">59.5</span><span class="p">,</span> <span class="mf">0.48</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mf">0.03</span><span class="p">,</span> <span class="mf">0.12</span><span class="p">,</span> <span class="mi">20</span><span class="p">,</span> <span class="mf">1.65</span><span class="p">,</span> <span class="mf">0.46</span><span class="p">,</span> <span class="mf">0.21</span><span class="p">,</span> <span class="mf">3.33</span><span class="p">,</span> <span class="mi">0</span><span class="p">]</span> <span class="c1"># Create a list of lower boundaries</span>

<span class="n">high</span> <span class="o">=</span> <span class="p">[</span><span class="mf">0.3</span><span class="p">,</span> <span class="mf">91.3</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mf">578.6</span><span class="p">,</span> <span class="mf">0.95</span><span class="p">,</span> <span class="mf">3.34</span><span class="p">,</span> <span class="mi">100</span><span class="p">,</span> <span class="mf">6.93</span><span class="p">,</span> <span class="mf">3.13</span><span class="p">,</span> <span class="mf">3.24</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">80</span><span class="p">]</span> <span class="c1"># Create a list of higher boundaries</span>

<span class="c1"># Create two empty lists to store the player&#39;s stats</span>
<span class="n">a_values</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">b_values</span> <span class="o">=</span> <span class="p">[]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get the stats for each player from the csv file</span>
<span class="k">for</span> <span class="n">x</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">central_mids</span><span class="p">[</span><span class="s1">&#39;Player&#39;</span><span class="p">])):</span>
    <span class="k">if</span> <span class="n">central_mids</span><span class="p">[</span><span class="s1">&#39;Player&#39;</span><span class="p">][</span><span class="n">x</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Romain Perraud&#39;</span><span class="p">:</span>
        <span class="n">a_values</span> <span class="o">=</span> <span class="n">central_mids</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="n">x</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">()</span>
    <span class="k">if</span> <span class="n">central_mids</span><span class="p">[</span><span class="s1">&#39;Player&#39;</span><span class="p">][</span><span class="n">x</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Ryan Bertrand&#39;</span><span class="p">:</span>
        <span class="n">b_values</span> <span class="o">=</span> <span class="n">central_mids</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="n">x</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">tolist</span><span class="p">()</span>

<span class="c1"># Drop the non-stats columns (usually player&#39;s info)</span>
<span class="n">a_values</span> <span class="o">=</span> <span class="n">a_values</span><span class="p">[</span><span class="mi">4</span><span class="p">:]</span>
<span class="n">b_values</span> <span class="o">=</span> <span class="n">b_values</span><span class="p">[</span><span class="mi">4</span><span class="p">:]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Load some fonts using mplsoccer&#39;s FontManager package</span>
<span class="n">URL1</span> <span class="o">=</span> <span class="s1">&#39;https://github.com/googlefonts/roboto/blob/main/src/hinted/Roboto-Thin.ttf?raw=true&#39;</span>
<span class="n">robotto_thin</span> <span class="o">=</span> <span class="n">FontManager</span><span class="p">(</span><span class="n">URL1</span><span class="p">)</span>
<span class="n">URL2</span> <span class="o">=</span> <span class="s1">&#39;https://github.com/googlefonts/roboto/blob/main/src/hinted/Roboto-Regular.ttf?raw=true&#39;</span>
<span class="n">robotto_regular</span> <span class="o">=</span> <span class="n">FontManager</span><span class="p">(</span><span class="n">URL2</span><span class="p">)</span>
<span class="n">URL3</span> <span class="o">=</span> <span class="s1">&#39;https://github.com/googlefonts/roboto/blob/main/src/hinted/Roboto-Bold.ttf?raw=true&#39;</span>
<span class="n">robotto_bold</span> <span class="o">=</span> <span class="n">FontManager</span><span class="p">(</span><span class="n">URL3</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Draw the radar with the created arrays of data</span>
<span class="n">radar</span> <span class="o">=</span> <span class="n">Radar</span><span class="p">(</span><span class="n">cm_params</span><span class="p">,</span> <span class="n">low</span><span class="p">,</span> <span class="n">high</span><span class="p">,</span>
                      <span class="c1"># Round values to integer or keep them as float values</span>
                      <span class="n">round_int</span> <span class="o">=</span> <span class="p">[</span><span class="kc">False</span><span class="p">]</span> <span class="o">*</span> <span class="mi">12</span><span class="p">,</span>
                      <span class="n">num_rings</span> <span class="o">=</span> <span class="mi">6</span><span class="p">,</span>  <span class="c1"># The number of concentric circles (excluding center circle)</span>
                      <span class="n">ring_width</span> <span class="o">=</span> <span class="mf">0.65</span><span class="p">,</span> <span class="n">center_circle_radius</span> <span class="o">=</span> <span class="mf">0.5</span><span class="p">)</span>

<span class="c1"># Call radar_mosaic function to setup the radar</span>
<span class="n">fig</span><span class="p">,</span> <span class="n">axs</span> <span class="o">=</span> <span class="n">radar_mosaic</span><span class="p">(</span><span class="n">radar_height</span> <span class="o">=</span> <span class="mf">0.8</span><span class="p">,</span> <span class="n">title_height</span> <span class="o">=</span> <span class="mf">0.07</span><span class="p">,</span> <span class="n">figheight</span> <span class="o">=</span> <span class="mi">13</span><span class="p">)</span>

<span class="n">radar</span><span class="o">.</span><span class="n">setup_axis</span><span class="p">(</span><span class="n">ax</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">])</span> <span class="c1"># Setup an axis to draw the radar</span>
<span class="n">rings_inner</span> <span class="o">=</span> <span class="n">radar</span><span class="o">.</span><span class="n">draw_circles</span><span class="p">(</span><span class="n">ax</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">],</span> <span class="n">facecolor</span> <span class="o">=</span> <span class="s1">&#39;#b7b7b7&#39;</span><span class="p">,</span> <span class="n">edgecolor</span> <span class="o">=</span> <span class="s1">&#39;#b7b7b7&#39;</span><span class="p">)</span> <span class="c1"># Draw inner circles</span>
<span class="c1"># Call the draw_radar_compare from mplsoccer package</span>
<span class="n">radar_output</span> <span class="o">=</span> <span class="n">radar</span><span class="o">.</span><span class="n">draw_radar_compare</span><span class="p">(</span><span class="n">a_values</span><span class="p">,</span> <span class="n">b_values</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">],</span>
                                        <span class="n">kwargs_radar</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;facecolor&#39;</span><span class="p">:</span> <span class="s1">&#39;#f72516&#39;</span><span class="p">,</span> <span class="s1">&#39;alpha&#39;</span><span class="p">:</span> <span class="mf">0.6</span><span class="p">},</span> <span class="c1"># Set the facecolor and the transparency of the first radar</span>
                                        <span class="n">kwargs_compare</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;facecolor&#39;</span><span class="p">:</span> <span class="s1">&#39;#273e8a&#39;</span><span class="p">,</span> <span class="s1">&#39;alpha&#39;</span><span class="p">:</span> <span class="mf">0.6</span><span class="p">})</span> <span class="c1"># Set the facecolor and the transparency of the second radar</span>
<span class="n">radar_poly</span><span class="p">,</span> <span class="n">rings_outer</span><span class="p">,</span> <span class="n">vertices1</span><span class="p">,</span> <span class="n">vertices2</span> <span class="o">=</span> <span class="n">radar_output</span>
<span class="n">range_labels</span> <span class="o">=</span> <span class="n">radar</span><span class="o">.</span><span class="n">draw_range_labels</span><span class="p">(</span><span class="n">ax</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">],</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">18</span><span class="p">,</span> 
                                        <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_thin</span><span class="o">.</span><span class="n">prop</span><span class="p">)</span> <span class="c1"># Set the necessary properties for the radar&#39;s ranges</span>
<span class="n">param_labels</span> <span class="o">=</span> <span class="n">radar</span><span class="o">.</span><span class="n">draw_param_labels</span><span class="p">(</span><span class="n">ax</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;radar&#39;</span><span class="p">],</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">17</span><span class="p">,</span> 
                                        <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_regular</span><span class="o">.</span><span class="n">prop</span><span class="p">)</span> <span class="c1"># Set the necessary properties for the radar&#39;s parameters</span>

<span class="n">endnote1_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;endnote&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.99</span><span class="p">,</span> <span class="mf">0.35</span><span class="p">,</span> <span class="s1">&#39;Created by @dgouilard</span><span class="se">\n</span><span class="s1">Data via FBRef / Statsbomb&#39;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">15</span><span class="p">,</span>
                                           <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_regular</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span> <span class="n">ha</span> <span class="o">=</span> <span class="s1">&#39;right&#39;</span><span class="p">,</span> <span class="n">va</span> <span class="o">=</span> <span class="s1">&#39;center&#39;</span><span class="p">)</span> <span class="c1"># Add creator details and data source at the end</span>
<span class="n">title1_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;title&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.01</span><span class="p">,</span> <span class="mf">0.65</span><span class="p">,</span> <span class="s2">&quot;Romain Perraud&quot;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">25</span><span class="p">,</span> <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_bold</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span> 
                                <span class="n">ha</span> <span class="o">=</span> <span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">va</span> <span class="o">=</span> <span class="s1">&#39;center&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s2">&quot;#f72516&quot;</span><span class="p">)</span> <span class="c1"># Set the properties for the first player</span>
<span class="n">title2_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;title&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.01</span><span class="p">,</span> <span class="mf">0.25</span><span class="p">,</span> <span class="s2">&quot;Stade Brestois&quot;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">20</span><span class="p">,</span> <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_regular</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span>
                                <span class="n">ha</span> <span class="o">=</span> <span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">va</span> <span class="o">=</span> <span class="s1">&#39;center&#39;</span><span class="p">)</span>
<span class="n">title3_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;title&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.99</span><span class="p">,</span> <span class="mf">0.65</span><span class="p">,</span> <span class="s1">&#39;Ryan Bertrand&#39;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">25</span><span class="p">,</span> <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_bold</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span>
                                <span class="n">ha</span><span class="o">=</span><span class="s1">&#39;right&#39;</span><span class="p">,</span> <span class="n">va</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s2">&quot;#273e8a&quot;</span><span class="p">)</span> <span class="c1"># Set the properties for the second player</span>
<span class="n">title4_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;title&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.99</span><span class="p">,</span> <span class="mf">0.25</span><span class="p">,</span> <span class="s1">&#39;Southampton FC&#39;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">20</span><span class="p">,</span> 
                                <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_regular</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span> <span class="n">ha</span><span class="o">=</span><span class="s1">&#39;right&#39;</span><span class="p">,</span> <span class="n">va</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>
<span class="n">endnote2_text</span> <span class="o">=</span> <span class="n">axs</span><span class="p">[</span><span class="s1">&#39;endnote&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">text</span><span class="p">(</span><span class="mf">0.01</span><span class="p">,</span> <span class="mf">0.35</span><span class="p">,</span> <span class="s1">&#39;Template: vs Big 5 European Leagues Full Backs </span><span class="se">\n</span><span class="s1">All stats are per 90 minutes&#39;</span><span class="p">,</span> 
                                    <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">15</span><span class="p">,</span> <span class="n">fontproperties</span> <span class="o">=</span> <span class="n">robotto_regular</span><span class="o">.</span><span class="n">prop</span><span class="p">,</span> <span class="n">ha</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">va</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span> <span class="c1"># Radar&#39;s name</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_facecolor</span><span class="p">(</span><span class="s2">&quot;#ffffff&quot;</span><span class="p">)</span> <span class="c1"># Set the background colour of the figure</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_figwidth</span><span class="p">(</span><span class="mi">13</span><span class="p">)</span> <span class="c1"># Set the width of the figure</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_figheight</span><span class="p">(</span><span class="mi">13</span><span class="p">)</span> <span class="c1"># Set the height of the figure</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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xAR+fn4oV64chg4dimHDhuHrr79G1apVOahljH109OuGZ88Uf+HCBSxfvhwVK1YUMxDr59wuXboUAPDpp58CyMqpsGzZMnh5eeHChQs4fPgwPDw8xOkdwPP37OPHj2PFihVv3DZfX180adLEICBVq9XQ6XSwsbHBt99+i0uXLsHOzg7ffvstVCoVqlevjsjISAwdOhTnz59H9erVodPp4Ofnh40bNwJ4v6HSjLFioBASVjHGCpFOp8s1S/Gff/5J5ubmZG1tTcHBwUT0PJvxwoULycLCgubOnUtERCkpKeTh4UEmJibUoEEDsre3p5YtW75zNs3sWYvVajWdP3+eUlNTc92em3bt2olte/LkCW3atIn69u1L33333Tu1hzHGiqOYmBgaNmwYbdu2jYiev7cePnyY5HK5+D4aGRlJHTp0IDc3N0pISKCMjAyKjo6mgQMHkqurq0GWYq1WSx06dCCFQkGnT59+57b9/fff5OTkRDt37iS1Wi2WHz9+nDZt2kRERLdu3SJBEGjFihVERJSYmEg9evSghg0bklarfedzM8aKBw5sGfuIZP/Dn5CQQAEBAZSSkiKWjRw5kkxMTGj37t1ERJSRkSFuq1GjBlWuXJnOnj1LRERXrlyhH3/8kQYPHky///77O7VHp9MZBK0rVqwgZ2dnsrGxodq1a4vLQLzqgSUjI4OWLFlCR44cMdiPH3IYY+z1nj59Si1atKDKlStTaGgo6XQ6WrduHUkkElq5cqXBvseOHSNBEAyW6Fm3bh2VKFGCRo8e/V7tiI2NpW7dupGlpSV9+eWX9P333xucR2/w4MHUtGlTioiIICKixYsXk5GREV27du29zs8YK/oEIh63wdjHZs6cOVi+fDkUCgUUCgVGjRqFSZMm4caNG+jevTucnJzw999/w8TEBJmZmVAoFNi9ezeGDRuGXr16YenSpXmajCkyMhInT57EggUL0LVrV6hUKqxatQpqtRrHjx+Hq6srtFptrglSAODhw4coUaIElEplnrWJMcaKG32G+ew2btyIgQMHYv369ejfvz/u37+PXr16QaVS4d9//4WxsbG478GDB9GmTRssXboUY8aMQXR0NLp27YrY2Fjs3LkT3t7euZ7jbaxfv178++Ti4oI1a9bg7t272L17N6ZNm4br16+jX79+sLS0xJ49eyAIAn7++WfMmzfvnc/J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YDQaCQwMZNOmTeL1Zg6dkslkYnVkpVJJRUUFSqVSXET7+vpKzeklJK4AR0dHxowZ0+pz5vlJEAQEQSA7O5uCggL69u2Lq6srDQ0NrFixgpEjRzJjxgwUCoVNRi516tQJQRBsJufWaDRy5swZvLy8cHd3t7Q514wePXoAzXms/+///T/8/f0B2L9/P19++SU7d+7EwcGBRx99lKefflpc/11MjB45coTVq1eL151erxdTsLp16yZu8k6fPv2C45gjmL799luWLVvGBx98wL333svNN99MbGysmNKze/dusrKyyMvLIyEhgbfffhudTicJWyvDNleTEpeMIAjiDUqhUODp6cnp06fRarX8+9//5v333+fbb79lzZo1PP/887i5uVFeXm5hqzsmp0+fpqGhwSZyP8wtffr372+Tng0z5mqsgiBw0003UV1dzc6dOyksLKRnz54IgkB6ejo1NTWcPXsW+KutQnp6Ohs2bJAaz0tIXEN++eUX9Hp9i3nZaDSi0Wg4cOAACxcuZM+ePfTp04eYmBh8fHyAixfRsVaCg4NtqlqyyWQiOTkZvV5vaVOuGX5+fmzcuJEPPvgAf39/zp49y0svvcRDDz3E9u3bufnmm1m1ahVvv/02AQEBmEymFpX82yI3N5fu3btzyy23APDAAw/w+++/A805s8nJyZdUeM28keTt7c0zzzwjhh/LZDK8vb3Jyspi+vTpjBw5EqVSyciRIzl06BAjRoyw6g0JW0Xy2Eq0SXp6Ot27dxe9RHZ2dowZM4annnoKJycnevfuzRtvvMG4ceMwmUw4ODig0+nEfAmJS6e8vJy8vDyb2OWWy+W4uLjYvKg1c++996LVajl58iQFBQXiokAmkxEfH8+OHTsYO3YsR44coby8HC8vL44cOYJKpWL06NHi7rmEhET7Yb4GPT09W/TTNnuhysvLqa6u5tSpU0RFRUkF2s4hJCQEQRA4deqUTdzTDAYDx48fp2/fvla7oREREYFWq+WLL77g559/Jisri5iYGObMmcP48ePF111OvmpISAhFRUWUlJQQFhZGbGwsjo6ObN26lYCAAEJCQlqkBFyIc793V1dXoPl3eeutt/jggw9wc3PjjTfe4O6778bBwYF33nmHkpIS/P39rfY3s1WkHFuJVjl8+DAJCQncc889fPzxx3Tq1AmA0tJSNmzYQGlpKXfd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ykEVbieLf/zjHyFhIUEQqKiowG638+Uvfzm0TVpaGmVlZezevZt3332Xc845J4IWB6iqqmLTpk3MmjWL8847T3NrnHDY7XauuOKKfudxUlISF1988ZDHvaqqKjTf1u12s2XLFu69914ALrroIn73u98NacNtt93GX//6V770pS/hcDj42c9+RlFREUuXLuWxxx4jIyODH/zgB6P8C89MtH9mxpjShMvYbtq0KeKzvTZs2MC6desGLBXS2k1fluV+8wt37drFggULImjV0AiCMOZjnRhvoqw4jUMVzWOzJS4OLFZUl3PQ7RRV1WaPrQrCQEM7oxQVjR7riUINZFy05NgKgoggCqhy3x/ycP3BsGXHkhj5vy0/tZAjDYfJ9eZTmlPK5nYD+7v1XJzeQ6k1EGhZmJXBwqwM9ja38Pgne/jmwrmj/j61uRH5b39CyMlDPO8ihJJpo3Zwh6NCffbZZ7Nx40Y++9nPjuo7xot9+/Zx5MgRvvGNbzBjxgyKiooG3Pa3v/0tHR0drF69ehIt7M/+/fv7KObu2LFjwBLq+fPn8+c//3kyzRuQoAN35MgRfvnLX1JcXMyVV16pubVOb8aaEU9JSQllst9++21EUQwdpz179gxL/OvFF1/kwQcf5D/+4z8ASE9P53e/+x3f+MY3+PGPf8xTTz0Vc2xHSKwUOYI8/vjj/PjHPwagp6eHb33rW8yfP58777xTk/2OY+H3v/89v/jFL3jooYd44IEHeOGFF4Dw5bG1tbWTbV4/jh8/zoYNG3jllVdob2/v9340Da/vzT/+8Q8eeOABHnzwQR544IGQQqPf7++3EDp8+HAkTOzHb3/720FtGY9F+qK541CODJAevr/P5enl7A6Qsd1fs3d8bBglW45swuF2DLqNoLEaakVWtFn2PYForedYEkVEof9Spbkr/JgUMQocWwFYUrKMTmc7h2oDZbudPoFn6iz8vcGMw3/qpJyTnka9Y/DrbriodTXIT/0f8hP/i1JdNap9DOd+mpSURFdX16j2P558/PHHXHHFFWHH/ZzOd7/7Xd54441JsmxggsH64HEeKgARbX22M2fO5KabbmLFihX89re/5Xe/+x2dnZ2RNmvU9PT08N57743qsxdddBH33nsvDz30EDfffDOXXXYZRqORxx57jLvvvpurrrpqyH04nc4+vdaf/exnQ7OjFy9e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ox8dbKuqBoSzxWq10tjYOGjb4cOHeeCBB9i+fTuf/OQnfdvPnz8/pMDxFyaTadh1wsc+9jE6Ojr4j//4D5YsWcKWLVum2brBmM1mWltbh7zP7t69m/nz5w/aFijrn1tuuYWXX36Z06dPc99995GUlERtbS27d+8mMzPzmmaZgTAqcCzce++9AOTk5PDWW2+N67WbN2/m3XffHbJR6Pvvvz+mY23+/Pn85je/YfHixfzoRz9i0aJFxMfHU1JSwr/8y7+wfPnycdmkowvbaSUhIWFI75uqqgwMDLB161afl0uSJGprR551ORsQOWIbiPU9I2E2mwPGOzweZFnG4XAII2wBUpNj2bTCxsnzHVy41DOh91CNJnqSUrG2NGLq7ppkC4fHWz8u4rECYDKbcLldMz4l2WZwsjlJEfYaCmC328e0sHebTB+O3fHMkXVERE67kL0STdOIiooatO2BBx7g0KFD/Ou//isf/ehHWbBgAVVVVfz3f/83n/vc5/xk6WW+9KUvcf/99zN37lwSEhK4ePEi3d3d3H777URERPDUU0/5rrHR0dHXjLjzB88//zyaphEcHOxrwHX1dcl7/BgMBnbs2OF3Yfutb32LH//4xzQ3N5OWlkZERATNzc2cPHmSrKysa6L6gXSdveOOO0hISKClpYXDhw+TnJzMN77xDZ8TR0R+9atf8c477/Diiy8CHufC3r17ufHGG1m2bNmIry0oKOCxxx6jra1t0FivlpYW/uu//ovPfvazfO973wM8x+G//Mu/XPMe3/3ud9m6dSt/+ctfkCSJF154AYCvfe1r1NbW8uSTT07SN5096ON+ppEHH3xwXBep3//+91NojRg4nU52794tXJRIxBmGnZ2dHD58WLholsFgYN68eQEVQRgNTdN4++23cbvd1DXZOXiqHefAxC/Fpq4OrC1NSNN0OTeZzRgFSrO/GrfbHRBRsqlCAu6Pa6MwMYLAWRaPD03TqK2tHVLYui2WyzNkbXEeIRtAAuC5557jxz/+8ZDXJE3T2LlzJ2fPniUpKYlbb701YDK13nrrLYqLi2ltbSU1NZXExER/mzQmkpKSePPNN/m7v/s7f5syZl544QVKS0vp6+sjPDycvLy8IUs82trarnGS+JOcnByysrL8bcak8Nvf/paHH36Ye++9lz/+8Y/s2rWLLVu2oGkaiqKwfft2br75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EhHRF+H48ePw8vKCnZ0d1Go1KlSogMWLFyM9Pf1zN+1vde/ePXTo0AEFChTAgQMH0K5duxznrVOnDqpWrfo3to6IiOifwcCWiIjyvK1bt6J27dowMzPD0qVLsXXrVjRt2hSjRo1C3759P3fz/lYnTpzAs2fPMGvWLHh6eqJw4cKfu0lERET/OL3P3QAiIqJP9cMPP6BSpUrYuHGjss3Lyws2NjYYOnQoRowYgdKlS3/GFv594uPjAQCWlpafuSVERESfD+/YEhFRnvf8+XOYmZll2t62bVt8//33AABnZ2d06tRJa7+fnx9UKhUiIiKUbTExMejUqROsrKxgbm6O+vXr49SpU1r5zp8/j2bNmiF//vywsrJCixYtEB4erpUmNDQUjRs3hqmpKaysrNC3b188ffpU2S8imDdvHooXLw61Wo1ixYphxowZSEtLU9I8efIEgwYNgoODA0xMTODh4YEtW7Yo+52dnfH1118DAAoXLgyVSgUACAwMhEqlwt69e7XaxKHHRET0pWJgS0REeV7btm1x4MABfP/990hMTFS2FyxYENOnT8/x3dqHDx+iWrVqOH/+PObPn481a9ZARODp6YmQkBAAQEREBGrUqIHExET8+uuvWLZsGWJjY1GtWjXExsYCeB3U1qxZE69evcK6deswa9Ys7NixA23btlXqmjdvHkaNGoUePXpg27Zt6NSpEyZOnIhJkyYpabp3744//vgDPj4+2LJlC5ydndG+fXvs378fALB582aMGjUKAPDHH3/g2LFjn3QeiYiI8ioORSYiojxv0qRJiI+Px8yZMzFnzhw0aNAA7dq1Q+fOnWFkZJTjcubMmYOEhASEhISgYMGCAIAGDRqgcOHCWL58OTw8PDB58mRoNBocOHAAarUaAFCrVi0ULFgQ69atw9ixYzF69GjY2Nhgz549Sv0WFhZo06YNzp49i4oVK2L37t0oV66ccke5YcOGEBFlaLGIYO/evRg8eDB69eqltKVdu3a4fv06GjVqBA8PDyXg9vDwgLOzc66cTyIioryGd2yJiCjP09fXx5IlS3Dt2jWMGzcOt2/fRu/evVGkSBEEBgbmuJzDhw+jcuXKSlALAMbGxggODsbEiROVNI0bN1aCWgCwsbFBREQEevfujeTkZAQGBqJ169bQ09NDamoqUlNTUa1aNQBQhjXXqlUL58+fx8iR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HOzs7NCjRw/4+Pi8t91v171x40b069cPGzduRN26dfHjjz9+xNkgIiL691EJxyERERERERFRHsY5tkRERERERJSnMbAlIiIiIiKiPI2BLREREREREeVpDGyJiIiIiIgoT2NgS0RERERERHkaA1siIiIiIiLK0xjYEhERERERUZ7GwJaIiIiIiIjyNAa2RERERERElKcxsCUiIiIiIqI8jYEtERERERER5WkMbImIiIiIiChPY2BLREREREREeRoDWyIiIiIiIsrTGNgSERERERFRnsbAloiIiIiIiPI0BrZERERERESUpzGwJSIiIiIiojyNgS0RERERERHlaQxsiYiIiIiIKE9jYEtERERERER5GgNbIiIiIiIiytMY2BIREREREVGexsCWiIiIiIiI8jQGtkRERERERJSnMbAlIiIiIiKiPI2BLREREREREeVpDGyJiIiIiIgoT2NgS0RERERERHkaA1siIiIiIiLK0xjYEhERERERUZ7GwJaIiIiIiIjyNAa2RERERERElKcxsCUiIiIiIqI8jYEtERERERER5WkMbImIiIiIiChPY2BLREREREREeRoDWyIiIiIiIsrTGNgSERERERFRnsbAloiIiIiIiPI0BrZERERERESUpzGwJSIiIiIiojyNgS0RERERERHlaQxsiYiIiIiIKE9jYEtERERERER5GgNbIiIiIiIiytMY2BIREREREVGexsCWiIiIiIiI8jQGtkRERERERJSn5Upg27NnT6hUqmxfPXv2zI1qPsqUKVNQtGjRz1Z/bqpTp45yTnV0dFCgQAF07NgRMTExSpr//Oc/8PDw+KR6GjdunOkaZldmYGBgttd96dKln9SOvKZnz55o0KDB527GP2bKlCnZXvvExMT35o+JiYFKpcLx48eV8t71t/pm+fr6+ihSpAhGjx6NZ8+e5dYhQaVSYe3atblWHhER0ZcqKioKnTt3hrW1NczNzVG7dm0cPnz4czcrR/z8/KCnp5flvoy+7e3bt3O1zpSUFPj6+qJGjRqwtLSEubk5KlasiAULFuDFixef1Oa/y7Bhw9C2bVvl/d/RT8rN850rZ2fBggWYOXMmACAoKAht27ZFaGgo7O3tAQDGxsa5Uc0/Yu3atejevTtE5HM3JUtdunTB3LlzISK4c+cORo8ejRYtWiAsLAy6uroYPnw4Bg0a9El1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"
class="
"
>
</div>

</div>

</div>

</div>

</div>
</body>







</html>
