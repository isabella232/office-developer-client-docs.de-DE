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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288911"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="10604-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="10604-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="10604-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10604-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10604-p101">Unter idealen Bedingungen für einen ADO- oder RDS-Programmierer wäre für jede Datenquelle eine OLE DB-Schnittstelle verfügbar, sodass ADO Aufrufe direkt in der Datenquelle ausführen könnte. Obwohl Datenbankanbieter zunehmend OLE DB-Schnittstellen implementieren, sind einige Datenquellen noch nicht auf diese Weise verfügbar. Dennoch kann auf praktisch alle heutigen DBMS-Systeme über ODBC zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="10604-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="10604-107">ODBC-Treiber sind für alle größeren DBMS-Systeme von heute verfügbar, so auch für Microsoft SQL Server, Microsoft Access (Microsoft Jet-Datenbankmodul) und Microsoft FoxPro sowie für Datenbankprodukte, die nicht von Microsoft stammen, wie z. B. Oracle.</span><span class="sxs-lookup"><span data-stu-id="10604-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="10604-p102">Mithilfe des Microsoft ODBC-Anbieters kann ADO jedoch eine Verbindung mit einer ODBC-Datenquelle herstellen. Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="10604-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="10604-p103">Der Anbieter unterstützt Transaktionen, wenngleich unterschiedliche DBMS-Module Transaktionen auf unterschiedliche Art unterstützen. So unterstützt Microsoft Access beispielsweise bis zu fünf Ebenen tief geschachtelte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="10604-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="10604-112">Hierbei handelt es sich um den Standardanbieter für ADO. Alle vom Anbieter abhängigen ADO-Eigenschaften und -Methoden werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10604-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="10604-113">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="10604-113">Connection String Parameters</span></span>

<span data-ttu-id="10604-114">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=**-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="10604-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="10604-115">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10604-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="10604-116">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="10604-116">Typical Connection String</span></span>

