---
title: 'Schritt 5: Verwendbarmachen des DataControl-Objekts (RDS-Lernprogramm)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5871138f2b82770f49da2d5f9d4977443b0664e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884044"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="bfc3c-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span><span class="sxs-lookup"><span data-stu-id="bfc3c-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="bfc3c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfc3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfc3c-p101">Das zurückgegebene **Recordset** -Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset** -Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset** -Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset** -Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="bfc3c-108">Wenn eine Webseite in Microsoft Internet Explorer angezeigt werden, sollten Sie die **Recordset** -Objektdaten in einem visuellen Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-108">For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="bfc3c-109">Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-109">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="bfc3c-110">Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="bfc3c-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="bfc3c-111">RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="bfc3c-112">Der **DATASRC** -Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD** -Eigenschaft auf ein **Recordset** -Objektfeld (Spalte) festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="bfc3c-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="bfc3c-113">In diesem Lernprogramm legen Sie die **SourceRecordset** -Eigenschaft fest:</span><span class="sxs-lookup"><span data-stu-id="bfc3c-113">In this tutorial, set the **SourceRecordset** property:</span></span>

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

