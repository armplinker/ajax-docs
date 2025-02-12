---
title: Telerik.Web.UI.GridBinaryImageColumn
page_title: Telerik.Web.UI.GridBinaryImageColumn
description: Telerik.Web.UI.GridBinaryImageColumn
---

# Telerik.Web.UI.GridBinaryImageColumn

Each cell in a GridBinaryImageColumn contains an image streamed from a binary image source field 
            (specified through the DataField property of the column). When used this column will show a RadBinaryImage
            control in view mode and RadUpload in edit mode to upload an image.
            The image will be sized automatically to ImageHeight and ImageWidth pixel values if the ResizeMode property
            of the column is different than None. Possible values for the ResizeMode property of the column are:
            - Crop (the image will be trimmed)
            - Fit (the image will be sized to fit the given dimensions)
            - None (default)
            Additionally, you can set the DataAlternateTextField property to specify by which field in the grid source 
            the column will be sorted/filtered. For the filtering you must also set explicitly the DataType property of
            the column to the type of the field specified through the DataAlternateTextField property 
            (System.String in the common case). You can also apply format using the DataAlternateTextFormatString property.

## Inheritance Hierarchy

* System.Object
* Telerik.Web.UI.GridColumn : IComparable, IStateManager
* Telerik.Web.UI.GridEditableColumn : IGridDataColumn, IGridEditableColumn
* Telerik.Web.UI.GridBinaryImageColumn

## Properties

###  AllowFiltering `Boolean`

Gets or sets whether the column data can be filtered.

###  AllowSorting `Boolean`

Gets or sets a whether the column data can be sorted.

###  AlternateText `String`

Gets or sets a string, specifying the text which will be shown as alternate
            text to the image

###  AndCurrentFilterFunction `GridKnownFunction`

Gets or sets the current second filter condition function.

###  AndCurrentFilterValue `String`

Gets or sets a value of the currently applied second filter condition value.

###  AutoAdjustImageControlSize `Boolean`

Specifies if the HTML image element's dimensions are inferred from image's binary data

###  AutoPostBackOnFilter `Boolean`

Gets or sets a value indicating whether the grid should automatically postback,
            when the value in the filter text-box changes, and the the focus moves to another
            element.

###  ColumnEditor `IGridColumnEditor`

Gets the column editor instance for this column.

###  ColumnEditorID `String`

Gets or sets the column editor ID that will be used when the column is displayed in edit mode.

###  ColumnType `String`

Gets the string representation of the type-name of this instance. The value is
            used by RadGrid to determine the type of the columns persisted into the ViewState, when
            recreating the grid after postback. The value is also used by the grid client-side
            object. This property is read only.

###  ConvertEmptyStringToNull `Boolean`

Convert the emty string to null when extracting values for inserting, updating, deleting

###  CurrentColumnEditor `IGridColumnEditor`

Get the current colum editor. If the column editor is not assigned at the moment the column will search for the ColumnEditorID on the page or should
            create its default column editor

###  CurrentFilterFunction `GridKnownFunction`

Gets or sets the current function used for filtering.

###  CurrentFilterValue `String`

Gets or sets a value of the currently applied filter.

###  DataAlternateTextField `String`

Gets or sets a string, representing the DataField name from the data source,
            which will be used to supply the alternateText for the image in the column. This text can
            further be customized, by using the DataTextFormatString property.

###  DataAlternateTextFormatString `String`

Gets or sets a string, specifying the format string, which will be used to format
            the alternate text of the image, rendered in the cells of the column.

###  DataField `String`

Gets or sets the field name from the specified data source to bind to the
            .

###  DataType `Type`

Gets or sets (see the Remarks) the type of the data from the DataField as it
                was set in the DataSource.

#### Remarks
The DataType property supports the following base .NET Framework data
                types:BooleanByteCharDateTimeDecimalDoubleInt16Int32Int64SByteSingleStringTimeSpanUInt16UInt32UInt64

###  DataTypeName `String`

