# [1.0.0] - DTCD release

DataCAD is a single-page web application for building flexible user interfaces that can be extended and customized by plugins.

## Core systems

The core of the application includes the following systems:

- EventSystem - allows you to add communication between application plugins, as well as implement custom logic between them.
- StorageSystem - allows you to store the data necessary for the user to work with the application and build dashboards. The system provides the following types of storage:
  - Browser;
  - Session.
- DataSourceSystem - allows you to receive data from external sources, for example, OT.Platform. The list of available data sources can be extended with the external datasource extension plugins.
- StyleSystem - responsible for the appearance of the application and allows you to customize it, which includes the ability to add custom themes and change the set of basic GUI elements.
- WorkspaceSystem - allows you to create workspaces where you can place plugin panels.

## Panel plugins

Panel plugins are interactive user interface components placed on the workspace.

List of available panels:

- ConfigEditorPanel - allows you to configure settings of panel plugins on workspace.
- DatasourcePanel - allows you to interact with the DataSourceSystem;
- EventSystemPanel - allows you to interact with the EventSystem;
- LiveDashPanel - a canvas on which primitive objects can be placed and links between them can be configured. LiveDashPanel core functions include creating graph fragments, saving them to the server or to the local file system, retrieving list of available fragments from server or loading graph from file system.
- LiveDashControlPanel - panel with a set of buttons to interact with LiveDashPanel API (opening graph, saving graph, undo, redo, copy, cut, paste, zoom in/out etc.)
- PrimitiveLibraryPanel - panel-aggregator of primitives for canvas. By itself, it does not contain primitives. Primitive sets are supplied as plugin extensions. List of available sets:
- ExtensionCommonPrimitives;
- ExtensionElectricalSchemePrimitives;
- ExtensionRiskPrimitives.
- PrimitivePropertiesPanel - allows you to manage the properties of primitives placed on the canvas;
- ButtonPanel;
- Visualization Gauge;
- Visualization Text;
- Visualization Table;
- Visualization-BarChart;
- Visualization-RiskReview;
- Visualization List.

## User functionality

User profile customization - change personal data, password, application theme;
