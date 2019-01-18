---
title: Microsoft OLE DB-Anbieter für ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704560"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="f088f-102">Microsoft OLE DB-Anbieter für ODBC</span><span class="sxs-lookup"><span data-stu-id="f088f-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="f088f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f088f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f088f-p101">Unter idealen Bedingungen für einen ADO- oder RDS-Programmierer wäre für jede Datenquelle eine OLE DB-Schnittstelle verfügbar, sodass ADO Aufrufe direkt in der Datenquelle ausführen könnte. Obwohl Datenbankanbieter zunehmend OLE DB-Schnittstellen implementieren, sind einige Datenquellen noch nicht auf diese Weise verfügbar. Dennoch kann auf praktisch alle heutigen DBMS-Systeme über ODBC zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f088f-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="f088f-107">ODBC-Treiber sind für alle größeren DBMS-Systeme von heute verfügbar, so auch für Microsoft SQL Server, Microsoft Access (Microsoft Jet-Datenbankmodul) und Microsoft FoxPro sowie für Datenbankprodukte, die nicht von Microsoft stammen, wie z. B. Oracle.</span><span class="sxs-lookup"><span data-stu-id="f088f-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="f088f-p102">Mithilfe des Microsoft ODBC-Anbieters kann ADO jedoch eine Verbindung mit einer ODBC-Datenquelle herstellen. Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="f088f-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="f088f-p103">Der Anbieter unterstützt Transaktionen, wenngleich unterschiedliche DBMS-Module Transaktionen auf unterschiedliche Art unterstützen. So unterstützt Microsoft Access beispielsweise bis zu fünf Ebenen tief geschachtelte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="f088f-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="f088f-112">Hierbei handelt es sich um den Standardanbieter für ADO. Alle vom Anbieter abhängigen ADO-Eigenschaften und -Methoden werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f088f-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="f088f-113">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="f088f-113">Connection String Parameters</span></span>

<span data-ttu-id="f088f-114">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="f088f-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="f088f-115">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="f088f-116">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f088f-116">Typical Connection String</span></span>

