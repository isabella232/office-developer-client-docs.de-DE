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
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a>Schritt 5: Verwendbarmachen des DataControl-Objekts (RDS-Lernprogramm)


**Betrifft**: Access 2013 | Office 2013

Das zurückgegebene **Recordset** -Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset** -Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset** -Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset** -Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.

<<<<<<< HEAD für Beispiel, wenn eine Webseite in Microsoft Internet Explorer angezeigt werden Sie möglicherweise Daten des **Recordset** -Objekts in einem visuellen Steuerelement anzeigen möchten. Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen. Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md). RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.
=== Angenommen, wenn eine Webseite in Microsoft Internet Explorer angezeigt wird, möglicherweise möchten Sie die **Recordset** -Objektdaten in einem visuellen Steuerelement anzuzeigen. Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset** -Objekt zugreifen. Jedoch können sie das **Recordset** -Objekt über die [RDS. zugreifen. DataControl](datacontrol-object-rds.md). RDS **. DataControl** durch ein visuelles Steuerelement verwendet wird, wenn die [SourceRecordset](recordset-sourcerecordset-properties-rds.md) -Eigenschaft auf das **Recordset** -Objekt festgelegt ist.
>>>>>>> master

Der **DATASRC** -Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD** -Eigenschaft auf ein **Recordset** -Objektfeld (Spalte) festgelegt sein.

In diesem Lernprogramm legen Sie die **SourceRecordset** -Eigenschaft fest:

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

