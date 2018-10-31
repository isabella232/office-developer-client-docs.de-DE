---
title: 'Kapitel 6: Fehlerbehandlung'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7fd97104be4563b0245aac97f37aa1158d0463fa
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860413"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="6e245-102">Kapitel 6: Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="6e245-102">Chapter 6: Error Handling</span></span>


<span data-ttu-id="6e245-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e245-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e245-p101">ADO verwendet mehrere unterschiedliche Methoden, um eine Anwendung über aufgetretene Fehler zu informieren. In diesem Kapitel werden die Fehlertypen behandelt, die beim Verwenden von ADO auftreten können, sowie die Art und Weise, wie die Anwendung informiert wird. Schließlich werden Vorschläge zum Behandeln dieser Fehler gemacht.</span><span class="sxs-lookup"><span data-stu-id="6e245-p101">ADO uses several different methods to notify an application of errors that occur. This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified. It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="6e245-107">Wie meldet ADO Fehler?</span><span class="sxs-lookup"><span data-stu-id="6e245-107">How Does ADO Report Errors?</span></span>

<span data-ttu-id="6e245-108">ADO verwendet mehrere Methoden, um Sie über Fehler zu informieren:</span><span class="sxs-lookup"><span data-stu-id="6e245-108">ADO notifies you about errors in several ways:</span></span>

  - <span data-ttu-id="6e245-p102">ADO-Fehler generieren einen Laufzeitfehler. Behandeln Sie einen ADO-Fehler genau so wie jeden anderen Laufzeitfehler, wie z. B. mithilfe einer **On Error** -Anweisung in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e245-p102">ADO errors generate a run-time error. Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

  - <span data-ttu-id="6e245-p103">Das Programm kann Fehler von OLE DB empfangen. Ein OLE DB-Fehler generiert auch einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="6e245-p103">Your program can receive errors from OLE DB. An OLE DB error generates a run-time error as well.</span></span>

  - <span data-ttu-id="6e245-113">Bei einem datenproviderspezifischen Fehler wird mindestens ein **Error** -Objekt in der **Errors** -Auflistung des **Connection** -Objekts platziert, mit dem beim Auftreten des Fehlers auf den Datenspeicher zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="6e245-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

  - <span data-ttu-id="6e245-p104">Wenn der Prozess, der ein Ereignis auslöste, außerdem einen Fehler erzeugt, werden Fehlerinformationen einem **Error** -Objekt hinzugefügt und als Parameter an das Ereignis übergeben. Weitere Informationen zu Ereignissen finden Sie in [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="6e245-p104">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event. See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

  - <span data-ttu-id="6e245-p105">Probleme, die beim Verarbeiten von Batchaktualisierungen oder sonstigen Massenvorgängen, bei denen ein **Recordset** -Objekt beteiligt ist, auftreten, können durch die **Status** -Eigenschaft des **Recordset** -Objekts angezeigt werden. Beispielsweise können Schemaeinschränkungsverletzungen oder unzureichende Berechtigungen durch **RecordStatusEnum** -Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e245-p105">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**. For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

  - <span data-ttu-id="6e245-p106">Probleme, die bei einem bestimmten **Field** -Objekt im aktuellen Datensatz auftreten, werden ebenfalls durch die **Status** -Eigenschaft jedes **Field** -Objekts in der **Fields** -Auflistung des **Record** - oder **Recordset** -Objekts angezeigt. Beispielsweise können Aktualisierungen, die nicht abgeschlossen werden konnten, oder inkompatible Datentypen durch **FieldStatusEnum** -Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e245-p106">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**. For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="6e245-120">In den folgenden Abschnitten werden die verschiedenen Benachrichtigungsmethoden ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e245-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="6e245-121">ADO-Fehler</span><span class="sxs-lookup"><span data-stu-id="6e245-121">ADO Errors</span></span>](ado-errors.md)

- [<span data-ttu-id="6e245-122">ADO-Fehlerreferenz</span><span class="sxs-lookup"><span data-stu-id="6e245-122">ADO Error Reference</span></span>](ado-error-reference.md)

- [<span data-ttu-id="6e245-123">Anbieterfehler</span><span class="sxs-lookup"><span data-stu-id="6e245-123">Provider Errors</span></span>](provider-errors.md)

- [<span data-ttu-id="6e245-124">Field-Related Error Information</span><span class="sxs-lookup"><span data-stu-id="6e245-124">Field-Related Error Information</span></span>](field-related-error-information.md)

- [<span data-ttu-id="6e245-125">Recordset-Related Error Information</span><span class="sxs-lookup"><span data-stu-id="6e245-125">Recordset-Related Error Information</span></span>](recordset-related-error-information.md)

- [<span data-ttu-id="6e245-126">Vorhersehen von Fehlern</span><span class="sxs-lookup"><span data-stu-id="6e245-126">Anticipating Errors</span></span>](anticipating-errors.md)

- [<span data-ttu-id="6e245-127">Handling Errors in Other Languages (ADO)</span><span class="sxs-lookup"><span data-stu-id="6e245-127">Handling Errors in Other Languages (ADO)</span></span>](handling-errors-in-other-languages.md)