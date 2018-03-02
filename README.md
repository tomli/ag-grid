
ag-Grid Row-Unselectable
==============

A fork of [ag-Grid](https://www.ag-grid.com)  which add the feature of disabling selection on row level.

How to use 
====================
Add "isNodeSelectable" property to the gridOptions , this property  must be a function which accept a RowNode object as parameter and return a boolean value, the return value of this function will decide if the row can be selected or not.

eg:
```js

        var gridOptions = {
            enableColResize: true,
            suppressRowClickSelection: true,
            rowSelection: 'multiple',
            columnDefs: columnDefs,
            isNodeSelectable: function (node) {
                return node.data.age >= 35;
            }
        };
```

[Example in Plunker](https://plnkr.co/edit/2bd3wuCPR7WAAShEQfMa?p=preview)

Note
====

This feature can be used as a solution to issue [Header Checkbox Not Able To Prevent Row Selection](https://github.com/ag-grid/ag-grid/issues/1503)