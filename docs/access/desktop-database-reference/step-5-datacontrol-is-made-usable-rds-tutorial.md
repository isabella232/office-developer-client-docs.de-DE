---
title: 'Schritt 5: Verwendbarmachen des DataControl-Objekts (RDS-Lernprogramm)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d5b0dfef4d14594c2b2a9b8b57b866e032a07a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605653"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="f2d71-102">Schritt 5: Verwendbarmachen des DataControl-Objekts (RDS-Lernprogramm)</span><span class="sxs-lookup"><span data-stu-id="f2d71-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="f2d71-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2d71-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f2d71-p101">Das zurückgegebene **Recordset** -Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset** -Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset** -Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset** -Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f2d71-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="f2d71-108"><<<<<<< HEAD für Beispiel, wenn eine Webseite in Microsoft Internet Explorer angezeigt werden Sie möglicherweise Daten des **Recordset** -Objekts in einem visuellen Steuerelement anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f2d71-108"><<<<<<< HEAD For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="f2d71-109">Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f2d71-109">Visual controls on a Web page cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="f2d71-110">Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f2d71-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="f2d71-111">RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2d71-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
<span data-ttu-id="f2d71-112">=== Angenommen, wenn eine Webseite in Microsoft Internet Explorer angezeigt wird, möglicherweise möchten Sie die **Recordset** -Objektdaten in einem visuellen Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2d71-112">======= For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="f2d71-113">Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f2d71-113">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="f2d71-114">Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f2d71-114">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="f2d71-115">RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2d71-115">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
>>>>>>> <span data-ttu-id="f2d71-116">master</span><span class="sxs-lookup"><span data-stu-id="f2d71-116">master</span></span>

<span data-ttu-id="f2d71-117">Der **DATASRC** -Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD** -Eigenschaft auf ein **Recordset** -Objektfeld (Spalte) festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="f2d71-117">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="f2d71-118">In diesem Lernprogramm legen Sie die **SourceRecordset** -Eigenschaft fest:</span><span class="sxs-lookup"><span data-stu-id="f2d71-118">In this tutorial, set the **SourceRecordset** property:</span></span>

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

