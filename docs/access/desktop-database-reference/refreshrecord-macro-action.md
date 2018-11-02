---
title: RefreshRecord-Makroaktion
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4b7ec534579b070d342fe2efd80af44e2ea921ef
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927270"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="fa3ad-102">RefreshRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="fa3ad-102">RefreshRecord macro action</span></span>


<span data-ttu-id="fa3ad-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa3ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa3ad-104">Mit der **DatensatzAktualisieren** -Aktion können Sie die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3ad-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa3ad-105">Remarks</span></span>

<span data-ttu-id="fa3ad-p101">Mit der **DatensatzAktualisieren** -Aktion werden nur Änderungen an Datensätzen in der aktuellen Gruppe angezeigt. Da die Datenbank mit der **DatensatzAktualisieren** -Aktion nicht erneut abgefragt wird, werden in die aktuelle Gruppe keine Datensätze aufgenommen, die hinzugefügt wurden, oder Datensätze daraus entfernt, die gelöscht wurden, seit die Datenbank das letzte Mal abgefragt wurde. Zudem werden Datensätze, die nicht mehr den Kriterien der Abfrage oder des Filters entsprechen, nicht entfernt. Wenn Sie eine erneute Abfrage der Datenbank ausführen möchten, verwenden Sie die **[AktualisierenDaten](requery-macro-action.md)** -Methode. Wenn die Datenquelle für ein Formular erneut abgefragt wird, entspricht die aktuelle Gruppe von Datensätze den gesamten Daten in der Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="fa3ad-110">Das Verhalten dieser Makroaktion hängt davon ab, ob Sie diese in einer Clientdatenbank oder einer Webdatenbank abfragen.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="fa3ad-111">Clientdatenbank</span><span class="sxs-lookup"><span data-stu-id="fa3ad-111">Client database</span></span>

<span data-ttu-id="fa3ad-p102">In einer Clientdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Daten in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer in einer Mehrbenutzerumgebung. Dies entspricht der **[Aktualisieren](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** -Methode.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** method.</span></span>

<span data-ttu-id="fa3ad-115">Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Clientdatenbank Folgendes ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="fa3ad-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="fa3ad-p103">Die Datensatzquelle für das aktive Formular oder Datenblatt wird mit den Änderungen an Zeilen in der aktuellen Gruppe aktualisiert. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="fa3ad-118">Aktualisiert die aktuelle Gruppe, um die Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="fa3ad-119">Wenn eine Zeile in der Datenquelle gelöscht wurde, wird es geändert, um anzeigen \#gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="fa3ad-120">Aktualisiert das aktive Formular oder Datenblatt, um alle geänderten Datensätze und alle \#Datensätze, die in der aktuellen Gruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="fa3ad-121">Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="fa3ad-122">Webdatenbank</span><span class="sxs-lookup"><span data-stu-id="fa3ad-122">Web database</span></span>

<span data-ttu-id="fa3ad-p105">In einer Webdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="fa3ad-125">Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Webdatenbank Folgendes ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="fa3ad-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="fa3ad-p106">Für alle Basistabellen in der aktuellen Gruppe werden Änderungen vom Server abgerufen. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="fa3ad-128">Aktualisiert die aktuelle Gruppe, um die Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="fa3ad-129">Wenn eine Zeile in der aktuellen Gruppe gelöscht wurde, wird es geändert, um anzeigen \#gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="fa3ad-130">Aktualisiert das aktive Formular oder Datenblatt an alle geänderten Datensätze und alle \#Datensätze, die in der aktuellen Gruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="fa3ad-131">Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.</span><span class="sxs-lookup"><span data-stu-id="fa3ad-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