Gets the string representation of the DataType property of the
            column, needed for the client-side grid instance.

###  DefaultImageUrl `String`

Gets or sets a url, specifying the location of a default image 
            which to be loaded if there is no data for the binary image

###  DefaultInsertValue `String`

Gets or sets a default value for the column when the row is in Insert mode

###  Display `Boolean`

Gets or sets a value indicating whether the cells corresponding to a column would be rendered with a 'display:none' style attribute (end-user-not-visible).
            To completely prevent cells from rendering, set the  property to false, instead of the Display property.

###  EditFormColumnIndex `Int32`

Specifies the vertical collumn number where this column will appear when
                using EditForms editing mode and the form is autogenerated. See the remarks for
                details.

#### Remarks
A practicle example of using this property is to deterimine the number of
                columns rendered in the edit form. If there will be only one column in the rendered
                edit form, when we retrieve the value of this property for a column, as shown in
                the code below:protected void RadGrid1_PreRender(object sender, EventArgs e)    {int columnIndex = RadGrid1.MasterTableView.Columns[3].EditFormColumnIndex;    }it will be equal to 0, meaning the the column belongs to the first group of
                columns in the edit form.

###  EditFormHeaderTextFormat `String`

String that formats the HeaderText when the column is displayed in an edit form

###  EnableHeaderContextMenu `Boolean`

Determines if the header context menu will be displayed for the current column.
            This property works together with the EnableHeaderContextMenu property of the corresponding GridTableView.
            Default value is true.

###  Exportable `Boolean`

Determines whether the given column will be shown in the exported file

###  FilterCheckListEnableLoadOnDemand `Boolean`

Get or Set if the Filter Check List will load data on demand from server.

###  FilterCheckListWebServiceMethod `String`

Get or Set the Methood from CheckListWebServicePath Web Service defined in the TableView,
            that to be used for getting data for the filter check list

###  FilterControlAltText `String`

Gets or Sets the text value which should be added to alt attribute of the filter control

###  FilterControlToolTip `String`

Gets or sets the filter control ToolTip property value.

###  FilterControlWidth `Unit`

Use this property to set width to the filtering control (depending on the column type, this may be a normal textbox, RadNumericTextBox, RadDatePicker, etc.)

###  FilterDelay `Nullable`1`

Gets or sets the filter delay which determines after how many milliseconds a 
            filtering will occur after a filter value have changed.

###  FilterImageToolTip `String`

Gets or sets the filter image tool tip.

###  FilterImageUrl `String`

Gets or sets a string representing the URL to the image used in the filtering
            box.

###  FilterListOptions `GridFilterListOptions`

Gets or sets the value indincating which of the filter functions should be
            available for that column. For more information see
             enumaration.

###  FilterTemplate `ITemplate`

Gets or sets the template, which will be rendered in the filter item cell of the column.

###  FooterStyle `TableItemStyle`

Style of the cell in the footer item of the grid, corresponding to the column.

###  FooterText `String`

Use the FooterText property to specify your own or determine the current
            text for the footer section of the column.

###  ForceExtractValue `GridForceExtractValues`

Force RadGrid to extract values from EditableColumns that are ReadOnly (or IsEditable is false).

###  Groupable `Boolean`

Gets or sets a value indicating whether you will be able to group
            Telerik RadGrid by that column. By default this property is
            true.

#### Remarks
See Telerik RadGrid manual for details about using grouping. If
            Groupable is false the column header cannot be dragged to the
            GroupPanel.

###  GroupByExpression `String`

The group-expression that should be used when grid is grouping-by this column. If
            not set explicitly, RadGrid will generate a group expression based on the DataField of
            the column (if available), using the 
            method.The grouping can be turned on/off for columns like GridBoundColumn using
             property.For more information about the Group-By expressions and their syntax, see
             class.

###  HeaderAbbr `String`

Gets or sets the column cell 'abbr' attribute.

###  HeaderAxis `String`

Gets or sets the column cell 'axis' attribute.

