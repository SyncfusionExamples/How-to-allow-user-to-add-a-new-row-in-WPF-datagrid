# How to allow user to add a new row in WPF DataGrid (SfDataGrid)?

## About the sample

This example illustrates how to add a new row in [WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) using buid in AddNewRow.

[WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) provides built-in row called AddNewRow. It allows user to add a new row to underlying collection. You can enable or disable by setting [SfDataGrid.AddNewRowPosition](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfDataGrid~AddNewRowPosition.html) property. You can also set the position of built-in AddNewRow through `AddNewRowPosition` property.

```xml
 <syncfusion:SfDataGrid  x:Name="dataGrid" 
                         ItemsSource="{Binding Orders}" 
                         AddNewRowPosition="Top"/>
```
## Requirements to run the demo
Visual Studio 2015 and above versions