<span data-ttu-id="f088f-117">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="f088f-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="f088f-118">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="f088f-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-119">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="f088f-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="f088f-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f088f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="f088f-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="f088f-122">Gibt den OLE DB-Anbieter für ODBC an.</span><span class="sxs-lookup"><span data-stu-id="f088f-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="f088f-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="f088f-124">Gibt den Namen der Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="f088f-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="f088f-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="f088f-126">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="f088f-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="f088f-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="f088f-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="f088f-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="f088f-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="f088f-130">Gibt die URL einer Datei oder das Verzeichnis in einem Webordner veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="f088f-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f088f-131">Da es sich hierbei um den Standardanbieter für ADO handelt, versucht ADO eine Verbindung mit diesem Anbieter herzustellen, wenn Sie den **Provider=** -Parameter in der Verbindungsreihenfolge nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="f088f-p104">Der Anbieter unterstützt neben den von ADO definierten keine bestimmten Verbindungsparameter. Der Anbieter übergibt jedoch alle Verbindungsparameter, die nicht von ADO stammen, an den ODBC-Treibermanager.</span><span class="sxs-lookup"><span data-stu-id="f088f-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="f088f-p105">Da Sie den **Provider**-Parameter nicht angeben müssen, können Sie eine ADO-Verbindungszeichenfolge erstellen, die mit einer ODBC-Verbindungszeichenfolge für dieselbe Datenquelle identisch ist. Verwenden Sie dieselben Parameternamen (**DRIVER=**, **DATABASE=**, **DSN=** usw.) und Werte und dieselbe Syntax wie beim Erstellen einer ODBC-Verbindungszeichenfolge. Sie können eine Verbindung mit oder ohne vordefinierten Datenquellennamen (DSN) oder Datei-DSN herstellen.</span><span class="sxs-lookup"><span data-stu-id="f088f-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="f088f-137">**Syntax mit einem DSN oder Datei-DSN:**</span><span class="sxs-lookup"><span data-stu-id="f088f-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="f088f-138">**Syntax ohne einen DSN (Verbindung ohne DSN):**</span><span class="sxs-lookup"><span data-stu-id="f088f-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="f088f-p106">Wenn Sie einen DSN oder Datei-DSN verwenden, muss dieser über den ODBC-Datenquellenadministrator in der Windows-Systemsteuerung definiert werden. Bei Microsoft Windows 2000 befindet sich ODBC Administrator unter Verwaltung. Bei früheren Versionen von Windows heißt das Symbol für ODBC Administrator 32-Bit-ODBC oder einfach ODBC.</span><span class="sxs-lookup"><span data-stu-id="f088f-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="f088f-142">Alternativ zum Festlegen eines **DSN** können Sie auch den ODBC-Treiber (**DRIVER=**), wie z. B. "SQL Server", den Servernamen (**SERVER=**) und den Datenbanknamen (**DATABASE=**) angeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="f088f-143">Sie können auch den Namen (**UID=**) und das Kennwort für ein Benutzerkonto (**PWD=**) in den ODBC-spezifischen Parametern oder in den von ADO definierten Standardparametern *user* und *password* angeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="f088f-144">Obwohl die Definition eines **DSN** bereits eine Datenbank angibt, können Sie \* *ein* Datenbankparameter neben einen **DSN** -Verbindung mit einer anderen Datenbank\* angeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="f088f-145">Es ist ratsam, immer *dem* Parameter *Database* einschließen aus, wenn Sie einen **DSN**verwenden.</span><span class="sxs-lookup"><span data-stu-id="f088f-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="f088f-146">Dadurch wird sichergestellt, dass Sie auf die gewünschte Datenbank verbinden, wenn ein anderer Benutzer den Datenbank Standardparameter geändert, seit Sie zuletzt die **DSN** -Definition geprüft.</span><span class="sxs-lookup"><span data-stu-id="f088f-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="f088f-147">Anbieterspezifische Verbindungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="f088f-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="f088f-p108">Der OLE DB-Anbieter für ODBC fügt der [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts verschiedene Eigenschaften hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f088f-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-150">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="f088f-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f088f-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-152">Zugänglich Prozeduren</span><span class="sxs-lookup"><span data-stu-id="f088f-152">Accessible Procedures</span></span><br />
<span data-ttu-id="f088f-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="f088f-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="f088f-154">Gibt an, ob der Benutzer Zugriff auf gespeicherte Prozeduren hat.</span><span class="sxs-lookup"><span data-stu-id="f088f-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-155">Zugänglich Tabellen</span><span class="sxs-lookup"><span data-stu-id="f088f-155">Accessible Tables</span></span><br />
<span data-ttu-id="f088f-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="f088f-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="f088f-157">Gibt an, ob der Benutzer über die Berechtigung zum Ausführen der SELECT-Anweisungen in Datenbanktabellen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f088f-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-158">Active-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f088f-158">Active Statements</span></span><br />
<span data-ttu-id="f088f-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="f088f-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-160">Gibt die Anzahl von Handles an, die ein ODBC-Treiber in einer Verbindung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="f088f-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-161">Treibername</span><span class="sxs-lookup"><span data-stu-id="f088f-161">Driver Name</span></span><br />
<span data-ttu-id="f088f-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="f088f-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="f088f-163">Gibt den Dateinamen des ODBC-Treibers an.</span><span class="sxs-lookup"><span data-stu-id="f088f-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-164">ODBC-Treiberversion</span><span class="sxs-lookup"><span data-stu-id="f088f-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="f088f-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="f088f-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="f088f-166">Gibt die Version von ODBC an, die von diesem Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-167">Verwendung der Datei</span><span class="sxs-lookup"><span data-stu-id="f088f-167">File Usage</span></span><br />
<span data-ttu-id="f088f-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="f088f-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="f088f-169">Gibt an, wie der Treiber eine Datei in einer Datenquelle behandelt: als Tabelle oder als Katalog.</span><span class="sxs-lookup"><span data-stu-id="f088f-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-170">Wie Escape-Klausel</span><span class="sxs-lookup"><span data-stu-id="f088f-170">Like Escape Clause</span></span><br />
<span data-ttu-id="f088f-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="f088f-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="f088f-172">Gibt an, ob der Treiber die Definition und Verwendung eines Escapezeichens für das Prozentzeichen (%) und das Unterstrichzeichen (_) im LIKE-Prädikat einer WHERE-Klausel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f088f-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-173">Maximale Anzahl von Spalten in Gruppen von</span><span class="sxs-lookup"><span data-stu-id="f088f-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="f088f-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="f088f-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="f088f-175">Gibt die maximale Anzahl von Spalten an, die in der GROUP BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="f088f-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-176">Maximale Anzahl von Spalten im Index</span><span class="sxs-lookup"><span data-stu-id="f088f-176">Max Columns in Index</span></span><br />
<span data-ttu-id="f088f-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="f088f-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="f088f-178">Gibt die maximale Anzahl von Spalten an, die in einem Index enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="f088f-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-179">Maximale Anzahl von Spalten in der Order By-</span><span class="sxs-lookup"><span data-stu-id="f088f-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="f088f-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="f088f-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="f088f-181">Gibt die maximale Anzahl von Spalten an, die in der ORDER BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="f088f-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-182">Maximale Anzahl von Spalten in auswählen</span><span class="sxs-lookup"><span data-stu-id="f088f-182">Max Columns in Select</span></span><br />
<span data-ttu-id="f088f-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="f088f-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="f088f-184">Gibt die maximale Anzahl von Spalten an, die im SELECT-Teil einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="f088f-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-185">Maximale Anzahl von Spalten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="f088f-185">Max Columns in Table</span></span><br />
<span data-ttu-id="f088f-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="f088f-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="f088f-187">Gibt die maximale Anzahl von Spalten an, die in einer Tabelle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f088f-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-188">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f088f-188">Numeric Functions</span></span><br />
<span data-ttu-id="f088f-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="f088f-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-p109">Gibt an, welche numerischen Funktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="f088f-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-192">Outer Join-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f088f-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="f088f-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="f088f-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="f088f-194">Gibt die vom Anbieter unterstützten OUTER JOIN-Typen an.</span><span class="sxs-lookup"><span data-stu-id="f088f-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-195">Äußere Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f088f-195">Outer Joins</span></span><br />
<span data-ttu-id="f088f-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="f088f-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-197">Gibt an, ob der Anbieter OUTER JOIN-Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f088f-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-198">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="f088f-198">Special Characters</span></span><br />
<span data-ttu-id="f088f-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="f088f-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-200">Gibt an, welche Zeichen eine besondere Bedeutung für den ODBC-Treiber haben.</span><span class="sxs-lookup"><span data-stu-id="f088f-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-201">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="f088f-201">Stored Procedures</span></span><br />
<span data-ttu-id="f088f-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="f088f-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="f088f-203">Gibt an, ob gespeicherte Prozeduren für die Verwendung mit diesem ODBC-Treiber verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f088f-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-204">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f088f-204">String Functions</span></span><br />
<span data-ttu-id="f088f-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="f088f-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-p110">Gibt an, welche Zeichenfolgenfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="f088f-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-208">Systemfunktionen</span><span class="sxs-lookup"><span data-stu-id="f088f-208">System Functions</span></span><br />
<span data-ttu-id="f088f-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="f088f-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-p111">Gibt an, welche Systemfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="f088f-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-212">/ Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f088f-212">Time/Date Functions</span></span><br />
<span data-ttu-id="f088f-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="f088f-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="f088f-p112">Gibt an, welche Uhrzeit- und Datumsfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="f088f-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-216">Unterstützung für SQL-Grammatik</span><span class="sxs-lookup"><span data-stu-id="f088f-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="f088f-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="f088f-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="f088f-218">Gibt die SQL-Grammatik an, die von diesem ODBC-Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="f088f-219">Anwenderspezifische Recordset- und Command-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f088f-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="f088f-p113">Der OLE DB-Anbieter für ODBC fügt der **Properties** -Auflistung der Objekte **Recordset** und **Command** verschiedene Objekte hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f088f-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-222">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="f088f-223">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f088f-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-224">Abfragebasierte Updates/löschen/fügt</span><span class="sxs-lookup"><span data-stu-id="f088f-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="f088f-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="f088f-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="f088f-226">Gibt an, ob Aktualisierungen und Lösch- und Einfügevorgänge mithilfe von SQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="f088f-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-227">ODBC-Parallelität-Typ</span><span class="sxs-lookup"><span data-stu-id="f088f-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="f088f-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="f088f-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="f088f-229">Gibt die Methode an, die verwendet wird, um potenzielle Probleme zu reduzieren, die von zwei Benutzern verursacht werden, die gleichzeitig auf dieselben Daten in der Datenquelle zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="f088f-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-230">BLOB-Eingabehilfen auf Vorwärtscursor</span><span class="sxs-lookup"><span data-stu-id="f088f-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="f088f-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="f088f-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="f088f-232">Gibt an, ob auf BLOB-<strong>Felder</strong> zugegriffen werden kann, wenn ein Vorwärtscursor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-233">SQL_FLOAT, SQL_DOUBLE und SQL_REAL in QBU WHERE-Klausel einschließen</span><span class="sxs-lookup"><span data-stu-id="f088f-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="f088f-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="f088f-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="f088f-235">Gibt an, ob die Werte SQL_FLOAT, SQL_DOUBLE und SQL_REAL in eine QBU WHERE-Klausel eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="f088f-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-236">Position in der letzten Zeile nach dem Einfügen</span><span class="sxs-lookup"><span data-stu-id="f088f-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="f088f-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="f088f-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="f088f-238">Gibt an, dass nach dem Einfügen eines neuen Datensatzes in eine Tabelle die letzte Zeile zur aktuellen Zeile wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="f088f-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="f088f-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="f088f-241">Gibt an, ob die <strong>IRowsetChange</strong>-Schnittstelle erweiterte Informationsunterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="f088f-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-242">ODBC-Cursor-Typ</span><span class="sxs-lookup"><span data-stu-id="f088f-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="f088f-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="f088f-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="f088f-244">Gibt den Cursortyp an, der vom <strong>Recordset</strong>-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-245">Generieren eines Rowsets, die gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f088f-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="f088f-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="f088f-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="f088f-247">Gibt an, dass der ODBC-Treiber eine Datensatzgruppe generiert, die gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f088f-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="f088f-248">Befehlstext</span><span class="sxs-lookup"><span data-stu-id="f088f-248">Command Text</span></span>

