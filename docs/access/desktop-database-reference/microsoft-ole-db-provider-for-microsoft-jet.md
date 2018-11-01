---
title: Microsoft OLE DB-Anbieter für Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39cb1288ef5e6be4f50d4ef976725122635db1dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884086"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="1f56d-102">Microsoft OLE DB-Anbieter für Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="1f56d-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="1f56d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f56d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f56d-104">Mithilfe des OLE DB-Anbieters für Microsoft Jet kann ADO auf Microsoft Jet-Datenbanken zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1f56d-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="1f56d-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="1f56d-105">Connection String Parameters</span></span>

<span data-ttu-id="1f56d-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="1f56d-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="1f56d-107">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f56d-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="1f56d-108">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1f56d-108">Typical Connection String</span></span>

<span data-ttu-id="1f56d-109">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="1f56d-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="1f56d-110">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="1f56d-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-111">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="1f56d-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="1f56d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f56d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="1f56d-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="1f56d-114">Gibt den OLE DB-Anbieter für Microsoft Jet an.</span><span class="sxs-lookup"><span data-stu-id="1f56d-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="1f56d-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="1f56d-116">Gibt den Pfad und den Dateinamen der Datenbank an (z. B. c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="1f56d-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="1f56d-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="1f56d-118">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="1f56d-118">Specifies the user name.</span></span> <span data-ttu-id="1f56d-119">Wenn dieses Schlüsselwort nicht angegeben ist, wird die Zeichenfolge &quot;Admin&quot;, wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f56d-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="1f56d-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="1f56d-121">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="1f56d-121">Specifies the user password.</span></span> <span data-ttu-id="1f56d-122">Wenn dieses Schlüsselwort nicht angegeben ist, die leere Zeichenfolge (&quot;&quot;), wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f56d-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="1f56d-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="1f56d-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="1f56d-p103">Der OLE DB-Anbieter für Microsoft Jet unterstützt neben den von ADO definierten auch mehrere anbieterspezifische dynamische Eigenschaften. Diese können wie alle anderen **Connection** -Parameter über die **Properties** -Auflistung des **Connection** -Objekts oder als Teil der Verbindungszeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="1f56d-126">In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f56d-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f56d-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1f56d-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f56d-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-129">Jet OLEDB:Compact freigegebenen Speicherplatz Betrag</span><span class="sxs-lookup"><span data-stu-id="1f56d-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="1f56d-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p104">Gibt einen Schätzwert für den Speicherplatz in Bytes an, der durch Komprimieren der Datenbank verfügbar gemacht werden kann. Dieser Wert ist erst dann gültig, wenn eine Datenbankverbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-133">Jet OLEDB:Connection-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1f56d-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="1f56d-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="1f56d-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-135">Gibt an, ob Benutzer eine Verbindung mit der Datenbank herstellen können.</span><span class="sxs-lookup"><span data-stu-id="1f56d-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-136">Jet OLEDB: Systemdatenbank erstellen</span><span class="sxs-lookup"><span data-stu-id="1f56d-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="1f56d-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-138">Gibt an, ob beim Erstellen einer neuen Datenquelle eine Systemdatenbank erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="1f56d-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-139">Jet OLEDB: Database Sperrmodus</span><span class="sxs-lookup"><span data-stu-id="1f56d-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="1f56d-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p105">Gibt den Sperrmodus für diese Datenbank an. Der erste Benutzer, der die Datenbank öffnet, legt den Modus fest, der verwendet wird, solange die Datenbank geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="1f56d-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="1f56d-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="1f56d-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-145">Gibt das Datenbankkennwort an.</span><span class="sxs-lookup"><span data-stu-id="1f56d-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="1f56d-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="1f56d-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-148">Gibt an, ob Jet beim Komprimieren einer Datenbank Gebietsschemainformationen kopieren soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="1f56d-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="1f56d-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p106">Gibt an, ob eine komprimierte Datenbank verschlüsselt werden soll. Wenn diese Eigenschaft nicht festgelegt ist, wird die komprimierte Datenbank verschlüsselt, sofern die ursprüngliche Datenbank ebenfalls verschlüsselt war.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="1f56d-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="1f56d-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-155">Gibt das Speichermodul an, das für Zugriff auf den aktuellen Datenspeicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f56d-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="1f56d-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="1f56d-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p107">Gibt die maximale Zeitdauer in Millisekunden an, für die Jet asynchrone Schreibvorgänge auf Datenträger verzögern kann, wenn die Datenbank exklusiv geöffnet ist. Diese Eigenschaft wird ignoriert, es sei denn <strong>Jet OLEDB: Flush Transaction Timeout</strong> ist auf 0 festgelegt.  </span><span class="sxs-lookup"><span data-stu-id="1f56d-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="1f56d-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="1f56d-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f56d-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p108">Gibt die Zeitdauer an, die gewartet wird, bevor Daten in einem Cache für asynchrones Schreiben tatsächlich auf den Datenträger geschrieben wird. Mit dieser Einstellung werden die Werte für <strong>Jet OLEDB:Shared Async Delay</strong> und <strong>Jet OLEDB:Exclusive Async Delay</strong> außer Kraft gesetzt.  </span><span class="sxs-lookup"><span data-stu-id="1f56d-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-164">Jet OLEDB: globale Bulk Transaktionen</span><span class="sxs-lookup"><span data-stu-id="1f56d-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="1f56d-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="1f56d-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-166">Gibt an, ob SQL-Massentransaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-167">Jet OLEDB: globale teilweise Massen-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="1f56d-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="1f56d-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="1f56d-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-169">Gibt das Kennwort an, das zum Öffnen der Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f56d-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="1f56d-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="1f56d-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="1f56d-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-172">Gibt an, ob Änderungen, die an internen impliziten Transaktionen vorgenommen wurden, im synchronen oder asynchronen Modus geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="1f56d-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="1f56d-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-175">Gibt die Zeitdauer in Millisekunden an, die gewartet werden muss, bevor nach einem gescheiterten Versuch erneut versucht wird, eine Sperre zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="1f56d-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="1f56d-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="1f56d-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-178">Gibt an, wie häufig der Versuch, auf eine gesperrte Seite zuzugreifen, wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="1f56d-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="1f56d-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="1f56d-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-181">Gibt den maximalen Speicherplatz in Kilobytes an, den Jet nutzen kann, bevor Änderungen auf den Datenträger geleert werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="1f56d-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="1f56d-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p109">Gibt die maximale Anzahl von Sperren an, die Jet in einer Datenbank setzen kann. Der Standardwert beträgt 9500.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-186">Jet OLEDB: neue Datenbankkennwort</span><span class="sxs-lookup"><span data-stu-id="1f56d-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="1f56d-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="1f56d-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p110">Gibt das neue Kennwort an, das für diese Datenbank festgelegt werden muss. Das alte Kennwort wird in <strong>Jet OLEDB:Database Password</strong> gespeichert.  </span><span class="sxs-lookup"><span data-stu-id="1f56d-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-190">Jet OLEDB: ODBC-Befehlstimeout</span><span class="sxs-lookup"><span data-stu-id="1f56d-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="1f56d-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f56d-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-192">Gibt die Zeitdauer in Millisekunden an, die verstreicht, bevor eine ODBC-Remoteabfrage von Jet das Zeitlimit überschreitet.</span><span class="sxs-lookup"><span data-stu-id="1f56d-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-193">Sperren von Jet OLEDB:Page Tabelle zu sperren</span><span class="sxs-lookup"><span data-stu-id="1f56d-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="1f56d-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="1f56d-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p111">Gibt an, wie viele Seiten in einer Transaktion gesperrt werden müssen, bevor Jet versucht, die Sperre auf eine Tabellensperre höherzustufen. Wenn dieser Wert 0 ist, wird die Sperre nie höhergestuft.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="1f56d-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="1f56d-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="1f56d-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-199">Gibt die Zeitdauer in Millisekunden an, die Jet abwartet, bevor geprüft wird, ob der Cache im Vergleich zur Datenbankdatei noch aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="1f56d-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="1f56d-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="1f56d-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="1f56d-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-202">Gibt an, ob Jet BLOB-Seiten nach deren Freigabe auf aggressive Weise verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="1f56d-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="1f56d-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="1f56d-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-205">Gibt den Windows-Registrierungsschlüssel an, der die Werte für das Jet-Datenbankmodul enthält.</span><span class="sxs-lookup"><span data-stu-id="1f56d-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-206">Jet OLEDB:Reset ISAM Stats</span><span class="sxs-lookup"><span data-stu-id="1f56d-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="1f56d-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="1f56d-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-208">Gibt an, ob das Schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS die Leistungsindikatoren nach dem Zurückgeben von Leistungsinformationen zurücksetzen soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="1f56d-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="1f56d-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-211">Gibt die maximale Zeitdauer in Millisekunden an, für die Jet asynchrone Schreibvorgänge auf Datenträger verzögern kann, wenn die Datenbank für mehrere Benutzer geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f56d-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="1f56d-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="1f56d-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="1f56d-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-214">Gibt den Pfad und den Dateinamen für die Arbeitsgruppen-Informationsdatei (Systemdatenbank) an.</span><span class="sxs-lookup"><span data-stu-id="1f56d-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-215">Jet OLEDB:Transaction Commit-Modus</span><span class="sxs-lookup"><span data-stu-id="1f56d-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="1f56d-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="1f56d-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-217">Gibt an, ob Jet Daten beim Ausführen einer Transaktion synchron oder asynchron auf Datenträger schreibt.</span><span class="sxs-lookup"><span data-stu-id="1f56d-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="1f56d-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="1f56d-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="1f56d-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-220">Gibt an, ob Änderungen, die an Transaktionen vorgenommen wurden, im synchronen oder asynchronen Modus geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="1f56d-221">Anwenderspezifische Recordset- und Command-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f56d-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="1f56d-p112">Der Jet-Anbieter unterstützt zudem auch mehrere anwenderspezifische **Recordset** - und **Command** -Eigenschaften. Diese Eigenschaften werden über die **Properties** -Auflistung der Objekte **Recordset** oder **Command** festgelegt. In der Tabelle ist der ADO-Eigenschaftenname sowie der entsprechende OLE DB-Eigenschaftenname in Klammern angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-225">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f56d-226">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f56d-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-227">Jet OLEDB:Bulk Transaktionen</span><span class="sxs-lookup"><span data-stu-id="1f56d-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="1f56d-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="1f56d-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p113">Gibt an, ob SQL-Massenvorgänge durchgeführt werden. Umfangreiche Massenvorgänge können aufgrund von Ressourcenverzögerungen möglicherweise nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-231">Jet OLEDB: Enable Fat Cursor</span><span class="sxs-lookup"><span data-stu-id="1f56d-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="1f56d-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="1f56d-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-233">Gibt an, ob Jet beim Auffüllen einer Datensatzgruppe für eine Remote-Datensatzherkunft mehrere Zeilen zwischenspeichern soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-234">Jet OLEDB:Fat Cursor Cachegröße</span><span class="sxs-lookup"><span data-stu-id="1f56d-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="1f56d-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="1f56d-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p114">Gibt die Anzahl von Zeilen an, die beim Zwischenspeichern von Zeilen von Remotedatenspeichern zwischengespeichert werden sollen. Dieser Wert wird nur beachtet, wenn <strong>Jet OLEDB:Enable Fat Cursors</strong> auf True gesetzt ist.  </span><span class="sxs-lookup"><span data-stu-id="1f56d-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-238">Jet OLEDB: inkonsistente</span><span class="sxs-lookup"><span data-stu-id="1f56d-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="1f56d-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="1f56d-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-240">Gibt an, ob in Abfrageergebnissen inkonsistente Aktualisierungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1f56d-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-241">Jet OLEDB: Granularität der Sperren</span><span class="sxs-lookup"><span data-stu-id="1f56d-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="1f56d-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-243">Gibt an, ob eine Tabelle mithilfe von Sperren auf Zeilenebene geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1f56d-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-244">Jet OLEDB: ODBC Pass-Through-Anweisung</span><span class="sxs-lookup"><span data-stu-id="1f56d-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="1f56d-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="1f56d-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-246">Gibt an, dass Jet den SQL-Text in einem <strong>Command</strong> -Objekt unverändert an das Back-End übergeben muss.</span><span class="sxs-lookup"><span data-stu-id="1f56d-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-247">Jet OLEDB:Partial Massen-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="1f56d-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="1f56d-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="1f56d-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-249">Gibt das Verhalten von Jet für den Fall an, dass SQL DML-Vorgänge nicht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="1f56d-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-250">Jet-OLEDB:Pass über Massen Abfrage ausgeführt</span><span class="sxs-lookup"><span data-stu-id="1f56d-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="1f56d-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="1f56d-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-252">Gibt an, ob Abfragen, die kein <strong>Recordset</strong> -Objekt zurückgeben, unverändert an die Datenquelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-253">Jet-OLEDB:Pass durch Abfrage für die Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1f56d-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="1f56d-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="1f56d-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-p115">Gibt die Jet-Verbindungszeichenfolge an, die für die Verbindung mit einem Remotedatenspeicher verwendet wird. Dieser Wert wird nur beachtet, wenn <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> auf True gesetzt ist.  </span><span class="sxs-lookup"><span data-stu-id="1f56d-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-257">Jet OLEDB: gespeicherte Abfrage</span><span class="sxs-lookup"><span data-stu-id="1f56d-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="1f56d-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="1f56d-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-259">Gibt an, ob der Befehlstext nicht als SQL-Befehl, sondern als gespeicherte Abfrage interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56d-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-260">Jet OLEDB: Regeln auf Satz überprüfen</span><span class="sxs-lookup"><span data-stu-id="1f56d-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="1f56d-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="1f56d-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="1f56d-262">Gibt an, ob die Jet-Gültigkeitsregeln beim Festlegen der Spaltendaten oder bei der Übergabe der Änderungen an die Datenbank ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f56d-p116">Der OLE DB-Anbieter für Microsoft Jet öffnet Microsoft Jet-Datenbanken standardmäßig im Lese-/Schreibmodus. Um eine Datenbank im schreibgeschützten Modus zu öffnen, legen Sie die [Mode](mode-property-ado.md)-Eigenschaft im ADO-Objekt **Connection** auf **adModeRead** fest.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="1f56d-265">Verwendung des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="1f56d-265">Command Object Usage</span></span>

<span data-ttu-id="1f56d-p117">Für Befehlstext im [Command](command-object-ado.md)-Objekt wird der Microsoft Jet SQL-Dialekt verwendet. Sie können im Befehlstext Abfragen, die Zeilen zurückgeben, Aktionsabfragen und Tabellennamen angeben. Gespeicherte Prozeduren werden jedoch nicht unterstützt und dürfen nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="1f56d-268">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="1f56d-268">Recordset Behavior</span></span>

<span data-ttu-id="1f56d-p118">Das Microsoft Jet-Datenbankmodul unterstützt keine dynamischen Cursor. Daher unterstützt der OLE DB-Anbieter für Microsoft Jet den **adLockDynamic**-Cursortyp nicht. Wenn ein dynamischer Cursor angefordert wird, gibt der Anbieter einen Keyset-Cursor zurück und setzt die [CursorType](cursortype-property-ado.md)-Eigenschaft zurück, um den Typ des zurückgegebenen [Recordset](recordset-object-ado.md)-Objekts anzugeben. Wenn ein aktualisierbares **Recordset**-Objekt angefordert wird (**LockType** ist auf **adLockOptimistic**, **adLockBatchOptimistic** oder **adLockPessimistic** gesetzt), gibt der Anbieter ebenfalls einen Keyset-Cursor zurück und setzt die **CursorType**-Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="1f56d-273">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f56d-273">Dynamic Properties</span></span>

<span data-ttu-id="1f56d-274">Der OLE DB-Anbieter für Microsoft Jet fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="1f56d-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="1f56d-p119">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="1f56d-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="1f56d-279">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="1f56d-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="1f56d-280">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f56d-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-281">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f56d-282">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="1f56d-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="1f56d-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="1f56d-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="1f56d-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="1f56d-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="1f56d-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="1f56d-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="1f56d-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="1f56d-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f56d-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f56d-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f56d-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="1f56d-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="1f56d-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="1f56d-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="1f56d-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="1f56d-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="1f56d-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="1f56d-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="1f56d-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="1f56d-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="1f56d-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="1f56d-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="1f56d-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="1f56d-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f56d-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="1f56d-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="1f56d-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="1f56d-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="1f56d-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f56d-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f56d-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f56d-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="1f56d-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="1f56d-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="1f56d-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="1f56d-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="1f56d-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="1f56d-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="1f56d-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="1f56d-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="1f56d-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="1f56d-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f56d-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f56d-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f56d-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="1f56d-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="1f56d-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="1f56d-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="1f56d-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="1f56d-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="1f56d-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="1f56d-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="1f56d-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="1f56d-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="1f56d-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="1f56d-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="1f56d-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="1f56d-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="1f56d-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="1f56d-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="1f56d-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="1f56d-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f56d-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-329">Mode</span><span class="sxs-lookup"><span data-stu-id="1f56d-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="1f56d-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="1f56d-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="1f56d-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="1f56d-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="1f56d-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="1f56d-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="1f56d-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f56d-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f56d-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="1f56d-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="1f56d-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f56d-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="1f56d-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="1f56d-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="1f56d-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="1f56d-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f56d-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f56d-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="1f56d-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="1f56d-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="1f56d-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f56d-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="1f56d-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="1f56d-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f56d-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="1f56d-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="1f56d-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="1f56d-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="1f56d-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="1f56d-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-355">Password</span><span class="sxs-lookup"><span data-stu-id="1f56d-355">Password</span></span></p></td>
<td><p><span data-ttu-id="1f56d-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="1f56d-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="1f56d-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="1f56d-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="1f56d-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="1f56d-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f56d-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f56d-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="1f56d-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f56d-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f56d-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="1f56d-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="1f56d-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="1f56d-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="1f56d-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="1f56d-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="1f56d-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="1f56d-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="1f56d-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="1f56d-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="1f56d-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="1f56d-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="1f56d-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="1f56d-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="1f56d-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="1f56d-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="1f56d-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f56d-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="1f56d-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="1f56d-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="1f56d-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="1f56d-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="1f56d-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="1f56d-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="1f56d-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="1f56d-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="1f56d-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f56d-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="1f56d-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="1f56d-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="1f56d-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="1f56d-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="1f56d-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="1f56d-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="1f56d-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="1f56d-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="1f56d-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="1f56d-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="1f56d-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-391">User ID</span><span class="sxs-lookup"><span data-stu-id="1f56d-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="1f56d-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="1f56d-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-393">User Name</span><span class="sxs-lookup"><span data-stu-id="1f56d-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="1f56d-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="1f56d-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="1f56d-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="1f56d-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="1f56d-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="1f56d-397">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="1f56d-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="1f56d-398">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f56d-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-399">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f56d-400">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f56d-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f56d-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f56d-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="1f56d-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f56d-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f56d-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f56d-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f56d-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f56d-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f56d-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f56d-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f56d-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="1f56d-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="1f56d-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f56d-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="1f56d-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="1f56d-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f56d-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f56d-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f56d-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f56d-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f56d-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="1f56d-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="1f56d-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="1f56d-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f56d-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f56d-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f56d-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f56d-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f56d-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f56d-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f56d-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f56d-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f56d-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f56d-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f56d-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f56d-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f56d-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f56d-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f56d-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f56d-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f56d-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f56d-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="1f56d-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f56d-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f56d-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f56d-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f56d-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f56d-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f56d-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f56d-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="1f56d-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f56d-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f56d-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f56d-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="1f56d-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f56d-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f56d-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f56d-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f56d-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f56d-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f56d-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f56d-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f56d-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="1f56d-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="1f56d-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="1f56d-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-466">IStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="1f56d-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f56d-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f56d-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="1f56d-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="1f56d-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f56d-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f56d-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f56d-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f56d-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f56d-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f56d-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f56d-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f56d-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f56d-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f56d-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f56d-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f56d-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f56d-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f56d-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f56d-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f56d-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f56d-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f56d-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f56d-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f56d-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f56d-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f56d-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f56d-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f56d-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f56d-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f56d-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f56d-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f56d-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f56d-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f56d-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f56d-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f56d-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f56d-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f56d-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f56d-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f56d-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="1f56d-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f56d-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f56d-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f56d-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f56d-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="1f56d-544">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="1f56d-544">Command Dynamic Properties</span></span>

<span data-ttu-id="1f56d-545">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f56d-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f56d-546">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f56d-547">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1f56d-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f56d-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f56d-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f56d-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="1f56d-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f56d-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f56d-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f56d-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f56d-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f56d-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f56d-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f56d-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f56d-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f56d-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f56d-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f56d-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f56d-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f56d-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f56d-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f56d-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f56d-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f56d-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f56d-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f56d-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f56d-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f56d-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f56d-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f56d-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f56d-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f56d-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f56d-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f56d-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f56d-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f56d-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f56d-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="1f56d-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="1f56d-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f56d-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f56d-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f56d-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f56d-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f56d-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f56d-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f56d-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f56d-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="1f56d-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="1f56d-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f56d-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f56d-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f56d-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f56d-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f56d-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f56d-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f56d-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f56d-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f56d-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f56d-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f56d-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="1f56d-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="1f56d-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="1f56d-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-607">IStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="1f56d-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="1f56d-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f56d-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f56d-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f56d-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f56d-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="1f56d-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="1f56d-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="1f56d-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f56d-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f56d-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f56d-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f56d-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f56d-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f56d-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f56d-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f56d-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f56d-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f56d-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f56d-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f56d-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f56d-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f56d-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f56d-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f56d-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f56d-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f56d-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f56d-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f56d-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f56d-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f56d-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f56d-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f56d-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f56d-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f56d-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f56d-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f56d-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f56d-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f56d-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f56d-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f56d-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f56d-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f56d-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f56d-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f56d-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f56d-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f56d-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f56d-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f56d-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f56d-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f56d-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f56d-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f56d-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f56d-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f56d-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="1f56d-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="1f56d-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="1f56d-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="1f56d-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f56d-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f56d-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f56d-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f56d-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f56d-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f56d-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f56d-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f56d-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f56d-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f56d-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1f56d-687">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f56d-687">See also</span></span>

<span data-ttu-id="1f56d-688">Implementierung und funktionale Informationen zu den OLE DB-Anbieter für Microsoft Jet finden Sie in der OLE DB-Anbieter für Microsoft Jet im MDAC SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1f56d-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

