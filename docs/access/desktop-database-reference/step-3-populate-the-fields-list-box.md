---
title: 'Schritt 3: Auffüllen des Listenfelds "Fields"'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473308"
---
# <a name="step-3-populate-the-fields-list-box"></a>Schritt 3: Auffüllen des Listenfelds "Fields"


**Betrifft**: Access 2013 | Office 2013

## <a name="step-3-populate-the-fields-list-box"></a>Schritt 3: Auffüllen des Listenfelds "Fields"

**So füllen Sie das Listenfeld "Fields" auf**

Fügen Sie im Click-Ereignishandler von IstMain den folgenden Code ein:

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

Dieser Code deklariert und instanziiert die lokalen **Record** und **Recordset** -Objekte, MAK und und Rs, jeweils.

Die Zeile, die in LstMain ausgewählten Ressource entspricht wird die aktuelle Zeile des Grs durchgeführt. Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und mit der aktuellen Zeile des MAK geöffnet wird. Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und MAK wird mit der aktuellen Zeile des Grs als Quelle geöffnet.

Ist die Ressource einen Auflistungsdatensatz (als durch **RecordType**angegeben), wird das lokale **Recordset**, Rs, auf die untergeordneten Elemente des MAK geöffnet. Und klicken Sie dann mit den Werten aus den Zeilen LstDetails ausgefüllt wird auf die untergeordneten Elemente des MAK geöffnet wird. Klicken Sie dann ist mit den Werten aus den Zeilen Rs LstDetails gefüllt.

Ist die Ressource ein einfacher Datensatz, wird RecFields aufgerufen. Weitere Informationen zu RecFields finden Sie im nächsten Schritt.

Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.

