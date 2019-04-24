---
title: CopyDatabaseFile-Makroaktion
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3c98d8795bb7039c0ae158414401dc5d754066f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295499"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="748a5-102">CopyDatabaseFile-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="748a5-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="748a5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="748a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="748a5-104">Sie können die **KopierenDatenbankdatei**-Aktion verwenden, um eine Kopie der aktuellen Microsoft SQL Server 7.0-Datenbank oder einer neueren Datenbank anzulegen, die mit Ihrem Access-Projekt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="748a5-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="748a5-105">Access trennt die aktuelle Datenbank und fügt Sie dann an den Zielserver an.</span><span class="sxs-lookup"><span data-stu-id="748a5-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="748a5-106">Weitere Informationen zum Trennen und Verbinden einer Datenbank finden Sie in der SQL Server-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="748a5-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="748a5-107">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="748a5-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="748a5-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="748a5-108">Setting</span></span>

<span data-ttu-id="748a5-109">Die **KopierenDatenbankdatei**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="748a5-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748a5-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="748a5-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="748a5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="748a5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748a5-112"><strong>Datenbankname</strong></span><span class="sxs-lookup"><span data-stu-id="748a5-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="748a5-p102">Der Name der neuen Masterdatendatei. Der Standardpfad der Datei ist der aktuelle Speicherort der Access-Projektdatei (ADP).</span><span class="sxs-lookup"><span data-stu-id="748a5-p102">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a5-115"><strong>Datei überschreiben</strong></span><span class="sxs-lookup"><span data-stu-id="748a5-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="748a5-p103">Gibt an, ob eine vorhandene Datei mit demselben Namen ersetzt werden soll. Wenn <strong>Ja</strong> festgelegt und der Dateiname bereits vorhanden ist, wird die Datei überschrieben. Wenn <strong>Nein</strong> festgelegt und der Dateiname bereits vorhanden ist, wird die Datei nicht überschrieben, und die Aktion schlägt fehl. Wenn die Datei noch nicht vorhanden ist, wird diese Einstellung ignoriert. Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="748a5-p103">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a5-121"><strong>Alle Verbindungen trennen</strong></span><span class="sxs-lookup"><span data-stu-id="748a5-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="748a5-122">Gibt an, ob Access das Trennen von Datenbankverbindungen erzwingen sollte.</span><span class="sxs-lookup"><span data-stu-id="748a5-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="748a5-123">Wenn <strong>Ja</strong> festgelegt ist, werden alle Verbindungen mit der aktuellen Datenbank getrennt, damit das Kopieren der Datenbank fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="748a5-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="748a5-124">Wenn <strong>Nein</strong> festgelegt ist und mindestens eine Verbindung zur Datenbank besteht, schlägt das Kopieren der Datenbank fehl.</span><span class="sxs-lookup"><span data-stu-id="748a5-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="748a5-125">Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="748a5-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="748a5-126"><strong>Warnung</strong>: das Trennen von Benutzern aus einer Datenbank ohne ausreichende Warnung kann zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="748a5-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="748a5-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="748a5-127">Remarks</span></span>

<span data-ttu-id="748a5-128">Der Kopiervorgang läuft synchron ab. Daher können Sie andere Vorgänge erst ausführen, wenn das Kopieren der Datenbank abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="748a5-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="748a5-129">Die **KopierenDatenbankdatei**-Aktion kopiert nicht nur Daten, Datendefinitionen und Datenbankobjekte, sondern auch erweiterte Eigenschaften wie Standardwerte, Texteinschränkungen und Nachschlagewerte.</span><span class="sxs-lookup"><span data-stu-id="748a5-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="748a5-130">Voraussetzungen für das Kopieren einer Datenbank:</span><span class="sxs-lookup"><span data-stu-id="748a5-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="748a5-131">Sie müssen vor dem Kopieren der Datenbankdatei alle Anwendungen und Benutzer trennen.</span><span class="sxs-lookup"><span data-stu-id="748a5-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="748a5-132">Alle Objekte und Sichten mit Ausnahme des Navigationsbereichs müssen geschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="748a5-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="748a5-133">Die aktuelle Datenbank darf nicht repliziert sein.</span><span class="sxs-lookup"><span data-stu-id="748a5-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="748a5-134">Bei der Quellserverdatenbank muss es sich um Microsoft SQL Server, Version 7.0 oder höher, oder SQL Server 2000 Desktop Engine handeln, die auf einem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="748a5-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="748a5-135">Bei der SQL Server-Datenbank auf dem Quellserver muss es sich um eine einzelne Dateidatenbank handeln.</span><span class="sxs-lookup"><span data-stu-id="748a5-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="748a5-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span><span class="sxs-lookup"><span data-stu-id="748a5-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="748a5-137">Verwenden Sie die **CopyDatabaseFile**-Methode des **DoCmd**-Objekts, um die **KopierenDatenbankdatei**-Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="748a5-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

