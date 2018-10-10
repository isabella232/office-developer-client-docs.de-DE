---
title: 'Schritt 4: Auffüllen des Textfelds "Details"'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e0f04d52edc55c7ccc5163bc9a858d7bc8845702
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474492"
---
# <a name="step-4-populate-the-details-text-box"></a>Schritt 4: Auffüllen des Textfelds "Details"


**Betrifft**: Access 2013 | Office 2013

## <a name="step-4-populate-the-details-text-box"></a>Schritt 4: Auffüllen des Textfelds "Details"

**So füllen Sie das Textfeld "Details" auf**

Erstellen Sie eine neue Unterroutine mit dem Namen recFields, und fügen Sie den folgenden Code ein:

```vb 
 
Sub recFields(r As Record, l As ListBox, t As TextBox) 
    Dim f As Field 
    Dim s As Stream 
    Set s = New Stream 
    Dim str As String 
     
    For Each f In r.Fields 
        l.AddItem f.Name & ": " & f.Value 
    Next 
    t.Text = "" 
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
        s.Open r, adModeRead, adOpenStreamFromRecord 
        str = s.ReadText(1) 
        s.Position = 0 
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
            s.Charset = "ascii" 
            s.Type = adTypeText 
        End If 
        t.Text = s.ReadText(adReadAll) 
    End If 
End Sub 
```

Dieser Code füllt lstDetails mit den Feldern und Werten des einfachen Datensatzes auf, der an recFields übergeben wird. Wenn die Ressource eine Textdatei ist, wird ein Textobjekt Stream im Ressourcendatensatz geöffnet. Der Code ermittelt, ob der Zeichensatz ASCII ist, und kopiert den Inhalt des Stream-Objekts in TxtDetails.

