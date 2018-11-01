---
title: 'Schritt 3: Auffüllen des Listenfelds "Fields"'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae1513c47c79da4f4df7fee2f3f3d7b3507ac1c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876659"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="59f5f-102">Schritt 3: Auffüllen des Listenfelds "Fields"</span><span class="sxs-lookup"><span data-stu-id="59f5f-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="59f5f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59f5f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="59f5f-104">Schritt 3: Auffüllen des Felderlistenfelds</span><span class="sxs-lookup"><span data-stu-id="59f5f-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="59f5f-105">**So füllen Sie das Listenfeld "Fields" auf**</span><span class="sxs-lookup"><span data-stu-id="59f5f-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="59f5f-106">Fügen Sie im Click-Ereignishandler von IstMain den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="59f5f-106">Insert the following code into the Click event handler of lstMain:</span></span>

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

<span data-ttu-id="59f5f-107">Dieser Code deklariert und instanziiert die lokalen **Record** und **Recordset** -Objekte, MAK und und Rs, jeweils.</span><span class="sxs-lookup"><span data-stu-id="59f5f-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="59f5f-108">Die Zeile, die in LstMain ausgewählten Ressource entspricht wird die aktuelle Zeile des Grs durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="59f5f-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="59f5f-109">Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und mit der aktuellen Zeile des MAK geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="59f5f-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="59f5f-110">Klicken Sie dann im Listenfeld **Details** deaktiviert ist, und MAK wird mit der aktuellen Zeile des Grs als Quelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="59f5f-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="59f5f-111">Ist die Ressource einen Auflistungsdatensatz (als durch **RecordType**angegeben), wird das lokale **Recordset**, Rs, auf die untergeordneten Elemente des MAK geöffnet. Und klicken Sie dann mit den Werten aus den Zeilen LstDetails ausgefüllt wird auf die untergeordneten Elemente des MAK geöffnet wird. Klicken Sie dann ist mit den Werten aus den Zeilen Rs LstDetails gefüllt.</span><span class="sxs-lookup"><span data-stu-id="59f5f-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="59f5f-p102">Ist die Ressource ein einfacher Datensatz, wird RecFields aufgerufen. Weitere Informationen zu RecFields finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="59f5f-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="59f5f-114">Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.</span><span class="sxs-lookup"><span data-stu-id="59f5f-114">No code is implemented if the resource is a structured document.</span></span>

