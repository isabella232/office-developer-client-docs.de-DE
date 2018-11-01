---
title: 'Schritt 4: Auffüllen des Textfelds "Details"'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c00fd9d1a13a68361c5b1a7c3c2aa39736b3c88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867258"
---
# <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="2a115-102">Schritt 4: Auffüllen des Textfelds "Details"</span><span class="sxs-lookup"><span data-stu-id="2a115-102">Step 4: Populate the Details Text Box</span></span>


<span data-ttu-id="2a115-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a115-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="2a115-104">Schritt 4: Auffüllen des Detailstextfelds</span><span class="sxs-lookup"><span data-stu-id="2a115-104">Step 4: Populate the Details Text Box</span></span>

<span data-ttu-id="2a115-105">**So füllen Sie das Textfeld "Details" auf**</span><span class="sxs-lookup"><span data-stu-id="2a115-105">**To populate the Details text box**</span></span>

<span data-ttu-id="2a115-106">Erstellen Sie eine neue Unterroutine mit dem Namen recFields, und fügen Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="2a115-106">Create a new subroutine named recFields and insert the following code:</span></span>

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

<span data-ttu-id="2a115-p101">Dieser Code füllt lstDetails mit den Feldern und Werten des einfachen Datensatzes auf, der an recFields übergeben wird. Wenn die Ressource eine Textdatei ist, wird ein Textobjekt Stream im Ressourcendatensatz geöffnet. Der Code ermittelt, ob der Zeichensatz ASCII ist, und kopiert den Inhalt des Stream-Objekts in TxtDetails.</span><span class="sxs-lookup"><span data-stu-id="2a115-p101">This code populates lstDetails with the fields and values of the simple record passed to recFields. If the resource is a text file, a text **Stream** is opened from the resource record. The code determines if the character set is ASCII and copies the **Stream** contents into txtDetails.</span></span>

