#include common-ctp-note-wo-devextreme

DevExtreme components currently only partly support the Shadow DOM. The following limitations apply:

- Diagram and Gantt do not support the Shadow DOM.

- CSS selectors in properties like [target](/api-reference/10%20UI%20Components/dxContextMenu/1%20Configuration/target.md '/Documentation/ApiReference/UI_Components/dxContextMenu/Configuration/#target') or [container](/api-reference/10%20UI%20Components/dxPopup/1%20Configuration/container.md '/Documentation/ApiReference/UI_Components/dxPopup/Configuration/#container') are not supported. Pass a DOM element instead.

- Popup, Tooltip, Popover, Toast, and LoadPanel render the dialog window in the `<body>` element, not in the Shadow DOM.

- DevExtreme stylesheets must be included in the Light DOM. Otherwise, Shadow DOM components may render incorrectly.

- If DevExtreme stylesheets lie in the same domain as `index.html`, the styles will be injected into the Shadow DOM. Otherwise, you need to state them explicitly in the Shadow DOM.

For an example on how to correctly set up DevExtreme components in the Shadow DOM, refer to the following GitHub repository:

#include btn-open-github with {
    href: "https://github.com/DevExpress-Examples/devextreme-datagrid-in-shadow-dom"
}

[tags] angular, react, vue