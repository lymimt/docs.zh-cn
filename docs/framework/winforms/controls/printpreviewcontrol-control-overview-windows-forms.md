---
title: PrintPreviewControl 控件概述（Windows 窗体）
ms.date: 03/30/2017
f1_keywords:
- PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
ms.openlocfilehash: 330172a2ccf285cb75432572a558363e71de7ab1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33536990"
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a>PrintPreviewControl 控件概述（Windows 窗体）
Windows 窗体<xref:System.Windows.Forms.PrintPreviewControl>用于显示[PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md)打印时的样子。 此控件具有没有按钮或其他用户界面元素，因此通常仅在你想要编写自己的打印预览用户界面时才使用 <xref:System.Windows.Forms.PrintPreviewControl>。 如果你想标准用户界面，使用<xref:System.Windows.Forms.PrintPreviewDialog>控制; 请参阅[PrintPreviewDialog 控件概述](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)的概述。  
  
## <a name="key-properties"></a>键属性  
 控件的键属性是<xref:System.Windows.Forms.PrintPreviewControl.Document%2A>，这会设置要预览的文档。 文档必须是<xref:System.Drawing.Printing.PrintDocument>对象。 创建用于打印的文档的概述，请参阅[PrintDocument 组件概述](../../../../docs/framework/winforms/controls/printdocument-component-overview-windows-forms.md)和[Windows 窗体打印支持](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)。 <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A>和<xref:System.Windows.Forms.PrintPreviewControl.Rows%2A>属性确定显示在控件上的水平和垂直的页面数。 抗锯齿功能可以使文本显示生成更平滑的但它还可显示更慢;若要使用它，将设置<xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A>属性`true`。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Forms.PrintPreviewControl>  
 [PrintPreviewDialog 控件概述](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)  
 [PrintPreviewControl 控件](../../../../docs/framework/winforms/controls/printpreviewcontrol-control-windows-forms.md)  
 [对话框控件和组件](../../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)