<span data-ttu-id="f088f-249">Die Verwendung des [Command](command-object-ado.md)-Objekts hängt zum großen Teil von der Datenquelle sowie vom Typ der Abfrage- oder Befehlsanweisung, die akzeptiert wird, ab.</span><span class="sxs-lookup"><span data-stu-id="f088f-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="f088f-250">ODBC stellt eine bestimmte Syntax zum Aufrufen von gespeicherten Prozeduren bereit.</span><span class="sxs-lookup"><span data-stu-id="f088f-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="f088f-251">Für die [CommandText](commandtext-property-ado.md) -Eigenschaft des **Command** -Objekts, das *CommandText* -Argument der **Execute** -Methode für ein [Connection](connection-object-ado.md) -Objekt oder das Argument *Source* an die **Open** -Methode für ein [Recordset-Objekt](recordset-object-ado.md) -Objekt übergibt eine Zeichenfolge mit der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="f088f-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="f088f-p115">Jedes Fragezeichen (**?**) verweist auf ein Objekt in der [Parameters](parameters-collection-ado.md)-Auflistung. Das erste Fragezeichen (**?**) verweist auf **Parameters**(0), das nächste Fragezeichen (**?**) auf **Parameters**(1) usw.</span><span class="sxs-lookup"><span data-stu-id="f088f-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="f088f-p116">Die Parameterverweise sind optional und hängen von der Struktur der gespeicherten Prozedur ab. Wenn Sie eine gespeicherte Prozedur aufrufen möchten, die keine Parameter definiert, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="f088f-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="f088f-259">Wenn zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="f088f-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="f088f-p117">Wenn die gespeicherte Prozedur einen Wert zurückgibt, wird der Rückgabewert wie ein weiterer Parameter verwendet. Wenn keine Abfrageparameter verwendet werden, aber ein Rückgabewert vorliegt, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="f088f-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="f088f-262">Wenn ein Rückgabewert und zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="f088f-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="f088f-263">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="f088f-263">Recordset Behavior</span></span>

