---
title: Microsoft OLE DB-Anbieter für Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288925"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="08636-102">Microsoft OLE DB-Anbieter für Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="08636-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="08636-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08636-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08636-104">Mithilfe des OLE DB-Anbieters für Microsoft Jet kann ADO auf Microsoft Jet-Datenbanken zugreifen.</span><span class="sxs-lookup"><span data-stu-id="08636-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="08636-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="08636-105">Connection String Parameters</span></span>

<span data-ttu-id="08636-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider*-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="08636-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="08636-107">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08636-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="08636-108">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="08636-108">Typical Connection String</span></span>

<span data-ttu-id="08636-109">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="08636-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="08636-110">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="08636-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-111">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="08636-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="08636-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08636-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="08636-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="08636-114">Gibt den OLE DB-Anbieter für Microsoft Jet an.</span><span class="sxs-lookup"><span data-stu-id="08636-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="08636-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="08636-116">Gibt den Pfad und den Dateinamen der Datenbank an (z. B. c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="08636-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="08636-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="08636-118">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="08636-118">Specifies the user name.</span></span> <span data-ttu-id="08636-119">Wenn dieses Schlüsselwort nicht angegeben ist, wird die &quot;Zeichen&quot;Folge "admin" standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="08636-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="08636-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="08636-121">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="08636-121">Specifies the user password.</span></span> <span data-ttu-id="08636-122">Wenn dieses Schlüsselwort nicht angegeben ist, wird die leere&quot;&quot;Zeichenfolge () standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="08636-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="08636-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="08636-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="08636-p103">Der OLE DB-Anbieter für Microsoft Jet unterstützt neben den von ADO definierten auch mehrere anbieterspezifische dynamische Eigenschaften. Diese können wie alle anderen **Connection**-Parameter über die **Properties**-Auflistung des **Connection**-Objekts oder als Teil der Verbindungszeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08636-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="08636-126">In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="08636-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="08636-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="08636-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08636-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-129">Jet OLEDB: Compact reclaimed Space Amount</span><span class="sxs-lookup"><span data-stu-id="08636-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="08636-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="08636-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="08636-p104">Gibt einen Schätzwert für den Speicherplatz in Bytes an, der durch Komprimieren der Datenbank verfügbar gemacht werden kann. Dieser Wert ist erst dann gültig, wenn eine Datenbankverbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08636-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-133">Jet OLEDB: Connection Control</span><span class="sxs-lookup"><span data-stu-id="08636-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="08636-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="08636-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="08636-135">Gibt an, ob Benutzer eine Verbindung mit der Datenbank herstellen können.</span><span class="sxs-lookup"><span data-stu-id="08636-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-136">Jet OLEDB: Create System Database</span><span class="sxs-lookup"><span data-stu-id="08636-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="08636-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="08636-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="08636-138">Gibt an, ob beim Erstellen einer neuen Datenquelle eine Systemdatenbank erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="08636-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-139">Jet OLEDB: Daten Bank Sperrmodus</span><span class="sxs-lookup"><span data-stu-id="08636-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="08636-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="08636-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="08636-141">Gibt den Sperrmodus für diese Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="08636-141">Indicates the locking mode for this database.</span></span> <span data-ttu-id="08636-142">Der erste Benutzer, der die Datenbank öffnet, legt den Modus fest, der verwendet wird, solange die Datenbank geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="08636-142">The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="08636-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="08636-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="08636-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="08636-145">Gibt das Datenbankkennwort an.</span><span class="sxs-lookup"><span data-stu-id="08636-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="08636-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="08636-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="08636-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="08636-148">Gibt an, ob Jet beim Komprimieren einer Datenbank Gebietsschemainformationen kopieren soll.</span><span class="sxs-lookup"><span data-stu-id="08636-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="08636-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="08636-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="08636-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="08636-p106">Gibt an, ob eine komprimierte Datenbank verschlüsselt werden soll. Wenn diese Eigenschaft nicht festgelegt ist, wird die komprimierte Datenbank verschlüsselt, sofern die ursprüngliche Datenbank ebenfalls verschlüsselt war.</span><span class="sxs-lookup"><span data-stu-id="08636-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="08636-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="08636-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="08636-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="08636-155">Gibt das Speichermodul an, das für Zugriff auf den aktuellen Datenspeicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08636-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="08636-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="08636-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="08636-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="08636-p107">Gibt die maximale Zeitdauer in Millisekunden an, für die Jet asynchrone Schreibvorgänge auf Datenträger verzögern kann, wenn die Datenbank exklusiv geöffnet ist. Diese Eigenschaft wird ignoriert, es sei denn <strong>Jet OLEDB: Flush Transaction Timeout</strong> ist auf 0 festgelegt.  </span><span class="sxs-lookup"><span data-stu-id="08636-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="08636-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="08636-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="08636-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="08636-p108">Gibt die Zeitdauer an, die gewartet wird, bevor Daten in einem Cache für asynchrones Schreiben tatsächlich auf den Datenträger geschrieben wird. Mit dieser Einstellung werden die Werte für <strong>Jet OLEDB:Shared Async Delay</strong> und <strong>Jet OLEDB:Exclusive Async Delay</strong> außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="08636-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-164">Jet OLEDB: globale Massentransaktionen</span><span class="sxs-lookup"><span data-stu-id="08636-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="08636-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="08636-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="08636-166">Gibt an, ob SQL-Massentransaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08636-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-167">Jet OLEDB: Global Partial Bulk OPS</span><span class="sxs-lookup"><span data-stu-id="08636-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="08636-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="08636-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="08636-169">Gibt das Kennwort an, das zum Öffnen der Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08636-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="08636-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="08636-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="08636-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="08636-172">Gibt an, ob Änderungen, die an internen impliziten Transaktionen vorgenommen wurden, im synchronen oder asynchronen Modus geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08636-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="08636-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="08636-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="08636-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="08636-175">Gibt die Zeitdauer in Millisekunden an, die gewartet werden muss, bevor nach einem gescheiterten Versuch erneut versucht wird, eine Sperre zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="08636-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="08636-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="08636-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="08636-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="08636-178">Gibt an, wie häufig der Versuch, auf eine gesperrte Seite zuzugreifen, wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="08636-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="08636-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="08636-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="08636-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="08636-181">Gibt den maximalen Speicherplatz in Kilobytes an, den Jet nutzen kann, bevor Änderungen auf den Datenträger geleert werden.</span><span class="sxs-lookup"><span data-stu-id="08636-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="08636-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="08636-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="08636-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="08636-184">Gibt die maximale Anzahl von Sperren an, die Jet in einer Datenbank setzen kann.</span><span class="sxs-lookup"><span data-stu-id="08636-184">Indicates the maximum number of locks Jet can place on a database.</span></span> <span data-ttu-id="08636-185">Der Standardwert beträgt 9500.</span><span class="sxs-lookup"><span data-stu-id="08636-185">The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-186">Jet OLEDB: New Database Password</span><span class="sxs-lookup"><span data-stu-id="08636-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="08636-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="08636-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="08636-188">Gibt das neue Kennwort an, das für diese Datenbank festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="08636-188">Indicates the new password to be set for this database.</span></span> <span data-ttu-id="08636-189">Das alte Kennwort wird in <strong>Jet OLEDB:Database Password</strong> gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08636-189">The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-190">Jet OLEDB: ODBC Command Timeout</span><span class="sxs-lookup"><span data-stu-id="08636-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="08636-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="08636-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="08636-192">Gibt die Zeitdauer in Millisekunden an, die verstreicht, bevor eine ODBC-Remoteabfrage von Jet das Zeitlimit überschreitet.</span><span class="sxs-lookup"><span data-stu-id="08636-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-193">Jet OLEDB: Seitensperren für die Tabellensperre</span><span class="sxs-lookup"><span data-stu-id="08636-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="08636-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="08636-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="08636-p111">Gibt an, wie viele Seiten in einer Transaktion gesperrt werden müssen, bevor Jet versucht, die Sperre auf eine Tabellensperre höherzustufen. Wenn dieser Wert 0 ist, wird die Sperre nie höhergestuft.</span><span class="sxs-lookup"><span data-stu-id="08636-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="08636-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="08636-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="08636-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="08636-199">Gibt die Zeitdauer in Millisekunden an, die Jet abwartet, bevor geprüft wird, ob der Cache im Vergleich zur Datenbankdatei noch aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="08636-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="08636-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="08636-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="08636-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="08636-202">Gibt an, ob Jet BLOB-Seiten nach deren Freigabe auf aggressive Weise verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="08636-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="08636-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="08636-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="08636-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="08636-205">Gibt den Windows-Registrierungsschlüssel an, der die Werte für das Jet-Datenbankmodul enthält.</span><span class="sxs-lookup"><span data-stu-id="08636-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-206">Jet OLEDB: Reset ISAM stats</span><span class="sxs-lookup"><span data-stu-id="08636-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="08636-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="08636-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="08636-208">Gibt an, ob das Schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS die Leistungsindikatoren nach dem Zurückgeben von Leistungsinformationen zurücksetzen soll.</span><span class="sxs-lookup"><span data-stu-id="08636-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="08636-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="08636-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="08636-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="08636-211">Gibt die maximale Zeitdauer in Millisekunden an, für die Jet asynchrone Schreibvorgänge auf Datenträger verzögern kann, wenn die Datenbank für mehrere Benutzer geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="08636-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="08636-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="08636-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="08636-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="08636-214">Gibt den Pfad und den Dateinamen für die Arbeitsgruppen-Informationsdatei (Systemdatenbank) an.</span><span class="sxs-lookup"><span data-stu-id="08636-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-215">Jet OLEDB: Transaction Commit Mode</span><span class="sxs-lookup"><span data-stu-id="08636-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="08636-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="08636-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="08636-217">Gibt an, ob Jet Daten beim Ausführen einer Transaktion synchron oder asynchron auf Datenträger schreibt.</span><span class="sxs-lookup"><span data-stu-id="08636-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="08636-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="08636-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="08636-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="08636-220">Gibt an, ob Änderungen, die an Transaktionen vorgenommen wurden, im synchronen oder asynchronen Modus geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08636-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="08636-221">Anwenderspezifische Recordset- und Command-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08636-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="08636-p112">Der Jet-Anbieter unterstützt zudem auch mehrere anwenderspezifische **Recordset**- und **Command**-Eigenschaften. Diese Eigenschaften werden über die **Properties**-Auflistung der Objekte **Recordset** oder **Command** festgelegt. In der Tabelle ist der ADO-Eigenschaftenname sowie der entsprechende OLE DB-Eigenschaftenname in Klammern angegeben.</span><span class="sxs-lookup"><span data-stu-id="08636-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-225">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="08636-226">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08636-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-227">Jet OLEDB: Massentransaktionen</span><span class="sxs-lookup"><span data-stu-id="08636-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="08636-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="08636-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="08636-229">Gibt an, ob SQL-Massenvorgänge durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08636-229">Indicates whether SQL bulk operations are transacted.</span></span> <span data-ttu-id="08636-230">Umfangreiche Massenvorgänge können aufgrund von Ressourcenverzögerungen möglicherweise nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08636-230">Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-231">Jet OLEDB: enable FAT Cursors</span><span class="sxs-lookup"><span data-stu-id="08636-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="08636-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="08636-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="08636-233">Gibt an, ob Jet beim Auffüllen einer Datensatzgruppe für eine Remote-Datensatzherkunft mehrere Zeilen zwischenspeichern soll.</span><span class="sxs-lookup"><span data-stu-id="08636-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-234">Jet OLEDB: FAT Cursor Cache Größe</span><span class="sxs-lookup"><span data-stu-id="08636-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="08636-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="08636-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="08636-p114">Gibt die Anzahl von Zeilen an, die beim Zwischenspeichern von Zeilen von Remotedatenspeichern zwischengespeichert werden sollen. Dieser Wert wird nur beachtet, wenn <strong>Jet OLEDB:Enable Fat Cursors</strong> auf True gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="08636-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-238">Jet OLEDB: inkonsistent</span><span class="sxs-lookup"><span data-stu-id="08636-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="08636-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="08636-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="08636-240">Gibt an, ob in Abfrageergebnissen inkonsistente Aktualisierungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="08636-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-241">Jet OLEDB: Sperrgranularität</span><span class="sxs-lookup"><span data-stu-id="08636-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="08636-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="08636-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="08636-243">Gibt an, ob eine Tabelle mithilfe von Sperren auf Zeilenebene geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="08636-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-244">Jet OLEDB: ODBC-Passthrough-Anweisung</span><span class="sxs-lookup"><span data-stu-id="08636-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="08636-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="08636-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="08636-246">Gibt an, dass Jet den SQL-Text in einem <strong>Command</strong>-Objekt unverändert an das Back-End übergeben muss.</span><span class="sxs-lookup"><span data-stu-id="08636-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-247">Jet OLEDB: Partial Bulk OPS</span><span class="sxs-lookup"><span data-stu-id="08636-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="08636-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="08636-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="08636-249">Gibt das Verhalten von Jet für den Fall an, dass SQL DML-Vorgänge nicht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="08636-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-250">Jet OLEDB: Durchlauf-Abfrage-BULK-OP</span><span class="sxs-lookup"><span data-stu-id="08636-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="08636-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="08636-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="08636-252">Gibt an, ob Abfragen, die kein <strong>Recordset</strong>-Objekt zurückgeben, unverändert an die Datenquelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="08636-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-253">Jet OLEDB: Durchlauf-Abfrage-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="08636-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="08636-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="08636-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="08636-p115">Gibt die Jet-Verbindungszeichenfolge an, die für die Verbindung mit einem Remotedatenspeicher verwendet wird. Dieser Wert wird nur beachtet, wenn <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> auf True gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="08636-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-257">Jet OLEDB: gespeicherte Abfrage</span><span class="sxs-lookup"><span data-stu-id="08636-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="08636-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="08636-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="08636-259">Gibt an, ob der Befehlstext nicht als SQL-Befehl, sondern als gespeicherte Abfrage interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="08636-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-260">Jet OLEDB: Validate Rules on Set</span><span class="sxs-lookup"><span data-stu-id="08636-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="08636-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="08636-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="08636-262">Gibt an, ob die Jet-Gültigkeitsregeln beim Festlegen der Spaltendaten oder bei der Übergabe der Änderungen an die Datenbank ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="08636-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="08636-p116">Der OLE DB-Anbieter für Microsoft Jet öffnet Microsoft Jet-Datenbanken standardmäßig im Lese-/Schreibmodus. Um eine Datenbank im schreibgeschützten Modus zu öffnen, legen Sie die [Mode](mode-property-ado.md)-Eigenschaft im ADO-Objekt **Connection** auf **adModeRead** fest.</span><span class="sxs-lookup"><span data-stu-id="08636-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="08636-265">Verwendung des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="08636-265">Command Object Usage</span></span>

<span data-ttu-id="08636-p117">Für Befehlstext im [Command](command-object-ado.md)-Objekt wird der Microsoft Jet SQL-Dialekt verwendet. Sie können im Befehlstext Abfragen, die Zeilen zurückgeben, Aktionsabfragen und Tabellennamen angeben. Gespeicherte Prozeduren werden jedoch nicht unterstützt und dürfen nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08636-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="08636-268">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="08636-268">Recordset Behavior</span></span>

<span data-ttu-id="08636-p118">Das Microsoft Jet-Datenbankmodul unterstützt keine dynamischen Cursor. Daher unterstützt der OLE DB-Anbieter für Microsoft Jet den **adLockDynamic**-Cursortyp nicht. Wenn ein dynamischer Cursor angefordert wird, gibt der Anbieter einen Keyset-Cursor zurück und setzt die [CursorType](cursortype-property-ado.md)-Eigenschaft zurück, um den Typ des zurückgegebenen [Recordset](recordset-object-ado.md)-Objekts anzugeben. Wenn ein aktualisierbares **Recordset**-Objekt angefordert wird (**LockType** ist auf **adLockOptimistic**, **adLockBatchOptimistic** oder **adLockPessimistic** gesetzt), gibt der Anbieter ebenfalls einen Keyset-Cursor zurück und setzt die **CursorType**-Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="08636-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="08636-273">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08636-273">Dynamic Properties</span></span>

<span data-ttu-id="08636-274">Der OLE DB-Anbieter für Microsoft Jet fügt verschiedene Eigenschaften in die **Properties**-Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="08636-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="08636-p119">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="08636-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="08636-279">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="08636-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="08636-280">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Connection**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="08636-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-281">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="08636-282">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="08636-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="08636-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="08636-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="08636-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="08636-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="08636-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="08636-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="08636-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="08636-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="08636-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="08636-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="08636-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="08636-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="08636-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="08636-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="08636-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="08636-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="08636-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="08636-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="08636-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="08636-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="08636-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="08636-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="08636-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="08636-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="08636-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="08636-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="08636-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="08636-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="08636-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="08636-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="08636-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="08636-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="08636-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="08636-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="08636-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="08636-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="08636-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="08636-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="08636-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="08636-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="08636-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="08636-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="08636-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="08636-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="08636-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="08636-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="08636-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="08636-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="08636-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="08636-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="08636-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="08636-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="08636-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="08636-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="08636-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="08636-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="08636-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="08636-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="08636-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="08636-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="08636-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="08636-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="08636-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="08636-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="08636-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="08636-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="08636-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="08636-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-329">Mode</span><span class="sxs-lookup"><span data-stu-id="08636-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="08636-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="08636-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="08636-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="08636-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="08636-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="08636-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="08636-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="08636-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="08636-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="08636-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="08636-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="08636-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="08636-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="08636-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="08636-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="08636-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="08636-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="08636-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="08636-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="08636-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="08636-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="08636-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="08636-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="08636-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="08636-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="08636-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="08636-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="08636-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="08636-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="08636-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="08636-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="08636-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="08636-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="08636-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="08636-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="08636-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-355">Password</span><span class="sxs-lookup"><span data-stu-id="08636-355">Password</span></span></p></td>
<td><p><span data-ttu-id="08636-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="08636-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="08636-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="08636-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="08636-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="08636-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="08636-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="08636-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="08636-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="08636-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="08636-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="08636-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="08636-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="08636-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="08636-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="08636-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="08636-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="08636-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="08636-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="08636-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="08636-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="08636-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="08636-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="08636-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="08636-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="08636-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="08636-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="08636-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="08636-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="08636-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="08636-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="08636-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="08636-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="08636-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="08636-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="08636-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="08636-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="08636-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="08636-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="08636-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="08636-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="08636-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="08636-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="08636-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="08636-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="08636-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="08636-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="08636-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="08636-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="08636-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="08636-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="08636-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="08636-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-391">User ID</span><span class="sxs-lookup"><span data-stu-id="08636-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="08636-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="08636-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-393">User Name</span><span class="sxs-lookup"><span data-stu-id="08636-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="08636-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="08636-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="08636-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="08636-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="08636-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="08636-397">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="08636-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="08636-398">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Recordset**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="08636-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-399">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="08636-400">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="08636-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="08636-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="08636-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="08636-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="08636-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="08636-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="08636-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="08636-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="08636-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="08636-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="08636-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="08636-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="08636-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="08636-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="08636-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="08636-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="08636-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="08636-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="08636-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="08636-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="08636-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="08636-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="08636-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="08636-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="08636-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="08636-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="08636-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="08636-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="08636-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="08636-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="08636-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="08636-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="08636-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="08636-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="08636-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="08636-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="08636-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="08636-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="08636-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="08636-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="08636-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="08636-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="08636-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="08636-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="08636-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="08636-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="08636-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="08636-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="08636-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="08636-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="08636-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="08636-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="08636-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="08636-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="08636-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="08636-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="08636-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="08636-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="08636-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="08636-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="08636-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="08636-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="08636-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="08636-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="08636-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="08636-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="08636-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="08636-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="08636-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="08636-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="08636-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="08636-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="08636-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="08636-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="08636-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="08636-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="08636-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="08636-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="08636-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="08636-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="08636-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="08636-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="08636-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="08636-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="08636-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="08636-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="08636-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="08636-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="08636-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-466">IStream</span><span class="sxs-lookup"><span data-stu-id="08636-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="08636-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="08636-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="08636-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="08636-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="08636-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="08636-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="08636-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="08636-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="08636-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="08636-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="08636-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="08636-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="08636-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="08636-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="08636-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="08636-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="08636-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="08636-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="08636-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="08636-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="08636-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="08636-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="08636-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="08636-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="08636-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="08636-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="08636-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="08636-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="08636-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="08636-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="08636-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="08636-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="08636-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="08636-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="08636-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="08636-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="08636-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="08636-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="08636-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="08636-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="08636-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="08636-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="08636-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="08636-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="08636-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="08636-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="08636-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="08636-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="08636-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="08636-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="08636-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="08636-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="08636-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="08636-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="08636-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="08636-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="08636-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="08636-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="08636-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="08636-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="08636-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="08636-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="08636-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="08636-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="08636-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="08636-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="08636-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="08636-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="08636-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="08636-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="08636-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="08636-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="08636-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="08636-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="08636-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="08636-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="08636-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="08636-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="08636-544">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="08636-544">Command Dynamic Properties</span></span>

<span data-ttu-id="08636-545">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Command**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="08636-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08636-546">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="08636-547">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="08636-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08636-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="08636-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="08636-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="08636-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="08636-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="08636-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="08636-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="08636-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="08636-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="08636-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="08636-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="08636-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="08636-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="08636-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="08636-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="08636-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="08636-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="08636-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="08636-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="08636-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="08636-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="08636-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="08636-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="08636-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="08636-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="08636-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="08636-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="08636-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="08636-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="08636-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="08636-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="08636-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="08636-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="08636-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="08636-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="08636-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="08636-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="08636-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="08636-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="08636-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="08636-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="08636-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="08636-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="08636-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="08636-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="08636-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="08636-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="08636-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="08636-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="08636-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="08636-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="08636-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="08636-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="08636-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="08636-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="08636-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="08636-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="08636-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="08636-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="08636-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="08636-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="08636-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="08636-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="08636-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="08636-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="08636-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="08636-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="08636-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="08636-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="08636-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="08636-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="08636-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="08636-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="08636-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="08636-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="08636-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="08636-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="08636-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="08636-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="08636-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="08636-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="08636-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-607">IStream</span><span class="sxs-lookup"><span data-stu-id="08636-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="08636-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="08636-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="08636-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="08636-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="08636-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="08636-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="08636-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="08636-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="08636-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="08636-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="08636-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="08636-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="08636-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="08636-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="08636-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="08636-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="08636-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="08636-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="08636-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="08636-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="08636-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="08636-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="08636-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="08636-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="08636-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="08636-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="08636-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="08636-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="08636-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="08636-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="08636-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="08636-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="08636-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="08636-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="08636-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="08636-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="08636-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="08636-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="08636-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="08636-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="08636-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="08636-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="08636-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="08636-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="08636-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="08636-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="08636-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="08636-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="08636-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="08636-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="08636-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="08636-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="08636-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="08636-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="08636-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="08636-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="08636-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="08636-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="08636-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="08636-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="08636-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="08636-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="08636-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="08636-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="08636-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="08636-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="08636-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="08636-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="08636-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="08636-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="08636-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="08636-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="08636-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="08636-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="08636-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="08636-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="08636-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="08636-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="08636-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="08636-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="08636-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="08636-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="08636-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="08636-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08636-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="08636-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="08636-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="08636-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08636-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="08636-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="08636-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="08636-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="08636-687">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08636-687">See also</span></span>

<span data-ttu-id="08636-688">Weitere Informationen zur Implementierung und zur Funktionsweise des OLE DB-Anbieters für Microsoft Jet finden Sie in der Dokumentation zum OLE DB-Anbieter für Microsoft Jet im MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="08636-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