###  HeaderButtonType `GridHeaderButtonType`

Gets or sets the button type of the button rendered in the header item, used
                for sorting. The possible values that this property accepts are:Telerik.Web.UI.GridHeaderButtonType.LinkButton
                Telerik.Web.UI.GridHeaderButtonType.PushButton
                Telerik.Web.UI.GridHeaderButtonType.TextButton

###  HeaderImageUrl `String`

Gets or sets the URL of an image in the cell in the header item of the grid
            current column. You can use a relative or an absolute URL.

###  HeaderStyle `TableItemStyle`

Style of the cell in the header item of the grid, corresponding to the column.

###  HeaderText `String`

Use the HeaderText property to specify your own or determine the current
            text for the header section of the column.

###  HeaderTooltip `String`

Gets or sets the header tooltip of the column.

###  ImageAlign `ImageAlign`

Gets or sets the  property for each cell.

###  ImageHeight `Unit`

Gets or sets the height of the image

###  ImageWidth `Unit`

Gets or sets the width of the image

###  InsertVisiblityMode `GridColumnVisibilityMode`

Gets or sets a value determining whether a editor
            will be displayed in the insert item.
            Inherited: The visibility is dependent on the value of the ReadOnly property.
            AlwaysVisible: The insert item is always visible
            AlwaysHidden: The insert item is always hidden

###  IsEditable `Boolean`

This property is supposed for developers of new grid columns. It gets whether
            a column is currently ReadOnly. The ReadOnly property determines whether a column
            will be editable in edit mode. A column for which the ReadOnly property is true
            will not be present in the automatically generated edit form.

###  IsEditable `Boolean`

This property is supposed for developers of new grid columns. It gets whether
                a column is currently ReadOnly. The ReadOnly property determines whether a column
                will be editable in edit mode. A column for which the ReadOnly property is true
                will not be present in the automatically generated edit form.

###  ItemStyle `TableItemStyle`

Style of the cells, corresponding to the column.

###  ListOfFilterValues `String[]`

Access the valus passed from the ListBox used for CheckList in the filter.

###  OrderIndex `Int32`

Gets or sets the order index of column in the collection of
                . Use
                 method for reordering the columns.

#### Remarks
We recommend using this property only for getting the order index for a
                    specific column instead of setting it. Use
                     method for reordering columns.
                Note that changing the column order index will change the order of the cells
                in the grid items, after the grid is rebound.
                    The value of the property would not affect the order of the column in the
                     collection.

###  Owner `GridTableView`

Gets the instance of the GridTableVeiw wich owns this column instance.

###  OwnerGridID `GridTableView`

Gets the value of the ClientID property of the RadGrid instance that owns this column. This property value is used by grid's client object

###  OwnerID `GridTableView`

Gets the value of the ClientID property of the GridTableView that owns this column. This property value is used by grid's client object

###  PersistBinaryDataOnEdit `Boolean`

Gets or sets a value indicating if the binary that will be persisted when editing.
            Setting the value to true will pass the old binary image data to the data source so
            the image could be persisted and not deleted.

###  ReadOnly `Boolean`

Gets or sets the readonly status of the column. The column will be displayed in
            browser mode (unless its Visible property is false)
            but will not appear in the edit-form.

###  Reorderable `Boolean`

Gets or sets a value indicating whether the column can be reordered client-side.

###  Resizable `Boolean`

Gets or sets a value indicating whether the column can be resized client-side.
            You can use this property, by setting it to false, to disable resizing for a particular
            column, while preserving this functionality for all the other columns.

###  ResizeMode `BinaryImageResizeMode`

Gets or sets the  property for each cell.

###  RowSpan `Int32`

For internal use. Gets or sets the row span of the grid column.

###  SavedImageName `String`

Get or set the name of the file which will appear inside of the SaveAs
            browser dialog

###  Selectable `Boolean`

Gets the value determining if the column is selectable.

###  Selected `Boolean`

Indicates whether all column cells have been selected

###  ShowFilterIcon `Boolean`

