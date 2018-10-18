---
title: Microsoft OLE DB-Anbieter für ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606939"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="9ec1e-102">Microsoft OLE DB-Anbieter für ODBC</span><span class="sxs-lookup"><span data-stu-id="9ec1e-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="9ec1e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ec1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ec1e-p101">Unter idealen Bedingungen für einen ADO- oder RDS-Programmierer wäre für jede Datenquelle eine OLE DB-Schnittstelle verfügbar, sodass ADO Aufrufe direkt in der Datenquelle ausführen könnte. Obwohl Datenbankanbieter zunehmend OLE DB-Schnittstellen implementieren, sind einige Datenquellen noch nicht auf diese Weise verfügbar. Dennoch kann auf praktisch alle heutigen DBMS-Systeme über ODBC zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="9ec1e-107">ODBC-Treiber sind für alle größeren DBMS-Systeme von heute verfügbar, so auch für Microsoft SQL Server, Microsoft Access (Microsoft Jet-Datenbankmodul) und Microsoft FoxPro sowie für Datenbankprodukte, die nicht von Microsoft stammen, wie z. B. Oracle.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="9ec1e-p102">Mithilfe des Microsoft ODBC-Anbieters kann ADO jedoch eine Verbindung mit einer ODBC-Datenquelle herstellen. Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="9ec1e-p103">Der Anbieter unterstützt Transaktionen, wenngleich unterschiedliche DBMS-Module Transaktionen auf unterschiedliche Art unterstützen. So unterstützt Microsoft Access beispielsweise bis zu fünf Ebenen tief geschachtelte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="9ec1e-112">Hierbei handelt es sich um den Standardanbieter für ADO. Alle vom Anbieter abhängigen ADO-Eigenschaften und -Methoden werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="9ec1e-113">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec1e-113">Connection String Parameters</span></span>

<span data-ttu-id="9ec1e-114">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="9ec1e-115">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="9ec1e-116">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9ec1e-116">Typical Connection String</span></span>

