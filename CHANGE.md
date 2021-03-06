Version 2.8.0
=============
**Date:** 16-Dec-2014

1. (bug #167): Fix Yii message parsing for Html5Input '$this->noSupport'.
2. (enh #168): Prevent user to rapidly toggle and break the expand row before expansion or collapse.
3. (enh #169): Enable itemsBefore and itemsAfter to be added for export dropdown menu.

Version 2.7.0
=============
**Date:** 02-Dec-2014

1. (enh #150): New `ExpandRowColumn` added - allows to expand grid rows, show details, and load content via ajax.
2. (enh #152): Included `prepend` and `append` settings within `pageSummaryOptions` to prepend/append content to page summary.
3. (enh #154): Trap alert confirm dialog to allow export even after being hidden by browser **do not show** option.
4. (enh #156): Separate all JS / CSS assets and load only if the relevant functionality is needed.
5. (enh #157): Recursively replace/merge PDF export configuration correctly.
6. (enh #158): Include demo messages for auto generating via config.

Version 2.6.0
=============
**Date:** 19-Nov-2014

1. (enh #139): German translations updated.
2. (enh #140): French translations added.
3. (bug #141): Enhance EditableColumn to have unique attribute input ids yet the same name.
4. (bug #142): Fix missing headers in export, due to improper floatThead settings.
5. (bug #143): Ability to disable / hide GridView panel footer. 
6. (enh #144): Revamp templates to easily configure different parts of the grid panel layout. (_BC breaking change_).
7. (enh #145): Enhance style to enable floated header wrapper tables to autofit/expand inside panel.

#### BC Breaking Changes

1. Removed `showFooter` from `panel` array configuration. This can be now configured with `footer` option within the `panel`.
2. Removed `layout` from `panel` array configuration. This can be now configured with `panelTemplate` at the GridView level.
3. Renamed `beforeTemplate` property to `panelBeforeTemplate`.
4. Renamed `afterTemplate` property to `panelAfterTemplate`.
5. Renamed `beforeContent` tag used in `panelBeforeTemplate` to `before`.
6. Renamed `afterContent` tag to `panelAfterTemplate` to `after`.
7. EditableColumn attribute naming convention has changed. Developers do not need to use `Model::loadMultiple` method anymore and have the ability to directly use the `$model->load` method.

#### Additions
1. Templates have been simplified and consolidated to the following configurable properties:
    - `panelTemplate`: Template to render the complete grid panel.
    - `panelHeadingTemplate`: Template to render the heading block part of the panel.
    - `panelBeforeTemplate`: Template to render the before block part of the panel.
    - `panelAfterTemplate`: Template to render the after block part of the panel.
    - `panelFooterTemplate`: Template to render the footer block part of the panel.
2. The `heading`, `footer`, `before`, and `after` properties in the `panel` typically accepts a string to render in that particular block. All of these can be set to boolean `false` to hide them.
3. HTML attributes for each of the above containers are now configurable i.e via `headingOptions`, `footerOptions`, `beforeOptions`, and `afterOptions` properties in the `panel` array configuration.
4. Vast enhancements to CSS styling when using Float Table Header wrapper. This now ensures tables auto fits and expand rightly to fit inside the panel.

Version 2.5.0
=============
**Date:** 17-Nov-2014

1. (bug #135): Upgrade to latest release of floatTHeader plugin.
2. (bug #136): Fix IE specific errors in floatHeader when columns are hidden.

Version 2.4.0
=============
**Date:** 14-Nov-2014

1. (bug #132): Correct page summary calculation.
2. (bug #133): Skip mPDF dependency when export is set to false.

Version 2.3.0
=============
**Date:** 07-Nov-2014

1. (bug #87): Fix key as object in mongodb.
2. (enh #116): Vietnamese translations added.
3. (enh #121): Portugese translations added.
4. (enh #122): Hungarian translations added.
5. (enh #127): Enhance dependency validation and ability to install optional packages.
6. (bug #131): Fix missing `options` in `toggleDataOptions` initialization.
7. First stable release

Version 2.2.0
=============
**Date:** 04-Nov-2014

1. (enh #110): Various export functionality enhancements):
    - Add a separate export popup progress window.
    - Setup a confirmation prompt to allow user to confirm if file is to be downloaded.
    - Separate `messages` configuration for all export related notifications.
    - Asynchronous export process on the separate window - and avoid any grid refresh
    - Set export mime types to be configurable
    - Add support for exporting new file types):
        - JSON export 
        - PDF export (using `yii2-mpdf` extension)
    - Add functionality for full data export
    - Enhance icons formatting for export file types (and beautify optionally using font awesome)
2. (enh #112): Toggle data button to allow toggling between **all data** and **paginated data**.
3. (enh #113): Enhance the PDF export generation method to allow generation of formatted reports.
4. (enh #114): Add `hiddenFromExport` property for all grid columns.
5. (enh #115): Add ability to plugin `yii2-export` extension for full grid data export.
6. (bug #118): Validate if `toggleGridData` is used in the extension.
7. (enh #121): Portugese translations.
8. (enh #122): Hungarian translations.

Version 2.1.0
=============
**Date:** 25-Oct-2014

1. (enh #94): Enhance and revamp toolbar.
2. (enh #95): Enhance export button dropdown feature.
3. (enh #96): Grid Plugins): Add ability to replace tags in gridview rendered layout.
4. (enh #99): Grid Export Plugins): Add ability to extend export dropdown.
5. (enh #106): Set right class for GridView):):FILTER_DATE_RANGE.
6. (enh #107): Cleanup and refactor GridView class code for better extensibility.
7. (enh #111): Fix export button dropdown menu display for IE.

Version 2.0.0
=============
**Date:** 14-Sep-2014

1. (enh #80): Add hidden property for columns to be hidden from display but available on export.
2. (bug #81): CSS class `kv-grid-hide` configured for hidden columns.
3. (enh #82): Created a reusable `ColumnTrait` for all custom yii2-grid columns.
4. (enh #83): Upgraded jQuery floatTheader plugin to latest version.
5. (bug #85, #87, #88): Enhance EditableColumn to capture keys of various data types
6. PSR 4 alias change
7. (bug #92): Bug fix for generating multiple rows in header/footer.

Version 1.9.0
=============
**Date:** 21-Aug-2014

1. (enh #65): Various enhancements to the widget to work with Pjax 
2. (enh #67): Fix Chrome bug for displaying loading indicator on tbody.
3. (enh #72): Enhancement for EditableColumn `beforeInput` and `afterInput`.
4. (enh #73): Enhancement for EditableColumn options to be configured as callback.
5. (enh #74,76): Enhance EditableColumn to allow grid refresh on successful update.


Version 1.8.0
=============

**Date:** 01-Aug-2014

1. (enh #58, #59): Russian language translation included
2. (enh #60): Added a new `EditableColumn` column to the grid that uses the enhanced `kartik\editable\Editable` widget to make the grid content editable.

Version 1.7.0
=============

**Date:** 14-Jul-2014

1. (enh #57): Added `containerOptions` to grid layout for allowing configuration of the grid table container. This can be set to
`false` to not display the container.

Version 1.6.0
=============

**Date:** 10-Jul-2014

1. (enh #54): Grid Export Enhancements
- Ability to preprocess and convert column data to your desired value before exporting. For example convert the HTML formatted icons for BooleanColumn to user friendly text like `Active` or `Inactive` after export.
- Hide any row or column in the grid by adding one or more of the following CSS classes):
    - `skip-export`): Will skip this element during export for all formats (`html`, `csv`, `txt`, `xls`).
    - `skip-export-html`): Will skip this element during export only for `html` export format.
    - `skip-export-csv`): Will skip this element during export only for `csv` export format.
    - `skip-export-txt`): Will skip this element during export only for `txt` export format.
    - `skip-export-xls`): Will skip this element during export only for `xls` (excel) export format.
    These CSS can be set virtually anywhere. For example `headerOptions`, `contentOptions`, `beforeHeader` etc.

2. (enh #52): Upgraded float header plugin

3. Enhanced panel footer to have a consistent height whether pagination is displayed or not.

4. `BooleanColumn` icons have been setup as `ICON_ACTIVE` and `ICON_INACTIVE` constants in GridView.

5. `ActionColumn` content by default has been disabled to appear in export output. The `skip-export` CSS class has been set as default in `headerOptions` and `contentOptions`.

Version 1.5.0
=============

**Date:** 04-Jul-2014

1. (enh #51): Enhanced GridView header and footer, to include additional headers/footers before or after default header/footer. 
   The properties below can be set as an array or string):
    - Added `beforeHeader` property to configure additional header rows before the default grid header. 
    - Added `afterHeader` property to configure additional header rows after the default grid header. 
    - Added `beforeFooter` property to configure additional footer rows before the default grid footer. 
    - Added `afterFooter` property to configure additional footer rows after the default grid footer. 
2. Fixes #26 to #50.

Version 1.4.0
=============

**Date:** 29-Apr-2014

1. (enh #25): Allow highlighting of selected row for a CheckboxColumn
    - Added `rowHighlight` property to set if a row needs to be highlighted
    - Added `rowSelectedClass` property to configure the CSS class for the highlighted row.
2. Fixes #20 to #24.

Version 1.3.0
=============

**Date:** 18-Apr-2014

1. (enh #19): Gridview enhancements (export, toolbar, iframe)
    - Enable rendering of export without panel by passing `{export}` variable to grid `layout` property.
    - Enable rendering of toolbar without panel by passing `{toolbar}` variable to grid `layout` property.
    - Revamp export form to be submitted in a new window (in a non-intrusive manner)
2. Fixes #1 to #19.

Version 1.2.0
=============

**Date:** 22-Mar-2014

1. Converted the extension into a module.
2. Export features enhanced for use across all browsers):
   - Save displayed grid as HTML
   - Save displayed grid as CSV
   - Save displayed grid as TEXT
   - Save displayed grid as XLS

Version 1.1.0
=============

**Date:** 15-Mar-2014

1. Export features added through a brand new custom JQuery plugin):
   - Save displayed grid as HTML
   - Save displayed grid as CSV
2. Templates to modify positioning of the export menu and the panel before and after contents
3. Ability to display toolbar in the header.

Version 1.0.0
=============

**Date:** 10-Mar-2014

Initial release
