---
title: Hinzufügen von Datensätzen (Access PC-Datenbank-Referenz)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f235d7535f15eea7bd5d4c2abb88abb1a30935c7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862506"
---
# <a name="adding-records"></a><span data-ttu-id="b117d-102">Hinzufügen von Datensätzen</span><span class="sxs-lookup"><span data-stu-id="b117d-102">Adding Records</span></span>


<span data-ttu-id="b117d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b117d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b117d-p101">Verwenden Sie die **AddNew** -Methode, um einen neuen Datensatz in einem vorhandenen **Recordset** -Objekt zu erstellen und zu initialisieren. Verwenden Sie die **Supports** -Methode mit dem Wert **adAddNew** für **CursorOptionEnum**, um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b117d-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="b117d-p102">Nachdem Sie die **AddNew** -Methode aufgerufen haben, wird der neue Datensatz der aktuelle Datensatz und bleibt der aktuelle Datensatz, nachdem Sie die **Update** -Methode aufgerufen haben. Wenn das **Recordset** -Objekt keine Lesezeichen unterstützt, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, sobald Sie zu einem anderen Datensatz wechseln. Deshalb müssen Sie in Abhängigkeit vom Cursortyp die **Requery** -Methode aufrufen, damit auf den neuen Datensatz zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b117d-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="b117d-109">Wenn Sie **AddNew** während des Bearbeitens des aktuellen Datensatzes oder des Hinzufügens eines neuen Datensatzes aufrufen, ruft ADO die **Update** -Methode auf, um alle Änderungen zu speichern, und ADO erstellt dann den neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="b117d-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="b117d-110">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b117d-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="b117d-111">Adding Multiple Fields</span><span class="sxs-lookup"><span data-stu-id="b117d-111">Adding Multiple Fields</span></span>](adding-multiple-fields.md)

- [<span data-ttu-id="b117d-112">Determining Edit Mode</span><span class="sxs-lookup"><span data-stu-id="b117d-112">Determining Edit Mode</span></span>](determining-edit-mode.md)

- [<span data-ttu-id="b117d-113">Verwenden der AddNew-Methode im sofortigen Aktualisierungsmodus und im Batchmodus</span><span class="sxs-lookup"><span data-stu-id="b117d-113">Using AddNew in Immediate and Batch Modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

