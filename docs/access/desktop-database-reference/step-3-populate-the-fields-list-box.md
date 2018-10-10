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
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="1a2ab-102">Schritt 3: Auffüllen des Listenfelds "Fields"</span><span class="sxs-lookup"><span data-stu-id="1a2ab-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="1a2ab-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a2ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="1a2ab-104">Schritt 3: Auffüllen des Listenfelds "Fields"</span><span class="sxs-lookup"><span data-stu-id="1a2ab-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="1a2ab-105">**So füllen Sie das Listenfeld "Fields" auf**</span><span class="sxs-lookup"><span data-stu-id="1a2ab-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="1a2ab-106">Fügen Sie im Click-Ereignishandler von IstMain den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-106">Insert the following code into the Click event handler of lstMain:</span></span>

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

<span data-ttu-id="1a2ab-107">Dieser Code deklariert und instanziiert die lokalen **Record** und **Recordset** -Objekte, MAK und und Rs, jeweils.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="1a2ab-108">Die Zeile, die in LstMain ausgewählten Ressource entspricht wird die aktuelle Zeile des Grs durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="1a2ab-109">Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und mit der aktuellen Zeile des MAK geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="1a2ab-110">Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und MAK wird mit der aktuellen Zeile des Grs als Quelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="1a2ab-111">Ist die Ressource einen Auflistungsdatensatz (als durch **RecordType**angegeben), wird das lokale **Recordset**, Rs, auf die untergeordneten Elemente des MAK geöffnet. Und klicken Sie dann mit den Werten aus den Zeilen LstDetails ausgefüllt wird auf die untergeordneten Elemente des MAK geöffnet wird. Klicken Sie dann ist mit den Werten aus den Zeilen Rs LstDetails gefüllt.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="1a2ab-p102">Ist die Ressource ein einfacher Datensatz, wird RecFields aufgerufen. Weitere Informationen zu RecFields finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="1a2ab-114">Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-114">No code is implemented if the resource is a structured document.</span></span>