Gets or sets if the filter icon in the  will be visible.

###  ShowNoSortIcon `Boolean`

Get or Sets a value indicating whether a no sort icon should appear next to the
            header button, when a column is not sorted but can be sorted.

###  ShowSortIcon `Boolean`

Get or Sets a value indicating whether a sort icon should appear next to the
            header button, when a column is sorted.

###  Sortable `Boolean`

Should override if sorting will be disabled

###  SortAscImageUrl `String`

Gets or sets a string representing the URL to the image used for sorting in
            ascending mode.

###  SortDescImageUrl `String`

Gets or sets a string representing the URL to the image used for sorting in
            descending mode.

###  SortedBackColor `Color`

Gets or sets the color of a cell which is sorted.

###  SortExpression `String`

The string representing a filed-name from the DataSource that should be used when grid sorts by this column. For example:
            'EmployeeName'

###  UniqueName `String`

Each column in Telerik RadGrid has an UniqueName
            property (string). This property is assigned automatically by the designer (or the
            first time you want to access the columns if they are built dynamically).

#### Remarks
You can also set it explicitly, if you prefer. However, the automatic
                generation handles most of the cases. For example a
                GridBoundColumn with DataField 'ContactName'
                would generate an UniqueName of 'ContactName'.Additionally, there may be occasions when you will want to set the UniqueName
                explicitly. You can do so simply by specifying the custom name that you want to
                choose:<radG:GridTemplateColumn UniqueName="ColumnUniqueName"></radG:GridTemplateColumn>

###  UploadControlType `GridUploadControlType`

Gets or sets a value indicating what type of upload control will be initialized during edit.
            (Default value = )

###  UseNativeEditorsInMobileMode `Boolean`

Gets or sets whether the column editor will be native when gird's RenderMode is set to Mobile

###  Visible `Boolean`

Gets or sets a value indicating if the column and all corresponding cells would be rendered.

## Methods

###  Clone

Creates a copy of the current column.

#### Remarks
Note: When implementing/overriding this method be sure to call
            the base member or call CopyBaseProperties to be sure that all base
            properties will be copied accordingly

#### Returns

`Telerik.Web.UI.GridColumn` 

###  Clone

Creates a copy of the current column.

#### Remarks
Note: When implementing/overriding this method be sure to call
            the base member or call CopyBaseProperties to be sure that all base
            properties will be copied accordingly

#### Returns

`Telerik.Web.UI.GridColumn` 

###  EvaluateFilterExpression

Gets a string representing a filter expression, based on the settings of all
            columns that support filtering, with a syntax ready to be used by a
            DataView object

#### Returns

`System.String` 

###  EvaluateFilterExpression

Evaluates the column filter expression based on the , , 
            ,  propeties. It could be used to handle custom 
            filtering and is internally used for determining  FilterExpression value.

#### Returns

`System.String` 

###  FillValues

Extracts the values from the editedItem and fills the names/values pairs for each data-field edited by the column in the newValues dictionary.

#### Parameters

#### newValues `System.Collections.IDictionary`

dictionary to fill. This param should not be null (Nothing in VB.NET)

#### editableItem `Telerik.Web.UI.GridEditableItem`

the GridEditableItem to extract values from

#### Returns

`System.Void` 

###  FillValues

Extracts the values from the editedItem and fills the names/values pairs for each data-field edited by the column in the newValues dictionary.

#### Parameters

#### newValues `System.Collections.IDictionary`

dictionary to fill. This param should not be null (Nothing in VB.NET)

#### editableItem `Telerik.Web.UI.GridEditableItem`

the GridEditableItem to extract values from

#### Returns

`System.Void` 

###  GetActiveDataField

Returns the DataField that will be used for Filter and Sorting operations

#### Returns

`System.String` 

###  GetCurrentFilterValueFromControl

Gets the value of the Text property of a textbox control found in the cell, used to set the value of the CurrentFilterValue property.

#### Parameters

#### cell `System.Web.UI.WebControls.TableCell`

