---
title: Hinzufügen von Datensätzen (Access Desktop Database Reference)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280287"
---
# <a name="adding-records"></a><span data-ttu-id="52ae7-102">Hinzufügen von Datensätzen</span><span class="sxs-lookup"><span data-stu-id="52ae7-102">Adding records</span></span>

<span data-ttu-id="52ae7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52ae7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52ae7-p101">Verwenden Sie die **AddNew** -Methode, um einen neuen Datensatz in einem vorhandenen **Recordset** -Objekt zu erstellen und zu initialisieren. Verwenden Sie die **Supports** -Methode mit dem Wert **adAddNew** für **CursorOptionEnum**, um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="52ae7-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="52ae7-p102">Nachdem Sie die **AddNew** -Methode aufgerufen haben, wird der neue Datensatz der aktuelle Datensatz und bleibt der aktuelle Datensatz, nachdem Sie die **Update** -Methode aufgerufen haben. Wenn das **Recordset** -Objekt keine Lesezeichen unterstützt, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, sobald Sie zu einem anderen Datensatz wechseln. Deshalb müssen Sie in Abhängigkeit vom Cursortyp die **Requery** -Methode aufrufen, damit auf den neuen Datensatz zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="52ae7-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="52ae7-109">Wenn Sie **AddNew** während des Bearbeitens des aktuellen Datensatzes oder des Hinzufügens eines neuen Datensatzes aufrufen, ruft ADO die **Update** -Methode auf, um alle Änderungen zu speichern, und ADO erstellt dann den neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="52ae7-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="52ae7-110">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="52ae7-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="52ae7-111">Hinzufügen mehrerer Felder</span><span class="sxs-lookup"><span data-stu-id="52ae7-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="52ae7-112">Bestimmen des Bearbeitungsmodus</span><span class="sxs-lookup"><span data-stu-id="52ae7-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="52ae7-113">Verwenden von AddNew im sofort-und Batch Modus</span><span class="sxs-lookup"><span data-stu-id="52ae7-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