<span data-ttu-id="9ec1e-117">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="9ec1e-118">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-119">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="9ec1e-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec1e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="9ec1e-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-122">Gibt den OLE DB-Anbieter für ODBC an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="9ec1e-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-124">Gibt den Namen der Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="9ec1e-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-126">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="9ec1e-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="9ec1e-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="9ec1e-130"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="9ec1e-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="9ec1e-131">Gibt die URL einer Datei oder eines Verzeichnisses an, die oder das in einem Webordner veröffentlicht ist.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="9ec1e-132">Gibt die URL einer Datei oder das Verzeichnis in einem Webordner veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="9ec1e-133">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="9ec1e-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="9ec1e-134">Da es sich hierbei um den Standardanbieter für ADO handelt, versucht ADO eine Verbindung mit diesem Anbieter herzustellen, wenn Sie den **Provider=** -Parameter in der Verbindungsreihenfolge nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="9ec1e-p104">Der Anbieter unterstützt neben den von ADO definierten keine bestimmten Verbindungsparameter. Der Anbieter übergibt jedoch alle Verbindungsparameter, die nicht von ADO stammen, an den ODBC-Treibermanager.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="9ec1e-p105">Da Sie den **Provider**-Parameter nicht angeben müssen, können Sie eine ADO-Verbindungszeichenfolge erstellen, die mit einer ODBC-Verbindungszeichenfolge für dieselbe Datenquelle identisch ist. Verwenden Sie dieselben Parameternamen (**DRIVER=**, **DATABASE=**, **DSN=** usw.) und Werte und dieselbe Syntax wie beim Erstellen einer ODBC-Verbindungszeichenfolge. Sie können eine Verbindung mit oder ohne vordefinierten Datenquellennamen (DSN) oder Datei-DSN herstellen.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="9ec1e-140">**Syntax mit einem DSN oder Datei-DSN:**</span><span class="sxs-lookup"><span data-stu-id="9ec1e-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="9ec1e-141">**Syntax ohne einen DSN (Verbindung ohne DSN):**</span><span class="sxs-lookup"><span data-stu-id="9ec1e-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="9ec1e-p106">Wenn Sie einen DSN oder Datei-DSN verwenden, muss dieser über den ODBC-Datenquellenadministrator in der Windows-Systemsteuerung definiert werden. Bei Microsoft Windows 2000 befindet sich ODBC Administrator unter Verwaltung. Bei früheren Versionen von Windows heißt das Symbol für ODBC Administrator 32-Bit-ODBC oder einfach ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="9ec1e-145">Alternativ zum Festlegen eines **DSN** können Sie auch den ODBC-Treiber (**DRIVER=**), wie z. B. "SQL Server", den Servernamen (**SERVER=**) und den Datenbanknamen (**DATABASE=**) angeben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="9ec1e-146">Sie können auch den Namen (**UID=**) und das Kennwort für ein Benutzerkonto (**PWD=**) in den ODBC-spezifischen Parametern oder in den von ADO definierten Standardparametern *user* und *password* angeben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="9ec1e-147">Obwohl die Definition eines **DSN** bereits eine Datenbank angibt, können Sie \* *ein* Datenbankparameter neben einen **DSN** -Verbindung mit einer anderen Datenbank\* angeben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="9ec1e-148">Es ist ratsam, immer *dem* Parameter *Database* einschließen aus, wenn Sie einen **DSN**verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="9ec1e-149">Dadurch wird sichergestellt, dass Sie auf die gewünschte Datenbank verbinden, wenn ein anderer Benutzer den Datenbank Standardparameter geändert, seit Sie zuletzt die **DSN** -Definition geprüft.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="9ec1e-150">Anbieterspezifische Verbindungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ec1e-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="9ec1e-p108">Der OLE DB-Anbieter für ODBC fügt der [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts verschiedene Eigenschaften hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-153">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec1e-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-155">Zugänglich Prozeduren</span><span class="sxs-lookup"><span data-stu-id="9ec1e-155">Accessible Procedures</span></span><br />
<span data-ttu-id="9ec1e-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-157">Gibt an, ob der Benutzer Zugriff auf gespeicherte Prozeduren hat.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-158">Zugänglich Tabellen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-158">Accessible Tables</span></span><br />
<span data-ttu-id="9ec1e-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-160">Gibt an, ob der Benutzer über die Berechtigung zum Ausführen der SELECT-Anweisungen in Datenbanktabellen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-161">Active-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-161">Active Statements</span></span><br />
<span data-ttu-id="9ec1e-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-163">Gibt die Anzahl von Handles an, die ein ODBC-Treiber in einer Verbindung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-164">Treibername</span><span class="sxs-lookup"><span data-stu-id="9ec1e-164">Driver Name</span></span><br />
<span data-ttu-id="9ec1e-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-166">Gibt den Dateinamen des ODBC-Treibers an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-167">ODBC-Treiberversion</span><span class="sxs-lookup"><span data-stu-id="9ec1e-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="9ec1e-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-169">Gibt die Version von ODBC an, die von diesem Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-170">Verwendung der Datei</span><span class="sxs-lookup"><span data-stu-id="9ec1e-170">File Usage</span></span><br />
<span data-ttu-id="9ec1e-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-172">Gibt an, wie der Treiber eine Datei in einer Datenquelle behandelt: als Tabelle oder als Katalog.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-173">Wie Escape-Klausel</span><span class="sxs-lookup"><span data-stu-id="9ec1e-173">Like Escape Clause</span></span><br />
<span data-ttu-id="9ec1e-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-175">Gibt an, ob der Treiber die Definition und Verwendung eines Escapezeichens für das Prozentzeichen (%) und das Unterstrichzeichen (_) im LIKE-Prädikat einer WHERE-Klausel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-176">Maximale Anzahl von Spalten in Gruppen von</span><span class="sxs-lookup"><span data-stu-id="9ec1e-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="9ec1e-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-178">Gibt die maximale Anzahl von Spalten an, die in der GROUP BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-179">Maximale Anzahl von Spalten im Index</span><span class="sxs-lookup"><span data-stu-id="9ec1e-179">Max Columns in Index</span></span><br />
<span data-ttu-id="9ec1e-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-181">Gibt die maximale Anzahl von Spalten an, die in einem Index enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-182">Maximale Anzahl von Spalten in der Order By-</span><span class="sxs-lookup"><span data-stu-id="9ec1e-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="9ec1e-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-184">Gibt die maximale Anzahl von Spalten an, die in der ORDER BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-185">Maximale Anzahl von Spalten in auswählen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-185">Max Columns in Select</span></span><br />
<span data-ttu-id="9ec1e-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-187">Gibt die maximale Anzahl von Spalten an, die im SELECT-Teil einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-188">Maximale Anzahl von Spalten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="9ec1e-188">Max Columns in Table</span></span><br />
<span data-ttu-id="9ec1e-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-190">Gibt die maximale Anzahl von Spalten an, die in einer Tabelle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-191">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-191">Numeric Functions</span></span><br />
<span data-ttu-id="9ec1e-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-p109">Gibt an, welche numerischen Funktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-195">Outer Join-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="9ec1e-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-197">Gibt die vom Anbieter unterstützten OUTER JOIN-Typen an.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-198">Äußere Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-198">Outer Joins</span></span><br />
<span data-ttu-id="9ec1e-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-200">Gibt an, ob der Anbieter OUTER JOIN-Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-201">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-201">Special Characters</span></span><br />
<span data-ttu-id="9ec1e-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-203">Gibt an, welche Zeichen eine besondere Bedeutung für den ODBC-Treiber haben.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-204">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="9ec1e-204">Stored Procedures</span></span><br />
<span data-ttu-id="9ec1e-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-206">Gibt an, ob gespeicherte Prozeduren für die Verwendung mit diesem ODBC-Treiber verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-207">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-207">String Functions</span></span><br />
<span data-ttu-id="9ec1e-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-p110">Gibt an, welche Zeichenfolgenfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-211">Systemfunktionen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-211">System Functions</span></span><br />
<span data-ttu-id="9ec1e-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-p111">Gibt an, welche Systemfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-215">/ Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-215">Time/Date Functions</span></span><br />
<span data-ttu-id="9ec1e-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-p112">Gibt an, welche Uhrzeit- und Datumsfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-219">Unterstützung für SQL-Grammatik</span><span class="sxs-lookup"><span data-stu-id="9ec1e-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="9ec1e-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-221">Gibt die SQL-Grammatik an, die von diesem ODBC-Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="9ec1e-222">Anwenderspezifische Recordset- und Command-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ec1e-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="9ec1e-p113">Der OLE DB-Anbieter für ODBC fügt der **Properties** -Auflistung der Objekte **Recordset** und **Command** verschiedene Objekte hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-225">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-226">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec1e-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-227">Abfragebasierte Updates/löschen/fügt</span><span class="sxs-lookup"><span data-stu-id="9ec1e-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="9ec1e-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-229">Gibt an, ob Aktualisierungen und Lösch- und Einfügevorgänge mithilfe von SQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-230">ODBC-Parallelität-Typ</span><span class="sxs-lookup"><span data-stu-id="9ec1e-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="9ec1e-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-232">Gibt die Methode an, die verwendet wird, um potenzielle Probleme zu reduzieren, die von zwei Benutzern verursacht werden, die gleichzeitig auf dieselben Daten in der Datenquelle zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-233">BLOB-Eingabehilfen auf Vorwärtscursor</span><span class="sxs-lookup"><span data-stu-id="9ec1e-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="9ec1e-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-235">Gibt an, ob auf BLOB-<strong>Felder</strong> zugegriffen werden kann, wenn ein Vorwärtscursor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-236">SQL_FLOAT, SQL_DOUBLE und SQL_REAL in QBU WHERE-Klausel einschließen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="9ec1e-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-238">Gibt an, ob die Werte SQL_FLOAT, SQL_DOUBLE und SQL_REAL in eine QBU WHERE-Klausel eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-239">Position in der letzten Zeile nach dem Einfügen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="9ec1e-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-241">Gibt an, dass nach dem Einfügen eines neuen Datensatzes in eine Tabelle die letzte Zeile zur aktuellen Zeile wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="9ec1e-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-244">Gibt an, ob die <strong>IRowsetChange</strong>-Schnittstelle erweiterte Informationsunterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-245">ODBC-Cursor-Typ</span><span class="sxs-lookup"><span data-stu-id="9ec1e-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="9ec1e-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-247">Gibt den Cursortyp an, der vom <strong>Recordset</strong>-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-248">Generieren eines Rowsets, die gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="9ec1e-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="9ec1e-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-250">Gibt an, dass der ODBC-Treiber eine Datensatzgruppe generiert, die gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="9ec1e-251">Befehlstext</span><span class="sxs-lookup"><span data-stu-id="9ec1e-251">Command Text</span></span>

<span data-ttu-id="9ec1e-252">Die Verwendung des [Command](command-object-ado.md)-Objekts hängt zum großen Teil von der Datenquelle sowie vom Typ der Abfrage- oder Befehlsanweisung, die akzeptiert wird, ab.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="9ec1e-253">ODBC stellt eine bestimmte Syntax zum Aufrufen von gespeicherten Prozeduren bereit.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="9ec1e-254">Für die [CommandText](commandtext-property-ado.md) -Eigenschaft des **Command** -Objekts, das *CommandText* -Argument der **Execute** -Methode für ein [Connection](connection-object-ado.md) -Objekt oder das Argument *Source* an die **Open** -Methode für ein [Recordset-Objekt](recordset-object-ado.md) -Objekt übergibt eine Zeichenfolge mit der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="9ec1e-p115">Jedes Fragezeichen (**?**) verweist auf ein Objekt in der [Parameters](parameters-collection-ado.md)-Auflistung. Das erste Fragezeichen (**?**) verweist auf **Parameters**(0), das nächste Fragezeichen (**?**) auf **Parameters**(1) usw.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="9ec1e-p116">Die Parameterverweise sind optional und hängen von der Struktur der gespeicherten Prozedur ab. Wenn Sie eine gespeicherte Prozedur aufrufen möchten, die keine Parameter definiert, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="9ec1e-262">Wenn zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="9ec1e-p117">Wenn die gespeicherte Prozedur einen Wert zurückgibt, wird der Rückgabewert wie ein weiterer Parameter verwendet. Wenn keine Abfrageparameter verwendet werden, aber ein Rückgabewert vorliegt, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="9ec1e-265">Wenn ein Rückgabewert und zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="9ec1e-266">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="9ec1e-266">Recordset Behavior</span></span>

<span data-ttu-id="9ec1e-267">In den folgenden Tabellen sind die für ein mit diesem Anbieter geöffnetes **Recordset** -Objekt verfügbaren ADO-Standardmethoden und -Eigenschaften aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="9ec1e-268">Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die **Properties** -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="9ec1e-269">Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-269">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="9ec1e-270">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ec1e-270">Property</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-271">ForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-272">Dynamic</span><span class="sxs-lookup"><span data-stu-id="9ec1e-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-273">Keyset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-274">Static</span><span class="sxs-lookup"><span data-stu-id="9ec1e-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-276">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-276">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-277">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-277">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-278">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-279">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-281">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-281">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-282">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-282">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-283">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-284">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-286">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-287">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-288">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-289">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-291">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-292">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-293">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-294">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-295"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-296">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-296">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-297">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-297">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-298">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-299">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-301">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-302">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-303">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-304">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-306">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-307">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-308">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-309">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-310"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-311">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-312">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-313">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-314">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-316">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-317">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-318">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-319">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-320"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-321">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-322">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-323">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-324">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-325"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-326">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-327">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-328">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-329">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-331">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-332">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-333">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-334">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-336">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-337">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-338">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-339">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-341">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-342">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-342">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-343">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-344">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-346">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-347">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-348">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-349">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-351">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-352">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9ec1e-352">not available</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-353">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-354">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-355"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-356">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-357">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-358">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-359">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ec1e-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-360"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-361">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-362">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-363">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-364">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-365"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-366">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-367">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-368">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-369">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="9ec1e-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ec1e-370">Die Eigenschaften [AbsolutePosition](absoluteposition-property-ado.md) und [AbsolutePage](absolutepage-property-ado.md) sind schreibgeschützt, wenn ADO mit der Version 1.0 des Microsoft OLE DB-Anbieters für ODBC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="9ec1e-371">Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="9ec1e-371">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="9ec1e-372">Methode</span><span class="sxs-lookup"><span data-stu-id="9ec1e-372">Method</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-373">ForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-374">Dynamic</span><span class="sxs-lookup"><span data-stu-id="9ec1e-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-375">Keyset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-376">Static</span><span class="sxs-lookup"><span data-stu-id="9ec1e-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-378">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-379">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-380">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-381">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-382"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-383">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-384">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-385">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-386">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-388">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-389">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-390">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-391">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-393">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-394">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-395">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-396">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-397"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-398">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-398">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-399">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-399">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-400">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-401">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-402"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-403">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-404">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-405">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-406">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-408">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-409">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-410">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-411">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-412"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-413">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-414">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-415">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-416">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-417"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-418">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-419">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-420">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-421">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-423">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-424">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-425">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-426">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-428">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-428">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-429">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-430">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-431">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-433">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-434">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-435">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-436">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-438">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-438">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-439">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-440">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-441">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="9ec1e-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-443">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-444">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-445">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-446">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-447"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-448">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-449">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-450">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-451">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-452"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-453">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-454">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-455">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-456">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-457"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-458">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-458">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-459">Nein</span><span class="sxs-lookup"><span data-stu-id="9ec1e-459">No</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-460">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-461">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-462"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-463">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-464">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-465">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-466">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-467"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-468">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-469">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-470">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-471">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="9ec1e-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9ec1e-473">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-474">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-475">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-476">Ja</span><span class="sxs-lookup"><span data-stu-id="9ec1e-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ec1e-477">\*Nicht unterstützt bei Microsoft Access-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="9ec1e-478">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ec1e-478">Dynamic Properties</span></span>

<span data-ttu-id="9ec1e-479">Der Microsoft OLE DB-Anbieter für ODBC fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="9ec1e-p118">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="9ec1e-484">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="9ec1e-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="9ec1e-485">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-486">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-487">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-488">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="9ec1e-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-490">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="9ec1e-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-492">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="9ec1e-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-494">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="9ec1e-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-496">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="9ec1e-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="9ec1e-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-498">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="9ec1e-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="9ec1e-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-500">Column Definition</span><span class="sxs-lookup"><span data-stu-id="9ec1e-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9ec1e-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-502">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="9ec1e-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-504">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="9ec1e-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="9ec1e-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-506">Data Source</span><span class="sxs-lookup"><span data-stu-id="9ec1e-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-508">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="9ec1e-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="9ec1e-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-510">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="9ec1e-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-512">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="9ec1e-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="9ec1e-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-514">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="9ec1e-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="9ec1e-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-516">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="9ec1e-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="9ec1e-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-518">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-520">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-522">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-524">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="9ec1e-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-525">NULL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-526">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="9ec1e-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-528">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="9ec1e-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="9ec1e-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-530">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="9ec1e-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="9ec1e-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-532">Location</span><span class="sxs-lookup"><span data-stu-id="9ec1e-532">Location</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-533">STANDARD</span><span class="sxs-lookup"><span data-stu-id="9ec1e-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-534">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="9ec1e-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-536">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="9ec1e-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-538">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="9ec1e-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="9ec1e-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-540">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-542">Mode</span><span class="sxs-lookup"><span data-stu-id="9ec1e-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-544">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="9ec1e-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-546">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="9ec1e-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-548">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="9ec1e-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-550">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="9ec1e-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-552">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="9ec1e-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="9ec1e-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-554">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="9ec1e-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9ec1e-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-556">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="9ec1e-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-557">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-558">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="9ec1e-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="9ec1e-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-560">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-562">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-564">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="9ec1e-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-566">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="9ec1e-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-568">Password</span><span class="sxs-lookup"><span data-stu-id="9ec1e-568">Password</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="9ec1e-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-570">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="9ec1e-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-572">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="9ec1e-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="9ec1e-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-574">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="9ec1e-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-576">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="9ec1e-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9ec1e-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-578">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="9ec1e-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="9ec1e-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-580">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="9ec1e-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="9ec1e-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-582">Prompt</span><span class="sxs-lookup"><span data-stu-id="9ec1e-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-584">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="9ec1e-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="9ec1e-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-586">Provider Name</span><span class="sxs-lookup"><span data-stu-id="9ec1e-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="9ec1e-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-588">Provider Version</span><span class="sxs-lookup"><span data-stu-id="9ec1e-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="9ec1e-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-590">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="9ec1e-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-592">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="9ec1e-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="9ec1e-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-594">Schema Term</span><span class="sxs-lookup"><span data-stu-id="9ec1e-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="9ec1e-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-596">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="9ec1e-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-598">SQL Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-600">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="9ec1e-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-602">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="9ec1e-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-604">Table Term</span><span class="sxs-lookup"><span data-stu-id="9ec1e-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="9ec1e-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-606">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-608">User ID</span><span class="sxs-lookup"><span data-stu-id="9ec1e-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="9ec1e-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-610">User Name</span><span class="sxs-lookup"><span data-stu-id="9ec1e-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="9ec1e-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-612">Window Handle</span><span class="sxs-lookup"><span data-stu-id="9ec1e-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="9ec1e-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="9ec1e-614">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="9ec1e-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="9ec1e-615">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-616">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-617">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-618">Access Order</span><span class="sxs-lookup"><span data-stu-id="9ec1e-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="9ec1e-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-620">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="9ec1e-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-622">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="9ec1e-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9ec1e-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-626">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-628">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="9ec1e-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-630">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="9ec1e-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-632">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="9ec1e-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-634">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="9ec1e-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-636">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="9ec1e-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="9ec1e-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9ec1e-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9ec1e-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="9ec1e-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="9ec1e-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-648">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9ec1e-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9ec1e-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="9ec1e-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9ec1e-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9ec1e-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-667">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-669">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-671">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-673">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-675">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-677">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-679">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="9ec1e-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-681">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="9ec1e-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-683">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="9ec1e-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-685">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="9ec1e-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-687">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="9ec1e-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-689">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="9ec1e-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-691">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="9ec1e-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="9ec1e-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-693">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="9ec1e-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-695">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="9ec1e-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-697">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="9ec1e-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-699">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="9ec1e-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-701">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-703">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-705">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-707">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="9ec1e-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-709">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="9ec1e-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-711">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="9ec1e-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-713">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-715">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-717">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-719">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-721">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-723">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-725">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="9ec1e-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-727">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="9ec1e-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-729">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-731">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-733">Updatability</span><span class="sxs-lookup"><span data-stu-id="9ec1e-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-735">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="9ec1e-737">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="9ec1e-737">Command Dynamic Properties</span></span>

<span data-ttu-id="9ec1e-738">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9ec1e-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec1e-739">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="9ec1e-740">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9ec1e-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-741">Access Order</span><span class="sxs-lookup"><span data-stu-id="9ec1e-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="9ec1e-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-743">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="9ec1e-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-745">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="9ec1e-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9ec1e-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-749">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-751">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="9ec1e-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-753">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="9ec1e-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-755">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="9ec1e-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-757">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="9ec1e-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-759">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="9ec1e-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="9ec1e-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9ec1e-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="9ec1e-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="9ec1e-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="9ec1e-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-771">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="9ec1e-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9ec1e-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="9ec1e-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="9ec1e-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="9ec1e-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9ec1e-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="9ec1e-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="9ec1e-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-790">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-792">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-794">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-796">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-798">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-800">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-802">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="9ec1e-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-804">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="9ec1e-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-806">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="9ec1e-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-808">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="9ec1e-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-810">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="9ec1e-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-812">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="9ec1e-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-814">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="9ec1e-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="9ec1e-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-816">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="9ec1e-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-818">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="9ec1e-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="9ec1e-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-820">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="9ec1e-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="9ec1e-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-822">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="9ec1e-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-824">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-826">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-828">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-830">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="9ec1e-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-832">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="9ec1e-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-834">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="9ec1e-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="9ec1e-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-836">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-838">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-840">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="9ec1e-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-842">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-844">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-846">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="9ec1e-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="9ec1e-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-848">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="9ec1e-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-850">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="9ec1e-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-852">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="9ec1e-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec1e-854">Updatability</span><span class="sxs-lookup"><span data-stu-id="9ec1e-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="9ec1e-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ec1e-856">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="9ec1e-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="9ec1e-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="9ec1e-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9ec1e-858">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ec1e-858">See also</span></span>

<span data-ttu-id="9ec1e-859">Weitere Informationen zur Implementierung und funktionale Informationen zu den Microsoft OLE DB-Anbieter für ODBC wenden Sie sich an dem [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) oder besuchen Sie das [Data Plattform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="9ec1e-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

