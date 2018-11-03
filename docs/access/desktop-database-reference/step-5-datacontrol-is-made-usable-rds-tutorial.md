---
title: 'Schritt 5: Verwendbarmachen des DataControl-Objekts (RDS-Lernprogramm)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2084b6ffb1b788ec5efcbb30ef2afaa5b3c5e650
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945544"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="af037-102">Schritt 5: DataControl ist verwendbar (RDS-Lernprogramm) vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="af037-102">Step 5: DataControl is made usable (RDS Tutorial)</span></span>


<span data-ttu-id="af037-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af037-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af037-p101">Das zurückgegebene **Recordset** -Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset** -Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset** -Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset** -Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.</span><span class="sxs-lookup"><span data-stu-id="af037-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="af037-108">Wenn eine Webseite in Microsoft Internet Explorer angezeigt werden, sollten Sie die **Recordset** -Objektdaten in einem visuellen Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="af037-108">For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="af037-109">Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="af037-109">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="af037-110">Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="af037-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="af037-111">RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="af037-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="af037-112">Der **DATASRC** -Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD** -Eigenschaft auf ein **Recordset** -Objektfeld (Spalte) festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="af037-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="af037-113">In diesem Lernprogramm legen Sie die **SourceRecordset** -Eigenschaft fest:</span><span class="sxs-lookup"><span data-stu-id="af037-113">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

