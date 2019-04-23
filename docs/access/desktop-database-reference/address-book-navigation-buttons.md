---
title: Navigationsschaltflächen des Adressbuchs
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282464"
---
# <a name="address-book-navigation-buttons"></a>Navigationsschaltflächen des Adressbuchs

**Gilt für**: Access 2013, Office 2013

Die Adressbuchanwendung zeigt die Navigationsschaltflächen am unteren Rand der Webseite an. Mithilfe der Navigationsschaltflächen können Sie durch die Daten in der HTML-Rasteransicht navigieren, indem Sie die erste oder die letzte Zeile mit Daten oder Zeilen neben der aktuellen Auswahl auswählen.

## <a name="navigation-sub-procedures"></a>Unterprozeduren für die Navigation

Die Adressbuchanwendung enthält verschiedene Prozeduren, die es den Benutzern ermöglichen, auf die Schaltflächen **First**, **Next**, **Previous** und **Last** zu klicken, um durch die Daten zu navigieren.

Wenn Sie beispielsweise auf die **erste** Schaltfläche klicken, wird\_die erste VBScript-Unterprozedur OnClick aktiviert. The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection. Wenn Sie auf die **Letzte** Schaltfläche klicken\_, wird die letzte OnClick-Sub-Prozedur aktiviert, die die [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) -Methode aufruft und die letzte Datenzeile zur aktuellen Auswahl macht. The remaining navigation buttons work in a similar fashion.

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

