<template>
  <tui-image-editor ref="tuiImageEditor" :include-ui="useDefaultUI" :options="options"></tui-image-editor>
</template>
<script>
import "../../node_modules/tui-color-picker/dist/tui-color-picker.css";
import "../../node_modules/tui-image-editor/dist/tui-image-editor.css";
import { ImageEditor } from "@toast-ui/vue-image-editor";
import "../../node_modules/tui-image-editor";
import icon_a from "../../node_modules/tui-image-editor/dist/svg/icon-a.svg";
import icon_b from "../../node_modules/tui-image-editor/dist/svg/icon-b.svg";
import icon_c from "../../node_modules/tui-image-editor/dist/svg/icon-c.svg";
import icon_d from "../../node_modules/tui-image-editor/dist/svg/icon-d.svg";

var theme = {
  //common (fixed)
  "common.bi.image": "",
  "common.bisize.width": "0px",
  "common.bisize.height": "0px",
  "common.backgroundImage": "none",
  "common.backgroundColor": "#FFFFFF",
  "common.border": "0px",

  // header (fixed)
  "header.backgroundImage": "none",
  "header.backgroundColor": "transparent",
  "header.border": "0px",

  // load button (fixed)
  "loadButton.backgroundColor": "#fff",
  "loadButton.border": "1px solid #ddd",
  "loadButton.color": "#222",
  "loadButton.fontFamily": "NotoSans, sans-serif",
  "loadButton.fontSize": "12px",

  // download button (fixed)
  "downloadButton.backgroundColor": "#fdba3b",
  "downloadButton.border": "1px solid #fdba3b",
  "downloadButton.color": "#fff",
  "downloadButton.fontFamily": "NotoSans, sans-serif",
  "downloadButton.fontSize": "12px",

  // main icons
  // "menu.normalIcon.path": "../dist/svg/icon-b.svg",
  // "menu.normalIcon.name": "icon-b",
  // "menu.activeIcon.path": "../dist/svg/icon-a.svg",
  // "menu.activeIcon.name": "icon-a",
  // "menu.iconSize.width": "24px",
  // "menu.iconSize.height": "24px",
  // メインアイコン
  "menu.normalIcon.path": icon_d,
  "menu.activeIcon.path": icon_b,
  "menu.disabledIcon.path": icon_a,
  "menu.hoverIcon.path": icon_c,
  // サブメニューアイコン
  "submenu.normalIcon.path": icon_d,
  "submenu.activeIcon.path": icon_c,
  // "menu.normalIcon.path":
  //   "../../node_modules/tui-image-editor/dist/svg/icon-b.svg",
  // "menu.normalIcon.name": "icon-b",
  // "menu.activeIcon.path":
  //   "../../node_modules/tui-image-editor/dist/svg/icon-a.svg",
  // "menu.activeIcon.name": "icon-a",
  // "menu.iconSize.width": "24px",
  // "menu.iconSize.height": "24px",

  // submenu primary color
  "submenu.backgroundColor": "#ffffff",
  "submenu.partition.color": "#858585",

  // submenu icons
  // "submenu.normalIcon.path":
  //   "../../node_modules/tui-image-editor/dist/svg/icon-a.svg",
  // "submenu.normalIcon.name": "icon-a",
  // "submenu.activeIcon.path":
  //   "../../node_modules/tui-image-editor/dist/svg/icon-c.svg",
  // "submenu.activeIcon.name": "icon-c",
  // "submenu.iconSize.width": "24px",
  // "submenu.iconSize.height": "24px",

  // submenu labels
  "submenu.normalLabel.color": "#858585",
  "submenu.normalLabel.fontWeight": "lighter",
  "submenu.activeLabel.color": "#000",
  "submenu.activeLabel.fontWeight": "lighter",

  // checkbox style!
  "checkbox.border": "1px solid #ccc",
  "checkbox.backgroundColor": "#fff",

  // range style
  "range.pointer.color": "#000",
  "range.bar.color": "#666",
  "range.subbar.color": "#d1d1d1",
  "range.value.color": "#000",
  "range.value.fontWeight": "lighter",
  "range.value.fontSize": "11px",
  "range.value.border": "1px solid #353535",
  "range.value.backgroundColor": "#151515",
  "range.title.color": "#000",
  "range.title.fontWeight": "lighter",

  // colorpicker style
  "colorpicker.button.border": "1px solid #1e1e1e",
  "colorpicker.title.color": "#fff"
};

export default {
  name: "cardEditor",
  components: {
    "tui-image-editor": ImageEditor
  },
  data() {
    return {
      useDefaultUI: true,
      options: {
        // for tui-image-editor component's "options" prop
        cssMaxWidth: 700,
        cssMaxHeight: 500,
        includeUI: {
          // menu: ["shape", "filter"],
          initMenu: "filter",
          uiSize: {
            width: "100%",
            height: "600px"
          },
          theme: theme,
          menuBarPosition: "left"
        }
      }
    };
  }
};
</script>
