---
title: TransferSQLDatenbank-Makroaktion
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff903c459a351f69b272224ca29f9cc717498f0a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996853"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="a577b-102">TransferSQLDatenbank-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="a577b-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="a577b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a577b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a577b-104">Verwenden Sie in einem Access-Projekt die **TransferSQLDatenbank** -Aktion, um eine Microsoft SQL Server-Datenbank der Version 7.0 oder höher zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="a577b-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="a577b-105">Weitere Informationen zum Transferieren einer Datenbank finden Sie in der Dokumentation zu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a577b-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="a577b-106">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="a577b-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="a577b-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a577b-107">Setting</span></span>

<span data-ttu-id="a577b-108">Die **TransferSQLDatenbank** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a577b-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a577b-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="a577b-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a577b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a577b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a577b-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-112">Der Name des Datenbankservers mit SQL Server 7.0 oder höher, auf den Sie Daten kopieren.</span><span class="sxs-lookup"><span data-stu-id="a577b-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a577b-113"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-114">Der Name der neuen Datenbank, die auf dem Zielserver erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a577b-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a577b-115"><strong>Vertrauenswürdige Verbindung verwenden</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-116">Gibt an ist, ob eine vertrauenswürdige Verbindung zu SQL Server nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a577b-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="a577b-117">Wenn legen Sie auf <strong>Ja</strong>, und klicken Sie dann eine vertrauenswürdige Verbindung vorhanden ist und die Argumente <strong>Benutzername</strong> und <strong>Kennwort</strong> nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a577b-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="a577b-118">Wenn Sie auf <strong>Nein</strong>, den <strong>Benutzernamen</strong> und <strong>das Kennwort</strong> Argumente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a577b-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="a577b-119">Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a577b-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="a577b-120">Wenn Sie eine vertrauenswürdige Verbindung verwenden, ist SQL Server-Sicherheit in die Sicherheit des Betriebssystems Windows anzugebende eine einzige Anmeldung am Netzwerk und die Datenbank integriert.</span><span class="sxs-lookup"><span data-stu-id="a577b-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a577b-121"><strong>Benutzername</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-122">Der Anmeldename für den Zielserver.</span><span class="sxs-lookup"><span data-stu-id="a577b-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a577b-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-p103">Das Kennwort für das Argument <strong>Benutzername</strong>. Dieses Kennwort wird als Text im Access-Projekt gespeichert, bleibt während des Datenbanktransfers jedoch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="a577b-p103">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a577b-126"><strong>Auch Daten kopieren</strong></span><span class="sxs-lookup"><span data-stu-id="a577b-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="a577b-p104">Gibt an, ob Daten in den Datenbanktransfer eingeschlossen sind. Wenn das Argument auf <strong>Ja</strong> festgelegt ist, werden alle Daten aller Tabellen sowie alle Datenstrukturen, erweiterten Eigenschaften und Datenbankobjekte eingeschlossen. Ist das Argument auf <strong>Nein</strong> festgelegt, werden keine Daten aus den Tabellen eingeschlossen. Auf dem Zielserver werden nur die Tabellenstruktur und die erweiterten Eigenschaften erstellt sowie alle sonstigen Datenbankobjekte (außer Datenbankdiagramme). Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a577b-p104">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a577b-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a577b-132">Remarks</span></span>

<span data-ttu-id="a577b-133">Während des Datenbanktransfers können keine weiteren Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a577b-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="a577b-134">Die **TransferSQLDatenbank** -Aktion kopiert standardmäßig Daten, Datendefinitionen, Datenbankobjekte und erweiterte Eigenschaften, wie Standardwerte, Gültigkeitsmeldungseinschränkungen und Nachschlagewerte.</span><span class="sxs-lookup"><span data-stu-id="a577b-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="a577b-135">Voraussetzungen für das Transferieren einer Datenbank:</span><span class="sxs-lookup"><span data-stu-id="a577b-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="a577b-136">Sie müssen auf dem Zielserver ein Mitglied der Rolle sysadmin sein. (Auf dem Quellserver ist keine spezielle Rolle erforderlich.)</span><span class="sxs-lookup"><span data-stu-id="a577b-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="a577b-137">Der aktuelle SQL Server, der mit dem Access-Projekt verbunden ist, und der Zielserver, an den Sie die Datenbank transferieren, müssen SQL Server, Version 7.0 oder höher, sein.</span><span class="sxs-lookup"><span data-stu-id="a577b-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a577b-138">[!HINWEIS] Verbindungsserver werden während eines Datenbanktransfers nicht transferiert.</span><span class="sxs-lookup"><span data-stu-id="a577b-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="a577b-139">Verwenden Sie die **TransferSQLDatabase** -Methode des **DoCmd** -Objekts, um die **TransferSQLDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a577b-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

