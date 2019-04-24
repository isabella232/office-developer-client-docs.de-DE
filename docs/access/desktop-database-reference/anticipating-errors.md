---
title: Vorhersehen von Fehlern
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4bd130ca05527c7761ca587781c1fd4f939ebe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297172"
---
# <a name="anticipating-errors"></a><span data-ttu-id="43094-102">Vorhersehen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="43094-102">Anticipating errors</span></span>


<span data-ttu-id="43094-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43094-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43094-p101">Die Fehlervermeidung ist mindestens so wichtig wie die Fehlerbehandlung. Dieser letzte Abschnitt enthält eine kurze Aufstellung der Vorsichtsmaßnahmen für Ihre Anwendung, um die Wahrscheinlichkeit von Fehlern zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="43094-p101">Error prevention is at least as important as error handling. This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="43094-p102">Überprüfen Sie den Status von Objekten, indem Sie den Wert der **State** -Eigenschaft überprüfen, bevor Sie einen Vorgang mithilfe dieser Objekte ausführen. Wenn die Anwendung z. B. ein globales **Connection** -Objekt verwendet, überprüfen Sie dessen **State** -Eigenschaft, um festzustellen, ob es bereits geöffnet ist, bevor Sie die **Open** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="43094-p102">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects. For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

- <span data-ttu-id="43094-p103">Jedes Programm, das Daten von einem Benutzer annimmt, muss Code zum Überprüfen dieser Daten enthalten, bevor sie an den Datenspeicher gesendet werden. Sie können sich nicht darauf verlassen, dass Sie vom Datenspeicher, vom Anbieter, von ADO oder sogar von der Programmiersprache über Probleme informiert werden. Sie müssen jedes von den Benutzern eingegebene Byte überprüfen und sicherstellen, dass die Daten den richtigen Typ für das Feld aufweisen und dass erforderliche Felder nicht leer sind.</span><span class="sxs-lookup"><span data-stu-id="43094-p103">Any program that accepts data from a user must include code to validate that data before sending it to the data store. You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems. You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="43094-p104">Überprüfen Sie die Daten, bevor Sie versuchen, Daten in den Datenspeicher zu schreiben. Dazu verwenden Sie am einfachsten das Ereignis **WillMove** oder **WillUpdateRecordset**. Ausführlichere Informationen zum Behandeln von ADO-Ereignissen finden Sie in [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="43094-p104">Check the data before you try to write any data to the data store. The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="43094-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span><span class="sxs-lookup"><span data-stu-id="43094-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="43094-117">Fehler treten ebenfalls auf, wenn Sie z. B. versuchen, **Seek** oder **Find** für ein leeres **Recordset**-Objekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43094-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

