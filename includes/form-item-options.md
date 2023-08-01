When you modify an item, the Form also refreshes all other items in its group. If an item is not in a group, the whole Form is refreshed. To update only your chosen items, wrap them into a separate group.

[note] When you call this method, Form rerenders the layout. As a result, all editors are re-initialized and their settings return to the initial [editorOptions](/Documentation/ApiReference/UI_Components/dxForm/Item_Types/SimpleItem/#editorOptions) configuration.