<span data-ttu-id="f088f-264">In den folgenden Tabellen sind die für ein mit diesem Anbieter geöffnetes **Recordset** -Objekt verfügbaren ADO-Standardmethoden und -Eigenschaften aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f088f-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="f088f-265">Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die **Properties** -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f088f-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="f088f-266">Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="f088f-266">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-267">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f088f-267">Property</span></span></p></th>
<th><p><span data-ttu-id="f088f-268">ForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="f088f-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="f088f-269">Dynamic</span><span class="sxs-lookup"><span data-stu-id="f088f-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="f088f-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="f088f-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="f088f-271">Static</span><span class="sxs-lookup"><span data-stu-id="f088f-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="f088f-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-273">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-273">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-274">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-274">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-275">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-276">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="f088f-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-278">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-278">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-279">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-279">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-280">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-281">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="f088f-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-283">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-284">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-285">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-286">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="f088f-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-288">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-289">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-290">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-291">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-292"><a href="bookmark-property-ado.md">Lesezeichen</a></span><span class="sxs-lookup"><span data-stu-id="f088f-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-293">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-293">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-294">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-294">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-295">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-296">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="f088f-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-298">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-299">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-300">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-301">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="f088f-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-303">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-304">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-305">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-306">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="f088f-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-308">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-309">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-310">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-311">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="f088f-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-313">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-314">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-315">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-316">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="f088f-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-318">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-319">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-320">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-321">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="f088f-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-323">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-324">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-325">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-326">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="f088f-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-328">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-329">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-330">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-331">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="f088f-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-333">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-334">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-335">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-336">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="f088f-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-338">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-339">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-339">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-340">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-341">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="f088f-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-343">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-344">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-345">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-346">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="f088f-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-348">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-349">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f088f-349">not available</span></span></p></td>
<td><p><span data-ttu-id="f088f-350">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-351">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="f088f-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-353">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-354">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-355">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="f088f-356">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f088f-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="f088f-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-358">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-359">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-360">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-361">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="f088f-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-363">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-364">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-365">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="f088f-366">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="f088f-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f088f-367">Die Eigenschaften [AbsolutePosition](absoluteposition-property-ado.md) und [AbsolutePage](absolutepage-property-ado.md) sind schreibgeschützt, wenn ADO mit der Version 1.0 des Microsoft OLE DB-Anbieters für ODBC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="f088f-368">Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="f088f-368">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-369">Methode</span><span class="sxs-lookup"><span data-stu-id="f088f-369">Method</span></span></p></th>
<th><p><span data-ttu-id="f088f-370">ForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="f088f-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="f088f-371">Dynamic</span><span class="sxs-lookup"><span data-stu-id="f088f-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="f088f-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="f088f-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="f088f-373">Static</span><span class="sxs-lookup"><span data-stu-id="f088f-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="f088f-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-375">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-376">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-377">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-378">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="f088f-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-380">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-381">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-382">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-383">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="f088f-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-385">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-386">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-387">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-388">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="f088f-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-390">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-391">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-392">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-393">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="f088f-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-395">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-395">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-396">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-396">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-397">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-398">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="f088f-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-400">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-401">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-402">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-403">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="f088f-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-405">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-406">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-407">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-408">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="f088f-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-410">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-411">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-412">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-413">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="f088f-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-415">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-416">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-417">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-418">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="f088f-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-420">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-421">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-422">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-423">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="f088f-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-425">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-425">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-426">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-427">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-428">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="f088f-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-430">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-431">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-432">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-433">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="f088f-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-435">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-435">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-436">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-437">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-438">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="f088f-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="f088f-440">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-441">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-442">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-443">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="f088f-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-445">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-446">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-447">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-448">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="f088f-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-450">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-451">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-452">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-453">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="f088f-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-455">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-455">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-456">Nein</span><span class="sxs-lookup"><span data-stu-id="f088f-456">No</span></span></p></td>
<td><p><span data-ttu-id="f088f-457">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-458">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-459"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="f088f-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-460">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-461">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-462">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-463">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="f088f-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-465">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-466">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-467">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-468">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="f088f-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f088f-470">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-471">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-472">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="f088f-473">Ja</span><span class="sxs-lookup"><span data-stu-id="f088f-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f088f-474">\*Nicht unterstützt bei Microsoft Access-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="f088f-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="f088f-475">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f088f-475">Dynamic Properties</span></span>

