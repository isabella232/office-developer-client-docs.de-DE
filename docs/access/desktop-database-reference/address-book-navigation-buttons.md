---
title: Navigationsschaltflächen des Adressbuchs
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 11d79201416a0b02e7af8f4d25140d4d138bd7d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603067"
---
# <a name="address-book-navigation-buttons"></a>Navigationsschaltflächen des Adressbuchs

**Gilt für**: Access 2013, Office 2013

Die Adressbuchanwendung zeigt die Navigationsschaltflächen am unteren Rand der Webseite an. Mithilfe der Navigationsschaltflächen können Sie durch die Daten in der HTML-Rasteransicht navigieren, indem Sie die erste oder die letzte Zeile mit Daten oder Zeilen neben der aktuellen Auswahl auswählen.

## <a name="navigation-sub-procedures"></a>Unterprozeduren für die Navigation

Die Adressbuchanwendung enthält verschiedene Prozeduren, die es den Benutzern ermöglichen, auf die Schaltflächen **First**, **Next**, **Previous** und **Last** zu klicken, um durch die Daten zu navigieren.

Wenn Sie beispielsweise auf die Schaltfläche **"First"** klicken, wird die VBScript First \_ OnClick Sub-Prozedur aktiviert. The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection. Durch Klicken auf die Schaltfläche **"Last"** wird die Letzte \_ OnClick Sub-Prozedur aktiviert, die die [MoveLast-Methode](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) aufruft und die letzte Datenzeile zur aktuellen Auswahl macht. The remaining navigation buttons work in a similar fashion.

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

