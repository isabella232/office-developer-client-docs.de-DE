---
title: Bearbeiten vorhandener Datensätze
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dae80ddb85709ccc668e80adad0cb0c723c79cd5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710860"
---
# <a name="editing-existing-records"></a><span data-ttu-id="b06c3-102">Bearbeiten vorhandener Datensätze</span><span class="sxs-lookup"><span data-stu-id="b06c3-102">Editing existing records</span></span>


<span data-ttu-id="b06c3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b06c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b06c3-p101">Zum Bearbeiten vorhandener Datensätze wechseln Sie zu der Zeile, die Sie bearbeiten möchten, und ändern Sie die **Value** -Eigenschaft der Felder, die Sie bearbeiten möchten. Weitere Informationen zur **Value** -Eigenschaft des **Field** -Objekts finden Sie in [Kapitel 3: Untersuchen von Daten](chapter-3-examining-data.md). In Abhängigkeit vom Cursortyp verwenden Sie **Update** oder **UpdateBatch**, um Änderungen an die Datenquelle zurückzusenden. Weitere Informationen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="b06c3-p101">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change. For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md). Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source. For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="b06c3-p102">Gewöhnlich ist es effizienter, eine gespeicherte Prozedur mit einem Befehlsobjekt zu verwenden, um Aktualisierungen vorzunehmen sowie um andere Vorgänge auszuführen, da für eine gespeicherte Prozedur kein Cursor erstellt werden muss. Weitere Informationen zu Cursorn finden Sie in [Kapitel 8: Grundlegendes zu Cursorn und Sperren](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="b06c3-p102">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor. For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