<span data-ttu-id="f088f-476">Der Microsoft OLE DB-Anbieter für ODBC fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="f088f-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="f088f-p118">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="f088f-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="f088f-481">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="f088f-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="f088f-482">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f088f-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-483">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="f088f-484">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="f088f-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="f088f-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="f088f-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="f088f-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="f088f-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="f088f-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="f088f-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="f088f-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="f088f-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="f088f-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="f088f-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="f088f-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="f088f-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="f088f-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="f088f-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="f088f-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="f088f-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="f088f-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="f088f-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="f088f-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="f088f-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="f088f-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="f088f-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f088f-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="f088f-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="f088f-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="f088f-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="f088f-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="f088f-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="f088f-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="f088f-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="f088f-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="f088f-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="f088f-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="f088f-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="f088f-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="f088f-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="f088f-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="f088f-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="f088f-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="f088f-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="f088f-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="f088f-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="f088f-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="f088f-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="f088f-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="f088f-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="f088f-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="f088f-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="f088f-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="f088f-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="f088f-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="f088f-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="f088f-522">NULL</span><span class="sxs-lookup"><span data-stu-id="f088f-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="f088f-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="f088f-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="f088f-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="f088f-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="f088f-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="f088f-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="f088f-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="f088f-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="f088f-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-529">Location</span><span class="sxs-lookup"><span data-stu-id="f088f-529">Location</span></span></p></td>
<td><p><span data-ttu-id="f088f-530">STANDARD</span><span class="sxs-lookup"><span data-stu-id="f088f-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="f088f-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="f088f-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="f088f-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="f088f-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="f088f-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="f088f-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="f088f-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="f088f-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="f088f-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="f088f-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="f088f-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="f088f-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-539">Mode</span><span class="sxs-lookup"><span data-stu-id="f088f-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="f088f-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="f088f-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="f088f-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="f088f-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="f088f-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="f088f-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="f088f-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="f088f-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="f088f-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="f088f-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="f088f-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="f088f-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="f088f-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="f088f-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="f088f-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="f088f-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="f088f-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="f088f-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f088f-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="f088f-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="f088f-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="f088f-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="f088f-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="f088f-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="f088f-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="f088f-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="f088f-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="f088f-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="f088f-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="f088f-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="f088f-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="f088f-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="f088f-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="f088f-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-565">Password</span><span class="sxs-lookup"><span data-stu-id="f088f-565">Password</span></span></p></td>
<td><p><span data-ttu-id="f088f-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="f088f-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="f088f-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="f088f-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="f088f-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="f088f-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="f088f-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="f088f-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="f088f-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="f088f-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="f088f-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="f088f-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="f088f-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f088f-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="f088f-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="f088f-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f088f-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="f088f-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="f088f-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="f088f-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="f088f-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="f088f-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="f088f-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="f088f-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="f088f-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="f088f-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="f088f-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="f088f-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="f088f-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="f088f-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="f088f-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="f088f-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="f088f-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="f088f-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="f088f-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="f088f-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="f088f-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="f088f-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="f088f-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="f088f-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="f088f-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="f088f-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="f088f-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="f088f-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="f088f-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="f088f-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="f088f-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="f088f-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="f088f-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="f088f-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="f088f-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="f088f-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="f088f-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="f088f-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="f088f-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="f088f-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="f088f-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="f088f-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-605">User ID</span><span class="sxs-lookup"><span data-stu-id="f088f-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="f088f-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="f088f-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-607">User Name</span><span class="sxs-lookup"><span data-stu-id="f088f-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="f088f-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="f088f-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="f088f-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="f088f-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="f088f-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="f088f-611">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="f088f-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="f088f-612">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f088f-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-613">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="f088f-614">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="f088f-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="f088f-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="f088f-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="f088f-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="f088f-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="f088f-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="f088f-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="f088f-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="f088f-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="f088f-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="f088f-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="f088f-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="f088f-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f088f-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="f088f-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="f088f-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="f088f-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="f088f-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="f088f-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f088f-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="f088f-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="f088f-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="f088f-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="f088f-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f088f-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="f088f-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f088f-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="f088f-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="f088f-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="f088f-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="f088f-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="f088f-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="f088f-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="f088f-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="f088f-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="f088f-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="f088f-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="f088f-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="f088f-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="f088f-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="f088f-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="f088f-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="f088f-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="f088f-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="f088f-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="f088f-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="f088f-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f088f-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="f088f-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f088f-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="f088f-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="f088f-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="f088f-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="f088f-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="f088f-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="f088f-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="f088f-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="f088f-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="f088f-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="f088f-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="f088f-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="f088f-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="f088f-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="f088f-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="f088f-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="f088f-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f088f-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="f088f-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="f088f-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f088f-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="f088f-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="f088f-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="f088f-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="f088f-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="f088f-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="f088f-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="f088f-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="f088f-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="f088f-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="f088f-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="f088f-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="f088f-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="f088f-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="f088f-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="f088f-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f088f-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="f088f-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="f088f-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="f088f-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="f088f-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="f088f-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="f088f-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="f088f-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="f088f-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f088f-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="f088f-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="f088f-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f088f-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="f088f-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="f088f-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="f088f-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="f088f-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f088f-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="f088f-734">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="f088f-734">Command Dynamic Properties</span></span>

