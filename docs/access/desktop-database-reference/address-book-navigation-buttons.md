---
title: Navigationsschaltflächen des Adressbuchs
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f37a188fd3ddb3608eda414fbdcea6402cd9d41
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603945"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="e0f11-102">Navigationsschaltflächen des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="e0f11-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="e0f11-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0f11-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e0f11-104"><<<<<<< Adressbuch HEAD-Anwendung die Navigationsschaltflächen am unteren Rand der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e0f11-104"><<<<<<< HEAD The Address Book application displays the navigation buttons at the bottom of the Web page.</span></span> <span data-ttu-id="e0f11-105">Mithilfe der Navigationsschaltflächen können Sie durch die Daten in der HTML-Rasteransicht navigieren, indem Sie die erste oder die letzte Zeile mit Daten oder Zeilen neben der aktuellen Auswahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="e0f11-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
<span data-ttu-id="e0f11-106">=== Die adressbuchanwendung zeigt die Navigationsschaltflächen unten auf der Webseite.</span><span class="sxs-lookup"><span data-stu-id="e0f11-106">======= The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="e0f11-107">Mithilfe der Navigationsschaltflächen können Sie durch die Daten in der HTML-Rasteransicht navigieren, indem Sie die erste oder die letzte Zeile mit Daten oder Zeilen neben der aktuellen Auswahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="e0f11-107">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
>>>>>>> <span data-ttu-id="e0f11-108">master</span><span class="sxs-lookup"><span data-stu-id="e0f11-108">master</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="e0f11-109">Unterprozeduren für die Navigation</span><span class="sxs-lookup"><span data-stu-id="e0f11-109">Navigation Sub Procedures</span></span>

<span data-ttu-id="e0f11-110">Die Adressbuchanwendung enthält verschiedene Prozeduren, die es den Benutzern ermöglichen, auf die Schaltflächen **First**, **Next**, **Previous** und **Last** zu klicken, um durch die Daten zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="e0f11-110">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="e0f11-111">Aktiviert das erste VBScript beispielsweise durch Klicken auf die **erste** Schaltfläche\_OnClick Sub-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="e0f11-111">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="e0f11-112">Die Prozedur führt eine [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) -Methode, wodurch die erste Zeile der Daten der aktuellen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="e0f11-112">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="e0f11-113">Durch Klicken auf die Schaltfläche **letzte** aktiviert das letzte\_OnClick Sub-Prozedur, die die [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) -Methode der letzten Zeile der Daten der aktuellen Auswahl wird.</span><span class="sxs-lookup"><span data-stu-id="e0f11-113">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="e0f11-114">Die verbleibenden Navigationstasten funktionieren auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="e0f11-114">The remaining navigation buttons work in a similar fashion.</span></span>

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

