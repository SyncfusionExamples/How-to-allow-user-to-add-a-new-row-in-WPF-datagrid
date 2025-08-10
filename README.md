# How to allow user to add a new row in WPF DataGrid?

[WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid) provides built-in row called AddNewRow. It allows user to add a new row to underlying collection. You can enable or disable by setting [SfDataGrid.AddNewRowPosition](https://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.Grid.SfDataGrid~AddNewRowPosition.html) property. You can also set the position of built-in AddNewRow through `AddNewRowPosition` property.

When you start editing in AddNewRow, the WPF DataGrid control creates an instance for the underlying data object and adds it to underlying collection when editing completed. So, the underlying data object must be defined with default constructor.

You can commit or cancel a new row from being added by pressing the Enter and Esc key respectively.

```xml
 <syncfusion:SfDataGrid  x:Name="dataGrid" 
                         ItemsSource="{Binding Orders}" 
                         AddNewRowPosition="Top"/>
```

**Add a new row programmatically to WPF DataGrid**

You can add a new row by using [SfDataGrid.View.AddNew](https://help.syncfusion.com/cr/wpf/Syncfusion.Data.WPF~Syncfusion.Data.CollectionViewAdv~AddNew.html) and [SfDataGrid.View.CommitNew](https://help.syncfusion.com/cr/wpf/Syncfusion.Data.CollectionViewAdv.html#Syncfusion_Data_CollectionViewAdv_CommitNew) methods.

```C#
private void Button_Click(object sender, RoutedEventArgs e)
{
    dataGrid.View.AddNew();
    this.dataGrid.View.CommitNew();
}
```

**Customize default string of built-in AddNewRow**

WPF DataGrid enables you to customize the watermark text of AddNewRow by changing value of AddNewRowText in Resource Designer.

You can go through this [user guide](https://help.syncfusion.com/wpf/datagrid/data-manipulation#customizing-addnewrow-text-using-default-resource-file) to know more about customizing default string of AddNewRow’s text.

**Initializing default values for AddNewRow**

WPF DataGrid allows you to set the default values for AddNewRow while initiating through AddNewRowInitiatingEventArgs.NewObject property in SfDataGrid.AddNewRowInitiating event.

```C#
dataGrid.AddNewRowInitiating += DataGrid_AddNewRowInitiating;

private void DataGrid_AddNewRowInitiating(object sender, AddNewRowInitiatingEventArgs e)
{
    var data = e.NewObject as OrderInfo;
    data.OrderID = 1000;
    data.CustomerID = "BERGS";
    data.CustomerName = "Hanna";
    data.Country = "UK";
    data.ShipCity = "London";
}
```

Take a moment to peruse the [WPF DataGrid - AddNewRow](https://help.syncfusion.com/wpf/datagrid/data-manipulation#add-new-rows), where you can find about built-in AddNewRow feature, with code examples.

Please refer this [link](https://www.syncfusion.com/wpf-controls/datagrid) to know about the essential features of Syncfusion WPF DataGrid.

## Requirements to run the demo
Visual Studio 2015 and above versions
