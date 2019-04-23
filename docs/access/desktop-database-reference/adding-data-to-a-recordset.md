---
title: Hinzufügen von Daten zu einem Recordset
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280216"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="3e716-102">Hinzufügen von Daten zu einem Recordset</span><span class="sxs-lookup"><span data-stu-id="3e716-102">Adding data to a Recordset</span></span>

<span data-ttu-id="3e716-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e716-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e716-p101">Das **Recordset** -Objekt ist wahrscheinlich das am häufigsten verwendete ADO-Objekt. In ADO stellt man sich ein **Recordset** -Objekt am besten als Kombination eines Resultsets aus einer Datenquelle und der zugehörigen Cursorverhalten vor. Auf diese Weise können Sie Daten in ein **Recordset** -Objekt eingeben und dann mit den Methoden und Eigenschaften des **Recordset** -Objekts in den Datenzeilen navigieren, die Werte in den Zeilen anzeigen sowie das Resultset anderweitig bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3e716-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="3e716-p102">Dieser Abschnitt befasst sich mit dem Hinzufügen von Daten zum **Recordset** -Objekt. Informationen zum Navigieren in den Daten oder zum Aktualisieren der Daten finden Sie in [Kapitel 4: Bearbeiten von Daten](chapter-4-editing-data.md) und [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md). Sie benötigen nicht immer die erweiterten Funktionen eines **Command** -Objekts, um einem **Recordset** -Objekt das Resultset hinzuzufügen. In vielen Fällen können Sie den Befehl ausführen, indem Sie die **Source** -Eigenschaft im **Recordset** -Objekt festlegen oder aber eine Befehlszeichenfolge an die **Open** -Methode des **Recordset** -Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="3e716-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="3e716-p103">Es gibt verschiedene Möglichkeiten, um Daten aus der Datenquelle einem **Recordset** -Objekt hinzuzufügen. Die verwendete Technik hängt von den Anforderungen Ihrer Anwendung und der angebotenen Funktionalität des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="3e716-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

