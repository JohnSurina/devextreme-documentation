---
id: dxHtmlEditorToolbarItem.formatName
acceptValues: 'background' | 'bold' | 'color' | 'font' | 'italic' | 'link' | 'image' | 'size' | 'strike' | 'subscript' | 'superscript' | 'underline' | 'blockquote' | 'header' | 'increaseIndent' | 'decreaseIndent' | 'orderedList' | 'bulletList' | 'alignLeft' | 'alignCenter' | 'alignRight' | 'alignJustify' | 'codeBlock' | 'variable' | 'separator' | 'undo' | 'redo' | 'clear' | 'insertTable' | 'insertRowAbove' | 'insertRowBelow' | 'insertColumnLeft' | 'insertColumnRight' | 'deleteColumn' | 'deleteRow' | 'deleteTable'
type: String
---
---
##### shortDescription
Specifies the predefined item that this object customizes or a format with multiple choices.

---
To customize a [predefined item](/concepts/05%20UI%20Components/HtmlEditor/20%20Toolbar/00%20Predefined%20Items '/Documentation/Guide/UI_Components/HtmlEditor/Toolbar/Predefined_Items/'), assign its name to this property and specify the other item properties.

This property also accepts names of formats with multiple choices. In addition to the format name, specify [formatValues](/api-reference/_hidden/dxHtmlEditorToolbarItem/formatValues.md '/Documentation/ApiReference/UI_Components/dxHtmlEditor/Configuration/toolbar/items/#formatValues'). On the toolbar, such formats are represented by [SelectBox](/api-reference/10%20UI%20Components/dxSelectBox '/Documentation/ApiReference/UI_Components/dxSelectBox/') UI components whose [properties](/api-reference/10%20UI%20Components/dxSelectBox/1%20Configuration '/Documentation/ApiReference/UI_Components/dxSelectBox/Configuration/') you can specify in the [options](/api-reference/_hidden/dxHtmlEditorToolbar/items/options.md '/Documentation/ApiReference/UI_Components/dxHtmlEditor/Configuration/toolbar/items/#options') object.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/HtmlEditor/Overview/"
}

In the following code, the `header` and `size` formats are configured as described in the previous paragraph:


---
#####jQuery

    <!--JavaScript-->
    $(function(){
        $("#htmlEditorContainer").dxHtmlEditor({
            toolbar: {
                items: [ // ...
                {
                    formatName: "header",
                    formatValues: [1, 2, 3, false],
                    options: {
                        width: 150
                    }
                }, {
                    formatName: "size",
                    formatValues: ["11px", "14px", "16px"]
                }]
            }
        })
    })

#####Angular

    <!--HTML-->
    <dx-html-editor>
        <dxo-toolbar>
            <dxi-item
                formatName="header"
                [formatValues]="[1, 2, 3, false]"
                [options]="{ width: 150 }">
            </dxi-item>
            <dxi-item
                formatName="size"
                [formatValues]="['11px', '14px', '16px']">
            </dxi-item>
        </dxo-toolbar>
    </dx-html-editor>   

    <!--TypeScript-->
    import { DxHtmlEditorModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxHtmlEditorModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxHtmlEditor ... >
            <DxToolbar>
                <DxItem
                    format-name="header"
                    :format-values="headerFormatValues" 
                    :options="headerFormatOptions"
                />
                <DxItem
                    format-name="size"
                    :format-values="sizeFormatValues"
                />
            </DxToolbar>
        </DxHtmlEditor>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import DxHtmlEditor, {
        DxToolbar,
        DxItem
    } from 'devextreme-vue/html-editor';

    export default {
        components: {
            DxHtmlEditor,
            DxToolbar,
            DxItem
        },
        data() {
            return {
                headerFormatValues: [1, 2, 3, false],
                headerFormatOptions: { width: 150 },
                sizeFormatValues: ["11px", "14px", "16px"]
            };
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import 'devextreme/dist/css/dx.light.css';

    import HtmlEditor, {
        Toolbar,
        Item
    } from 'devextreme-react/html-editor';

    const headerFormatValues = [1, 2, 3, false];
    const headerFormatOptions = { width: 150 };
    const sizeFormatValues = ["11px", "14px", "16px"];

    export default function App() {
        return (
            <HtmlEditor>
                <Toolbar>
                    <Item
                        formatName="header"
                        formatValues={headerFormatValues} 
                        options={headerFormatOptions}
                    />
                    <Item
                        formatName="size"
                        formatValues={sizeFormatValues}
                    />
                </Toolbar>
            </HtmlEditor>
        );
    }

---

Refer to the [Formats](/concepts/05%20UI%20Components/HtmlEditor/10%20Formats '/Documentation/Guide/UI_Components/HtmlEditor/Formats/') article for a full list of available formats.

#####See Also#####
- [widget](/api-reference/_hidden/dxHtmlEditorToolbarItem/widget.md '/Documentation/ApiReference/UI_Components/dxHtmlEditor/Configuration/toolbar/items/#widget')