<span data-ttu-id="f088f-735">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f088f-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f088f-736">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="f088f-737">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f088f-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f088f-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="f088f-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="f088f-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="f088f-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="f088f-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="f088f-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="f088f-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="f088f-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="f088f-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="f088f-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="f088f-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="f088f-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="f088f-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="f088f-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f088f-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="f088f-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="f088f-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="f088f-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f088f-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="f088f-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="f088f-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f088f-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="f088f-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="f088f-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="f088f-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="f088f-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f088f-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="f088f-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f088f-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="f088f-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="f088f-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="f088f-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="f088f-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="f088f-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="f088f-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="f088f-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="f088f-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="f088f-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="f088f-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="f088f-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="f088f-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="f088f-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="f088f-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="f088f-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="f088f-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="f088f-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="f088f-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="f088f-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="f088f-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="f088f-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="f088f-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f088f-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f088f-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="f088f-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f088f-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="f088f-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="f088f-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="f088f-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="f088f-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="f088f-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="f088f-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="f088f-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="f088f-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="f088f-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="f088f-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="f088f-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="f088f-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="f088f-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="f088f-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="f088f-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="f088f-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="f088f-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f088f-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="f088f-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="f088f-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f088f-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="f088f-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="f088f-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="f088f-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="f088f-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="f088f-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="f088f-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="f088f-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="f088f-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="f088f-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="f088f-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="f088f-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="f088f-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="f088f-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="f088f-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="f088f-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="f088f-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="f088f-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f088f-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="f088f-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="f088f-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="f088f-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="f088f-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="f088f-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="f088f-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="f088f-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="f088f-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="f088f-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="f088f-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="f088f-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="f088f-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="f088f-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f088f-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="f088f-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="f088f-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f088f-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="f088f-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f088f-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="f088f-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="f088f-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="f088f-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f088f-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f088f-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f088f-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f088f-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f088f-855">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f088f-855">See also</span></span>

<span data-ttu-id="f088f-856">Weitere Informationen zur Implementierung und funktionale Informationen zu den Microsoft OLE DB-Anbieter für ODBC wenden Sie sich an dem [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) oder besuchen Sie das [Data Plattform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="f088f-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

