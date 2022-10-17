# [1.6.0] - Custom template fragments

## Added

- Custom template fragments support.
- Replacement of primitiveIDs loaded from file system in LiveDahPanel.
- Drag and drop to tabs in workspace.
- Ability for setting the X axis in Visualization-BarChart.
- Ability to set the settings from the request in Visualization-Gauge.

## Changed

- Icon on node without children node in GraphStructurePanel.
- `isColoredTitle` flag processing in Visualization-List.
- Design of notifications.

## Fixed

- Graph renaming save in LiveDashPanel.
- Manual adding of custom actions in EventSystemPanel.
- Sync Datasource panels by `autorun` and `runOnTokenChange` params.
- Access to the properties of primitives inside node labels in LiveDashPanel.
- Visualization-Gauge out of range value color.

# [1.5.0] - New GUID format, PieChart visualization

## Added

- Aliases for systems without version to simplify interaction with them.
- Notification bell with notification list.
- Button to run datasources in the DatasourcePanel.
- Additional settings for datasources in the DatasourcePanel.
- Checking subscription and action forms in the EventSystemPanel.
- Scroll to dropdown list of graphs in the LiveDashControlPanel.
- Possibility of using expression property in datasource property.
- User notification by new NotificationSystem plugin.
- Saving the display type of primitives in the PrimitiveLibraryPanel.
- The scrolling in the settings panel.
- ID restoration from workspace config in order not to brake custom actions.
- New PieChart visualization.
- Additional settings for BarChart visualization.
- Notification if the value is outside the boundaries in the Gauge visualization.
- Ability to customize Table visualization using metadata.
- Click event when clicking on PieChart, BarChart, Gauge and some other visualizations.

## Changed

- GUID format for panels and systems.

## Fixed

- Problem with label text resetting to `$this.primitiveID$` while copying nodes.
- Bug with incorrect falsy values (null, false) in tokenStorage getRecord() method.
- Workspace color and icon not imported.

# [1.4.0] - Updated panels, custom primitive templates

## Added

- New plugin - GraphStructurePanel.
- Ability to save primitive as custom template.
- Saving edge bends in a graph.
- Confirmation before deleting the graph from the server.

## Changed

- PrimitiveLibraryPanel UI and design.
- PrimitivePropertiesPanel UI and design.

## Fixed

- Redirect to root folder after editing subfolder.
- Drag and drop when importing dashboard file.
- Workspace folder meta data is not saved on creation.

# [1.3.0]

## Added

- Error status to graph list if something goes wrong.
- Role model to workspaces (it's possible to configure it through django admin panel, UI functionality will be implemented in next releases)
- Extended electrical primitives extension with new primitives.
- Config form now closes while deleting any element.

## Changed

- PrimitiveID generation moved to server, and it's now through whole model.

## Fixed

- Problem with saving graphs on server (red crosses, primitive duplicates)
- Width and height of raw primitives swapped and works as expected.
- Delete current graph button not working.
- Workspace element colors are not applied or applied incorrectly.
- Fields of dataset now maps correctly in BarChart visualization.
- The value from the previous field type is not saved in PrimitivePropertiesPanel.
- Selected column and value for input type "datasource" are shown correctly in PrimitivePropertiesPanel.
- Error message disappears after fixing the failed request in PrimitivePropertiesPanel.

# [1.2.0] - Workspace panels border settings

## Added

- Ability to customize the borders of the workspace panels.
- New plugin - PrimitivePropertiesPanelCompact.

# [1.1.0] - Raw primitives and new property types in primitives

## Added

- Ability to create raw primitives by adding image and primitives description to the server.
- Select with constant data or otl request data and switch inputs for primtive properties.
- Default values for token in tokenStorage.
- Switching tabs by URL query parameter on workspace.
- Ability to create folder for workspaces on homepage.
- Filtering and sorting workpsaces and folders.
- New modal window to create workspaces.
- "Loading" and "no data" status for graph list.
- Error message while entering wrong login or password.

## Changed

- Transparancy on workspace panels in edit mode.

## Fixed

- Long values in select component no longer overflow.
- DataSourceSelect create button not working.
- Bug while editing property of primitive and selecting another one PropertiesPanel not switching to selected one.

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