#### Returns

`System.String` 

###  GetCustomPropertyDataFields

This method should be used in case you develop your own column. It returns the
            full list of DataFields used by the column.
            GridTableView uses this to decide which DataFields
            from the specified DataSource will be inlcuded in case of
            GridTableView.RetrieveAllDataFields is set to
            false.

#### Returns

`System.Collections.IDictionary` 

###  GetDefaultGroupByExpression

Calculate the default Group-by expression based on the settings of the
            DataField (if available)

#### Remarks
For example, if a column's DataField is ProductType the default group-by expression will be:
            'ProductType Group By ProductType'

#### Returns

`System.String` 

###  GetFilterFunctionsList

Gets a list of filter functions based on the settings of the  property.

#### Parameters

#### options `Telerik.Web.UI.GridFilterListOptions`

#### sourceList `System.Collections.ArrayList`

#### Returns

`System.Collections.ArrayList` 

###  GetSortExpression

By default returns the SortExpression of the column. If the SortExpression is not set explicitly, it would be calculated, based on the
            DataField of the column.

#### Returns

`System.String` 

###  Initialize

The Initialize method is inherited by a derived
            GridColumn class. Is is used to reset a column of the derived
            type.

#### Remarks
This method is mainly used to reset properties common for all column types
            derived from GridColumn class.The Initialize method is usually called during data-binding, prior to the
            first row being bound.

#### Returns

`System.Void` 

###  InitializeCell

After a call to this method the column should add the corresponding controls
            (text, labels, input controls) into the cell given, regarding the inItem type and
            column index.Note: This method is called within RadGrid and is not intended
            to be used directly from your code.

#### Returns

`System.Void` 

###  IsBoundToFieldName

This method returns true if the column is bound to the specified field
            name.

#### Parameters

#### name `System.String`

The name of the DataField, which will be checked.

#### Returns

`System.Boolean` 

###  IsBoundToFieldName

This method returns true if the column is bound to the specified field
            name.

#### Parameters

#### name `System.String`

The name of the DataField, which will be checked.

#### Returns

`System.Boolean` 

###  PrepareCell

Prepares the cell of the item given, when grid is rendered.

#### Parameters

#### cell `System.Web.UI.WebControls.TableCell`

#### item `Telerik.Web.UI.GridItem`

#### Returns

`System.Void` 

###  RefreshCurrentFilterValue

Modifies the CurrentFilterFunction and
            CurrentFilterValue properties according to the function given and the
            corresponding filter text-box control in the filtering item.

#### Returns

`System.Void` 

###  RefreshCurrentFilterValue

Modifies the CurrentFilterValue property according to the
            corresponding selected item in the filter text-box control in the filtering
            item.

#### Returns

`System.Void` 

###  ResetCurrentFilterValue

Resets the values of the  and
             properties to their defaults.

#### Returns

`System.Void` 

###  ResetCurrentFilterValue

Resets the values of the ,
            ,  and
             properties to their defaults.

#### Returns

`System.Void` 

###  SetCurrentFilterValueToControl

Sets the value of the property CurrentFilterValue as a text on the TextBox control found in the cell

#### Parameters

#### cell `System.Web.UI.WebControls.TableCell`

#### Returns

`System.Void` 

###  SetupFilterControls

Instantiates the filter controls (text-box, image.) in the cell given

#### Parameters

#### cell `System.Web.UI.WebControls.TableCell`

#### Returns

`System.Void` 

###  ShouldExtractValues

Get value based on the current IsEditable state, item edited state and ForceExtractValue setting.

#### Parameters

#### item `Telerik.Web.UI.GridEditableItem`

item to check to extract values from

#### Returns

`System.Boolean` 

###  SupportsFiltering

This method should be used in case you develop your own column. It returns true
            if the column supports filtering.

#### Returns

`System.Boolean` 

###  SupportsFiltering

This method should be used in case you develop your own column. It returns true
            if the column supports filtering.

#### Returns

`System.Boolean` 