<span data-ttu-id="10604-117">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="10604-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="10604-118">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="10604-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-119">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="10604-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="10604-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10604-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="10604-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="10604-122">Gibt den OLE DB-Anbieter für ODBC an.</span><span class="sxs-lookup"><span data-stu-id="10604-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="10604-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="10604-124">Gibt den Namen der Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="10604-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="10604-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="10604-126">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="10604-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="10604-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="10604-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="10604-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="10604-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="10604-130">Gibt die URL einer Datei oder eines Verzeichnisses an, die in einem Webordner veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="10604-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10604-131">Da es sich hierbei um den Standardanbieter für ADO handelt, versucht ADO eine Verbindung mit diesem Anbieter herzustellen, wenn Sie den **Provider=** -Parameter in der Verbindungsreihenfolge nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="10604-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="10604-p104">Der Anbieter unterstützt neben den von ADO definierten keine bestimmten Verbindungsparameter. Der Anbieter übergibt jedoch alle Verbindungsparameter, die nicht von ADO stammen, an den ODBC-Treibermanager.</span><span class="sxs-lookup"><span data-stu-id="10604-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="10604-p105">Da Sie den **Provider**-Parameter nicht angeben müssen, können Sie eine ADO-Verbindungszeichenfolge erstellen, die mit einer ODBC-Verbindungszeichenfolge für dieselbe Datenquelle identisch ist. Verwenden Sie dieselben Parameternamen (**DRIVER=**, **DATABASE=**, **DSN=** usw.) und Werte und dieselbe Syntax wie beim Erstellen einer ODBC-Verbindungszeichenfolge. Sie können eine Verbindung mit oder ohne vordefinierten Datenquellennamen (DSN) oder Datei-DSN herstellen.</span><span class="sxs-lookup"><span data-stu-id="10604-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="10604-137">**Syntax mit einem DSN oder Datei-DSN:**</span><span class="sxs-lookup"><span data-stu-id="10604-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="10604-138">**Syntax ohne einen DSN (Verbindung ohne DSN):**</span><span class="sxs-lookup"><span data-stu-id="10604-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="10604-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="10604-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="10604-142">Alternativ zum Festlegen eines **DSN** können Sie auch den ODBC-Treiber (**DRIVER=**), wie z. B. "SQL Server", den Servernamen (**SERVER=**) und den Datenbanknamen (**DATABASE=**) angeben.</span><span class="sxs-lookup"><span data-stu-id="10604-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="10604-143">Sie können auch den Namen (**UID=**) und das Kennwort für ein Benutzerkonto (**PWD=**) in den ODBC-spezifischen Parametern oder in den von ADO definierten Standardparametern *user* und *password* angeben.</span><span class="sxs-lookup"><span data-stu-id="10604-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="10604-144">Obwohl eine **DSN** -Definition bereits eine Datenbank angibt, können Sie zusätzlich zu einem **DSN** *einen* *Daten Bank* Parameter angeben, um eine Verbindung mit einer anderen Datenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="10604-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="10604-145">Es empfiehlt sich, bei Verwendung eines **DSN**immer *den* Parameter *Database* einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="10604-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="10604-146">Dadurch wird sichergestellt, dass Sie eine Verbindung mit der richtigen Datenbank herstellen, falls ein anderer Benutzer den Standarddaten Bankparameter seit der letzten Überprüfung der **DSN** -Definition geändert hat.</span><span class="sxs-lookup"><span data-stu-id="10604-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="10604-147">Anbieterspezifische Verbindungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="10604-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="10604-p108">Der OLE DB-Anbieter für ODBC fügt der [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts verschiedene Eigenschaften hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="10604-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-150">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="10604-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10604-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-152">Zugängliche Verfahren</span><span class="sxs-lookup"><span data-stu-id="10604-152">Accessible Procedures</span></span><br />
<span data-ttu-id="10604-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="10604-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="10604-154">Gibt an, ob der Benutzer Zugriff auf gespeicherte Prozeduren hat.</span><span class="sxs-lookup"><span data-stu-id="10604-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-155">Barrierefreie Tabellen</span><span class="sxs-lookup"><span data-stu-id="10604-155">Accessible Tables</span></span><br />
<span data-ttu-id="10604-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="10604-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="10604-157">Gibt an, ob der Benutzer über die Berechtigung zum Ausführen der SELECT-Anweisungen in Datenbanktabellen verfügt.</span><span class="sxs-lookup"><span data-stu-id="10604-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-158">Aktive Anweisungen</span><span class="sxs-lookup"><span data-stu-id="10604-158">Active Statements</span></span><br />
<span data-ttu-id="10604-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="10604-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="10604-160">Gibt die Anzahl von Handles an, die ein ODBC-Treiber in einer Verbindung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="10604-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-161">Treiber Name</span><span class="sxs-lookup"><span data-stu-id="10604-161">Driver Name</span></span><br />
<span data-ttu-id="10604-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="10604-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="10604-163">Gibt den Dateinamen des ODBC-Treibers an.</span><span class="sxs-lookup"><span data-stu-id="10604-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-164">Treiber-ODBC-Version</span><span class="sxs-lookup"><span data-stu-id="10604-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="10604-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="10604-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="10604-166">Gibt die Version von ODBC an, die von diesem Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="10604-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-167">Datei Verwendung</span><span class="sxs-lookup"><span data-stu-id="10604-167">File Usage</span></span><br />
<span data-ttu-id="10604-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="10604-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="10604-169">Gibt an, wie der Treiber eine Datei in einer Datenquelle behandelt: als Tabelle oder als Katalog.</span><span class="sxs-lookup"><span data-stu-id="10604-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-170">Like-Escape-Klausel</span><span class="sxs-lookup"><span data-stu-id="10604-170">Like Escape Clause</span></span><br />
<span data-ttu-id="10604-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="10604-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="10604-172">Gibt an, ob der Treiber die Definition und Verwendung eines Escapezeichens für das Prozentzeichen (%) und das Unterstrichzeichen (_) im LIKE-Prädikat einer WHERE-Klausel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10604-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-173">Maximale Anzahl von Spalten in Group by</span><span class="sxs-lookup"><span data-stu-id="10604-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="10604-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="10604-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="10604-175">Gibt die maximale Anzahl von Spalten an, die in der GROUP BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="10604-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-176">Maximale Anzahl von Spalten im Index</span><span class="sxs-lookup"><span data-stu-id="10604-176">Max Columns in Index</span></span><br />
<span data-ttu-id="10604-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="10604-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="10604-178">Gibt die maximale Anzahl von Spalten an, die in einem Index enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="10604-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-179">Maximale Anzahl von Spalten in der Reihenfolge nach</span><span class="sxs-lookup"><span data-stu-id="10604-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="10604-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="10604-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="10604-181">Gibt die maximale Anzahl von Spalten an, die in der ORDER BY-Klausel einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="10604-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-182">Maximale Anzahl von Spalten in SELECT</span><span class="sxs-lookup"><span data-stu-id="10604-182">Max Columns in Select</span></span><br />
<span data-ttu-id="10604-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="10604-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="10604-184">Gibt die maximale Anzahl von Spalten an, die im SELECT-Teil einer SELECT-Anweisung enthalten sein darf.</span><span class="sxs-lookup"><span data-stu-id="10604-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-185">Maximale Anzahl von Spalten in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="10604-185">Max Columns in Table</span></span><br />
<span data-ttu-id="10604-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="10604-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="10604-187">Gibt die maximale Anzahl von Spalten an, die in einer Tabelle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="10604-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-188">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="10604-188">Numeric Functions</span></span><br />
<span data-ttu-id="10604-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10604-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10604-p109">Gibt an, welche numerischen Funktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="10604-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-192">Outer Join-Funktionen</span><span class="sxs-lookup"><span data-stu-id="10604-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="10604-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="10604-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="10604-194">Gibt die vom Anbieter unterstützten OUTER JOIN-Typen an.</span><span class="sxs-lookup"><span data-stu-id="10604-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-195">Outer-Joins</span><span class="sxs-lookup"><span data-stu-id="10604-195">Outer Joins</span></span><br />
<span data-ttu-id="10604-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="10604-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="10604-197">Gibt an, ob der Anbieter OUTER JOIN-Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10604-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-198">SonderZeichen</span><span class="sxs-lookup"><span data-stu-id="10604-198">Special Characters</span></span><br />
<span data-ttu-id="10604-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="10604-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="10604-200">Gibt an, welche Zeichen eine besondere Bedeutung für den ODBC-Treiber haben.</span><span class="sxs-lookup"><span data-stu-id="10604-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-201">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="10604-201">Stored Procedures</span></span><br />
<span data-ttu-id="10604-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="10604-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="10604-203">Gibt an, ob gespeicherte Prozeduren für die Verwendung mit diesem ODBC-Treiber verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="10604-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-204">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="10604-204">String Functions</span></span><br />
<span data-ttu-id="10604-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10604-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10604-p110">Gibt an, welche Zeichenfolgenfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="10604-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-208">System Funktionen</span><span class="sxs-lookup"><span data-stu-id="10604-208">System Functions</span></span><br />
<span data-ttu-id="10604-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10604-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10604-p111">Gibt an, welche Systemfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="10604-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-212">Zeit/Datum-Funktionen</span><span class="sxs-lookup"><span data-stu-id="10604-212">Time/Date Functions</span></span><br />
<span data-ttu-id="10604-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="10604-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="10604-p112">Gibt an, welche Uhrzeit- und Datumsfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</span><span class="sxs-lookup"><span data-stu-id="10604-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-216">SQL-Grammatik Unterstützung</span><span class="sxs-lookup"><span data-stu-id="10604-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="10604-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="10604-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="10604-218">Gibt die SQL-Grammatik an, die von diesem ODBC-Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="10604-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="10604-219">Anwenderspezifische Recordset- und Command-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10604-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="10604-p113">Der OLE DB-Anbieter für ODBC fügt der **Properties**-Auflistung der Objekte **Recordset** und **Command** verschiedene Objekte hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="10604-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-222">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="10604-223">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10604-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-224">Abfragebasierte Aktualisierungen/Löschungen/einFügungen</span><span class="sxs-lookup"><span data-stu-id="10604-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="10604-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="10604-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="10604-226">Gibt an, ob Aktualisierungen und Lösch- und Einfügevorgänge mithilfe von SQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="10604-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-227">ODBC-Parallelitätstyp</span><span class="sxs-lookup"><span data-stu-id="10604-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="10604-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="10604-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="10604-229">Gibt die Methode an, die verwendet wird, um potenzielle Probleme zu reduzieren, die von zwei Benutzern verursacht werden, die gleichzeitig auf dieselben Daten in der Datenquelle zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="10604-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-230">BLOB-Barrierefreiheit bei Vorwärtscursor</span><span class="sxs-lookup"><span data-stu-id="10604-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="10604-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="10604-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="10604-232">Gibt an, ob auf BLOB-<strong>Felder</strong> zugegriffen werden kann, wenn ein Vorwärtscursor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10604-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-233">Include SQL_FLOAT, SQL_DOUBLE und SQL_REAL in QBU WHERE-Klauseln</span><span class="sxs-lookup"><span data-stu-id="10604-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="10604-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="10604-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="10604-235">Gibt an, ob die Werte SQL_FLOAT, SQL_DOUBLE und SQL_REAL in eine QBU WHERE-Klausel eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="10604-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-236">Position in der letzten Zeile nach dem Einfügen</span><span class="sxs-lookup"><span data-stu-id="10604-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="10604-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="10604-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="10604-238">Gibt an, dass nach dem Einfügen eines neuen Datensatzes in eine Tabelle die letzte Zeile zur aktuellen Zeile wird.</span><span class="sxs-lookup"><span data-stu-id="10604-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="10604-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="10604-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="10604-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="10604-241">Gibt an, ob die <strong>IRowsetChange</strong>-Schnittstelle erweiterte Informationsunterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="10604-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-242">ODBC-Cursortyp</span><span class="sxs-lookup"><span data-stu-id="10604-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="10604-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="10604-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="10604-244">Gibt den Cursortyp an, der vom <strong>Recordset</strong>-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10604-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-245">Generieren eines Rowsets, das gemarshallt werden kann</span><span class="sxs-lookup"><span data-stu-id="10604-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="10604-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="10604-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="10604-247">Gibt an, dass der ODBC-Treiber eine Datensatzgruppe generiert, die gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="10604-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="10604-248">Befehlstext</span><span class="sxs-lookup"><span data-stu-id="10604-248">Command Text</span></span>

<span data-ttu-id="10604-249">Die Verwendung des [Command](command-object-ado.md)-Objekts hängt zum großen Teil von der Datenquelle sowie vom Typ der Abfrage- oder Befehlsanweisung, die akzeptiert wird, ab.</span><span class="sxs-lookup"><span data-stu-id="10604-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="10604-p114">ODBC stellt eine bestimmte Syntax zum Aufrufen von gespeicherten Prozeduren bereit. Bei der [CommandText](commandtext-property-ado.md)-Eigenschaft eines **Command**-Objekts übergibt das *CommandText*-Argument der **Execute**-Methode in einem [Connection](connection-object-ado.md)-Objekt oder das *Source*-Argument der **Open**-Methode in einem [Recordset](recordset-object-ado.md)-Objekt eine Zeichenfolge mit der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="10604-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="10604-252">Jedes Fragezeichen ( **?**</span><span class="sxs-lookup"><span data-stu-id="10604-252">Each **?**</span></span> <span data-ttu-id="10604-253">) verweist auf ein Objekt in der [Parameters](parameters-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="10604-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="10604-254">Das erste Fragezeichen ( **?**</span><span class="sxs-lookup"><span data-stu-id="10604-254">The first **?**</span></span> <span data-ttu-id="10604-255">Verweise **Parameter**(0), die nächste **?**</span><span class="sxs-lookup"><span data-stu-id="10604-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="10604-256">referenziert **Parameter**(1) usw.</span><span class="sxs-lookup"><span data-stu-id="10604-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="10604-p116">Die Parameterverweise sind optional und hängen von der Struktur der gespeicherten Prozedur ab. Wenn Sie eine gespeicherte Prozedur aufrufen möchten, die keine Parameter definiert, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="10604-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="10604-259">Wenn zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="10604-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="10604-p117">Wenn die gespeicherte Prozedur einen Wert zurückgibt, wird der Rückgabewert wie ein weiterer Parameter verwendet. Wenn keine Abfrageparameter verwendet werden, aber ein Rückgabewert vorliegt, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="10604-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="10604-262">Wenn ein Rückgabewert und zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="10604-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="10604-263">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="10604-263">Recordset Behavior</span></span>

<span data-ttu-id="10604-264">In den folgenden Tabellen sind die für ein mit diesem Anbieter geöffnetes **Recordset**-Objekt verfügbaren ADO-Standardmethoden und -Eigenschaften aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="10604-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="10604-265">Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die **Properties** -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="10604-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="10604-266">Verfügbarkeit von ADO-Standardeigenschaften des **Recordset**-Objekts:</span><span class="sxs-lookup"><span data-stu-id="10604-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="10604-267">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10604-267">Property</span></span></p></th>
<th><p><span data-ttu-id="10604-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="10604-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="10604-269">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="10604-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="10604-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="10604-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="10604-271">Static</span><span class="sxs-lookup"><span data-stu-id="10604-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="10604-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="10604-273">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-273">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-274">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-274">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-275">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-276">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="10604-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="10604-278">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-278">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-279">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-279">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-280">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-281">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="10604-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="10604-283">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-284">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-285">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-286">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="10604-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="10604-288">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-289">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-290">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-291">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="10604-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="10604-293">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-293">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-294">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-294">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-295">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-296">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="10604-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="10604-298">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-299">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-300">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-301">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="10604-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="10604-303">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-304">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-305">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-306">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="10604-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="10604-308">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-309">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-310">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-311">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="10604-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="10604-313">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-314">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-315">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-316">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="10604-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="10604-318">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-319">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-320">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-321">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="10604-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="10604-323">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-324">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-325">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-326">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="10604-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="10604-328">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-329">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-330">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-331">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="10604-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="10604-333">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-334">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-335">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-336">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="10604-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="10604-338">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-339">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-339">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-340">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-341">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="10604-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="10604-343">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-344">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-345">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-346">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="10604-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="10604-348">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-349">nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="10604-349">not available</span></span></p></td>
<td><p><span data-ttu-id="10604-350">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-351">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="10604-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="10604-353">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-354">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-355">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="10604-356">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10604-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="10604-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="10604-358">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-359">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-360">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-361">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="10604-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="10604-363">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-364">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-365">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="10604-366">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10604-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10604-367">Die Eigenschaften [AbsolutePosition](absoluteposition-property-ado.md) und [AbsolutePage](absolutepage-property-ado.md) sind schreibgeschützt, wenn ADO mit der Version 1.0 des Microsoft OLE DB-Anbieters für ODBC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10604-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="10604-368">Verfügbarkeit von ADO-Standardmethoden des **Recordset**-Objekts:</span><span class="sxs-lookup"><span data-stu-id="10604-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="10604-369">Methode</span><span class="sxs-lookup"><span data-stu-id="10604-369">Method</span></span></p></th>
<th><p><span data-ttu-id="10604-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="10604-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="10604-371">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="10604-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="10604-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="10604-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="10604-373">Static</span><span class="sxs-lookup"><span data-stu-id="10604-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="10604-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="10604-375">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-376">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-377">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-378">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="10604-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="10604-380">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-381">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-382">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-383">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="10604-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="10604-385">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-386">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-387">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-388">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="10604-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="10604-390">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-391">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-392">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-393">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="10604-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="10604-395">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-395">No</span></span></p></td>
<td><p><span data-ttu-id="10604-396">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-396">No</span></span></p></td>
<td><p><span data-ttu-id="10604-397">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-398">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="10604-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="10604-400">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-401">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-402">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-403">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="10604-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="10604-405">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-406">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-407">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-408">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="10604-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="10604-410">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-411">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-412">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-413">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="10604-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="10604-415">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-416">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-417">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-418">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="10604-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="10604-420">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-421">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-422">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-423">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="10604-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="10604-425">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-425">No</span></span></p></td>
<td><p><span data-ttu-id="10604-426">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-427">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-428">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="10604-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="10604-430">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-431">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-432">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-433">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="10604-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="10604-435">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-435">No</span></span></p></td>
<td><p><span data-ttu-id="10604-436">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-437">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-438">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="10604-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="10604-440">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-441">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-442">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-443">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="10604-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="10604-445">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-446">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-447">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-448">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="10604-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="10604-450">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-451">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-452">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-453">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="10604-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="10604-455">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-455">No</span></span></p></td>
<td><p><span data-ttu-id="10604-456">Nein</span><span class="sxs-lookup"><span data-stu-id="10604-456">No</span></span></p></td>
<td><p><span data-ttu-id="10604-457">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-458">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-459"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="10604-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="10604-460">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-461">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-462">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-463">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="10604-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="10604-465">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-466">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-467">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-468">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="10604-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="10604-470">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-471">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-472">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="10604-473">Ja</span><span class="sxs-lookup"><span data-stu-id="10604-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10604-474">\*Nicht unterstützt bei Microsoft Access-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="10604-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="10604-475">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10604-475">Dynamic Properties</span></span>

<span data-ttu-id="10604-476">Der Microsoft OLE DB-Anbieter für ODBC fügt verschiedene Eigenschaften in die **Properties**-Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="10604-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="10604-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="10604-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="10604-481">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="10604-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="10604-482">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Connection**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10604-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-483">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10604-484">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="10604-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="10604-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="10604-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="10604-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="10604-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="10604-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="10604-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="10604-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="10604-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="10604-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="10604-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="10604-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="10604-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="10604-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="10604-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="10604-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="10604-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="10604-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="10604-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="10604-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="10604-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="10604-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="10604-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="10604-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="10604-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="10604-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="10604-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="10604-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="10604-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="10604-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="10604-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="10604-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="10604-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="10604-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10604-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10604-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="10604-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="10604-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="10604-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="10604-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="10604-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="10604-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="10604-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="10604-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="10604-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="10604-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="10604-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="10604-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="10604-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="10604-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="10604-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="10604-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="10604-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="10604-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="10604-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="10604-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="10604-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="10604-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="10604-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="10604-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="10604-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="10604-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="10604-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="10604-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="10604-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="10604-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-529">Standort</span><span class="sxs-lookup"><span data-stu-id="10604-529">Location</span></span></p></td>
<td><p><span data-ttu-id="10604-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="10604-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="10604-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="10604-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="10604-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="10604-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="10604-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="10604-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="10604-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="10604-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="10604-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="10604-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="10604-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="10604-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-539">Mode</span><span class="sxs-lookup"><span data-stu-id="10604-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="10604-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="10604-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="10604-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="10604-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="10604-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="10604-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="10604-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="10604-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10604-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10604-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="10604-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="10604-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="10604-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="10604-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="10604-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="10604-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="10604-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="10604-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10604-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="10604-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="10604-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="10604-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="10604-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="10604-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="10604-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="10604-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="10604-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="10604-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="10604-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="10604-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="10604-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="10604-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="10604-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="10604-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="10604-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="10604-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-565">Password</span><span class="sxs-lookup"><span data-stu-id="10604-565">Password</span></span></p></td>
<td><p><span data-ttu-id="10604-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="10604-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="10604-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="10604-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="10604-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="10604-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="10604-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="10604-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="10604-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="10604-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="10604-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="10604-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="10604-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10604-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="10604-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="10604-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="10604-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="10604-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="10604-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="10604-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="10604-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="10604-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="10604-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="10604-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="10604-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="10604-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="10604-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="10604-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="10604-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="10604-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="10604-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="10604-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="10604-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="10604-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="10604-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="10604-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="10604-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="10604-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="10604-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="10604-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="10604-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="10604-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="10604-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="10604-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="10604-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="10604-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="10604-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="10604-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="10604-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="10604-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="10604-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="10604-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="10604-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="10604-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="10604-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="10604-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="10604-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="10604-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="10604-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-605">User ID</span><span class="sxs-lookup"><span data-stu-id="10604-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="10604-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="10604-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-607">User Name</span><span class="sxs-lookup"><span data-stu-id="10604-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="10604-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="10604-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="10604-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="10604-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="10604-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="10604-611">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="10604-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="10604-612">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Recordset**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10604-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-613">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10604-614">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="10604-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="10604-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="10604-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10604-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10604-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="10604-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="10604-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="10604-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="10604-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="10604-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="10604-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="10604-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="10604-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="10604-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="10604-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10604-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="10604-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="10604-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="10604-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="10604-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="10604-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="10604-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10604-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="10604-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="10604-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="10604-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="10604-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="10604-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10604-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10604-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10604-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="10604-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10604-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10604-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="10604-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10604-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="10604-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="10604-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="10604-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="10604-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="10604-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="10604-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="10604-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="10604-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10604-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="10604-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10604-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10604-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="10604-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10604-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10604-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10604-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10604-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="10604-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10604-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="10604-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10604-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="10604-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10604-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10604-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="10604-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10604-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10604-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10604-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10604-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="10604-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10604-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10604-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="10604-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="10604-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="10604-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="10604-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="10604-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="10604-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="10604-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="10604-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="10604-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="10604-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="10604-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="10604-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="10604-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="10604-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="10604-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="10604-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="10604-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="10604-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="10604-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="10604-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="10604-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="10604-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10604-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="10604-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="10604-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10604-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="10604-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="10604-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="10604-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="10604-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="10604-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="10604-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="10604-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="10604-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="10604-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="10604-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="10604-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="10604-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="10604-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="10604-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10604-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="10604-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10604-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="10604-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="10604-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10604-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="10604-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="10604-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="10604-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10604-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10604-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10604-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="10604-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10604-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="10604-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="10604-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="10604-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="10604-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="10604-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="10604-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10604-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="10604-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="10604-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10604-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="10604-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="10604-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="10604-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="10604-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="10604-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="10604-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10604-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="10604-734">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="10604-734">Command Dynamic Properties</span></span>

<span data-ttu-id="10604-735">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Command**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10604-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10604-736">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="10604-737">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="10604-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10604-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="10604-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="10604-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="10604-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="10604-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="10604-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="10604-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="10604-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="10604-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="10604-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="10604-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="10604-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="10604-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="10604-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="10604-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="10604-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10604-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="10604-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="10604-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="10604-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="10604-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="10604-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="10604-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="10604-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10604-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="10604-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="10604-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="10604-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="10604-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="10604-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10604-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="10604-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10604-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="10604-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="10604-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10604-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="10604-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="10604-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="10604-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="10604-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="10604-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="10604-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="10604-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="10604-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="10604-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="10604-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10604-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="10604-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="10604-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10604-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="10604-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="10604-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10604-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="10604-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10604-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="10604-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="10604-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="10604-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10604-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="10604-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="10604-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10604-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="10604-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="10604-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10604-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="10604-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="10604-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10604-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="10604-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10604-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10604-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="10604-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="10604-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="10604-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="10604-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="10604-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="10604-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="10604-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="10604-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="10604-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="10604-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="10604-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="10604-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="10604-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="10604-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="10604-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="10604-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="10604-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="10604-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="10604-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="10604-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="10604-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="10604-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10604-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="10604-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="10604-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="10604-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="10604-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="10604-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="10604-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="10604-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="10604-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="10604-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="10604-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="10604-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="10604-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="10604-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="10604-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="10604-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="10604-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="10604-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="10604-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10604-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="10604-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10604-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="10604-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="10604-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="10604-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="10604-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="10604-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="10604-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="10604-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="10604-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="10604-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="10604-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="10604-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="10604-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="10604-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="10604-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="10604-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="10604-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="10604-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="10604-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="10604-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="10604-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="10604-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="10604-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="10604-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="10604-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="10604-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="10604-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10604-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="10604-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="10604-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="10604-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10604-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="10604-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="10604-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="10604-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="10604-855">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10604-855">See also</span></span>

<span data-ttu-id="10604-856">Ausführliche Informationen zu spezifischen Implementierungs-und Funktionsinformationen zum Microsoft OLE DB-Anbieter für ODBC finden Sie im [OLE DB Programmer es Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) oder im [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="10604-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

