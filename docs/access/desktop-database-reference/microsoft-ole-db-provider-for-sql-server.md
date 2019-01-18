---
title: Microsoft OLE DB-Anbieter für SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705106"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="bde0c-102">Microsoft OLE DB-Anbieter für SQL Server</span><span class="sxs-lookup"><span data-stu-id="bde0c-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="bde0c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bde0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bde0c-104">SQLOLEDB, der OLE DB-Anbieter für SQL Server, ermöglicht ADO den Zugriff auf Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bde0c-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="bde0c-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="bde0c-105">Connection String Parameters</span></span>

<span data-ttu-id="bde0c-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="bde0c-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="bde0c-107">Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft gesetzt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="bde0c-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="bde0c-108">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bde0c-108">Typical Connection String</span></span>

<span data-ttu-id="bde0c-109">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="bde0c-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="bde0c-110">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="bde0c-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bde0c-111">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="bde0c-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="bde0c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bde0c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="bde0c-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="bde0c-114">Gibt den OLE DB-Anbieter für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-115"><strong>Data Source</strong> oder <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bde0c-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bde0c-116">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-117"><strong>Initial Catalog</strong> oder <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="bde0c-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="bde0c-118">Gibt den Namen einer Datenbank auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-119"><strong>User ID</strong> oder <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="bde0c-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="bde0c-120">Gibt den Benutzernamen (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-121"><strong>Password</strong> oder <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="bde0c-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="bde0c-122">Gibt das Benutzerkennwort (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="bde0c-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="bde0c-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="bde0c-p101">Der Anbieter unterstützt neben den von ADO definierten verschiedene anbieterspezifische Verbindungsparameter. Wie die ADO-Verbindungseigenschaften können diese anbieterspezifischen Eigenschaften über die [Properties](properties-collection-ado.md)-Auflistung eines [Connection](connection-object-ado.md)-Objekts oder als Teil der **ConnectionString** -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bde0c-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde0c-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="bde0c-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bde0c-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="bde0c-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="bde0c-p102">Gibt den Benutzerauthentifizierungsmodus an. Dieser kann auf <strong>Yes</strong> oder <strong>No</strong> gesetzt werden. Der Standardwert ist <strong>No</strong>. Wenn diese Eigenschaft auf <strong>Yes</strong> gesetzt ist, verwendet SQLOLEDB den Microsoft Windows NT-Authentifizierungsmodus, um den Benutzerzugriff auf die in den Eigenschaftswerten <strong>Location</strong> und <a href="datasource-property-ado.md">Datasource</a> angegebene SQL Server-Datenbank zu autorisieren. Wenn diese Eigenschaft auf <strong>No</strong> gesetzt ist, verwendet SQLOLEDB den gemischten Modus, um den Benutzerzugriff auf die SQL Server-Datenbank zu autorisieren. Der Anmeldename und das Kennwort für SQL Server sind in den Eigenschaften <strong>User Id</strong> und <strong>Password</strong> angegeben.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="bde0c-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="bde0c-p103">Gibt den Namen einer SQL Server-Sprache an. Erkennt die Sprache, die für die Auswahl und Formatierung von Systemmeldungen verwendet wird. Die Sprache muss auf dem Computer mit SQL Server installiert sein, da die Verbindung sonst nicht geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="bde0c-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="bde0c-140">Gibt die Netzwerkadresse des Computers mit SQL Server an, die in der <strong>Location</strong>-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bde0c-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="bde0c-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="bde0c-142">Gibt den Namen der Netzwerkbibliothek (Dynamic Link Libraries) verwendet, um eine Kommunikation mit dem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bde0c-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="bde0c-143">Der Name darf nicht den Pfad oder der DLL-Erweiterung enthalten.</span><span class="sxs-lookup"><span data-stu-id="bde0c-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="bde0c-144">Der Standardwert ist von der SQL Server-Clientkonfigurationsprogramm bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bde0c-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="bde0c-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="bde0c-146">Gibt an, ob SQL Server temporäre gespeicherte Prozeduren erstellt, wenn Befehle (von der <strong>Prepared</strong>-Eigenschaft) vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="bde0c-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="bde0c-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="bde0c-p105">Gibt an, ob OEM/ANSI-Zeichen konvertiert werden. Diese Eigenschaft kann auf <strong>True</strong> oder <strong>False</strong> festgelegt werden. Der Standardwert lautet <strong>True</strong>. Wenn diese Eigenschaft auf <strong>True</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen beim Empfangen oder Senden von Mehrbyte-Zeichenfolgen von oder an den Computer mit SQL Server. Wenn diese Eigenschaft auf <strong>False</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen in Daten mit Mehrbyte-Zeichenfolgen nicht.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="bde0c-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="bde0c-p106">Gibt eine Netzwerkpaketgröße in Bytes an. Der Wert für die Eigenschaft der Paketgröße muss zwischen 512 und 32767 liegen. Der Standardwert für die Größe von SQLOLEDB-Netzwerkpaketen beträgt 4096.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-158">Gibt den Namen der Clientanwendung an.</span><span class="sxs-lookup"><span data-stu-id="bde0c-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="bde0c-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="bde0c-160">Eine Zeichenfolge, die die Arbeitsstation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bde0c-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="bde0c-161">Verwendung des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="bde0c-161">Command Object Usage</span></span>

<span data-ttu-id="bde0c-p107">SQLOLEDB akzeptiert eine Mischung aus ODBC, ANSI und SQL Server-spezifischem Transact-SQL als gültige Syntax. In der folgenden SQL-Anweisung wird beispielsweise eine ODBC SQL-Escapesequenz zum Angeben der LCASE-Zeichenfolgenfunktion verwendet:</span><span class="sxs-lookup"><span data-stu-id="bde0c-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="bde0c-p108">LCASE gibt eine Zeichenfolge zurück und konvertiert dabei alle Großbuchstaben in die entsprechenden Kleinbuchstaben. Die ANSI SQL-Zeichenfolgenfunktion LOWER führt denselben Vorgang aus. Die folgende SQL-Anweisung ist somit die Entsprechung der oben dargestellten ODBC-Anweisung in ANSI:</span><span class="sxs-lookup"><span data-stu-id="bde0c-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="bde0c-166">SQLOLEDB verarbeitet beide Formen der Anweisung, sofern diese als Text für einen Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bde0c-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="bde0c-167">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="bde0c-167">Stored Procedures</span></span>

<span data-ttu-id="bde0c-p109">Verwenden Sie beim Ausführen einer gespeicherten SQL Server-Prozedur mit einem SQLOLEDB-Befehl die Escapesequenz des ODBC-Prozeduraufrufs im Befehlstext. SQLOLEDB verwendet dann den Remoteprozeduraufruf von SQL Server, um die Befehlsverarbeitung zu optimieren. So sollte beispielsweise die folgende ODBC SQL-Anweisung anstelle der Transact-SQL-Anweisung als Befehlstext verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="bde0c-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="bde0c-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="bde0c-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="bde0c-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="bde0c-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="bde0c-173">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="bde0c-173">Recordset Behavior</span></span>

<span data-ttu-id="bde0c-p110">SQLOLEDB kann keine SQL Server-Cursor verwenden, um die mehrfachen Ergebnisse, die von mehreren Befehlen generiert werden, zu unterstützen. Wenn ein Consumer eine Datensatzgruppe anfordert und die Unterstützung von SQL Server-Cursor erforderlich ist, tritt ein Fehler auf, sofern der verwendete Befehlstext mehrere Datensatzgruppen als Ergebnis generiert.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="bde0c-p111">SQL Server-Cursor unterstützen scrollfähige SQLOLEDB-Datensatzgruppen. SQL Server legt Einschränkungen für Cursor fest, die von Änderungen abhängen, die andere Benutzer an der Datenbank vornehmen. So können insbesondere die Zeilen in einigen Cursorn nicht sortiert werden, und beim Erstellen einer Datensatzgruppe mit einem Befehl, der eine ORDER BY-Klausel von SQL enthält, tritt möglicherweise ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bde0c-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="bde0c-179">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bde0c-179">Dynamic Properties</span></span>

<span data-ttu-id="bde0c-180">Der Microsoft OLE DB-Anbieter für SQL Server fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="bde0c-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="bde0c-p112">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties (in Englisch).</span><span class="sxs-lookup"><span data-stu-id="bde0c-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="bde0c-185">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="bde0c-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="bde0c-186">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bde0c-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bde0c-187">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bde0c-188">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="bde0c-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="bde0c-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="bde0c-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="bde0c-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="bde0c-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="bde0c-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="bde0c-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="bde0c-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="bde0c-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="bde0c-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="bde0c-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="bde0c-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="bde0c-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="bde0c-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="bde0c-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="bde0c-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="bde0c-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="bde0c-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="bde0c-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="bde0c-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="bde0c-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="bde0c-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="bde0c-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bde0c-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="bde0c-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="bde0c-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="bde0c-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="bde0c-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="bde0c-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="bde0c-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="bde0c-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="bde0c-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bde0c-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bde0c-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="bde0c-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="bde0c-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="bde0c-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="bde0c-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="bde0c-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="bde0c-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="bde0c-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="bde0c-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="bde0c-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="bde0c-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="bde0c-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="bde0c-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="bde0c-226">NULL</span><span class="sxs-lookup"><span data-stu-id="bde0c-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="bde0c-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="bde0c-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="bde0c-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="bde0c-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="bde0c-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="bde0c-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="bde0c-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="bde0c-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="bde0c-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="bde0c-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="bde0c-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="bde0c-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="bde0c-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="bde0c-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="bde0c-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="bde0c-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="bde0c-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="bde0c-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="bde0c-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="bde0c-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="bde0c-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="bde0c-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="bde0c-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="bde0c-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="bde0c-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="bde0c-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bde0c-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bde0c-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="bde0c-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="bde0c-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="bde0c-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="bde0c-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="bde0c-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="bde0c-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="bde0c-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="bde0c-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bde0c-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="bde0c-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="bde0c-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="bde0c-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="bde0c-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="bde0c-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="bde0c-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="bde0c-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="bde0c-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="bde0c-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="bde0c-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="bde0c-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="bde0c-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-265">Password</span><span class="sxs-lookup"><span data-stu-id="bde0c-265">Password</span></span></p></td>
<td><p><span data-ttu-id="bde0c-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="bde0c-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="bde0c-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="bde0c-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="bde0c-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="bde0c-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="bde0c-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="bde0c-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="bde0c-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="bde0c-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bde0c-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="bde0c-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="bde0c-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bde0c-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="bde0c-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="bde0c-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="bde0c-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="bde0c-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="bde0c-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="bde0c-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="bde0c-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="bde0c-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="bde0c-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="bde0c-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="bde0c-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="bde0c-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="bde0c-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="bde0c-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="bde0c-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="bde0c-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="bde0c-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="bde0c-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="bde0c-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="bde0c-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="bde0c-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="bde0c-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="bde0c-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="bde0c-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="bde0c-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="bde0c-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="bde0c-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="bde0c-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="bde0c-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="bde0c-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="bde0c-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="bde0c-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="bde0c-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="bde0c-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-303">User ID</span><span class="sxs-lookup"><span data-stu-id="bde0c-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="bde0c-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="bde0c-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-305">User Name</span><span class="sxs-lookup"><span data-stu-id="bde0c-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="bde0c-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="bde0c-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="bde0c-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="bde0c-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="bde0c-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="bde0c-309">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="bde0c-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="bde0c-310">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bde0c-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bde0c-311">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bde0c-312">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="bde0c-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="bde0c-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="bde0c-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bde0c-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bde0c-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="bde0c-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="bde0c-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="bde0c-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="bde0c-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="bde0c-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="bde0c-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="bde0c-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="bde0c-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bde0c-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="bde0c-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="bde0c-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="bde0c-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bde0c-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="bde0c-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="bde0c-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="bde0c-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="bde0c-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="bde0c-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="bde0c-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="bde0c-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bde0c-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="bde0c-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="bde0c-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="bde0c-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="bde0c-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bde0c-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="bde0c-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bde0c-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="bde0c-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="bde0c-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="bde0c-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="bde0c-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bde0c-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="bde0c-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bde0c-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bde0c-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bde0c-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bde0c-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="bde0c-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="bde0c-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="bde0c-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="bde0c-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="bde0c-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="bde0c-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bde0c-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="bde0c-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bde0c-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bde0c-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="bde0c-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bde0c-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bde0c-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="bde0c-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="bde0c-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="bde0c-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="bde0c-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="bde0c-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="bde0c-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="bde0c-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="bde0c-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="bde0c-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="bde0c-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bde0c-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="bde0c-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="bde0c-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bde0c-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="bde0c-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="bde0c-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="bde0c-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="bde0c-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="bde0c-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="bde0c-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="bde0c-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="bde0c-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="bde0c-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="bde0c-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="bde0c-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="bde0c-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="bde0c-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bde0c-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="bde0c-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="bde0c-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bde0c-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bde0c-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="bde0c-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="bde0c-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="bde0c-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="bde0c-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bde0c-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="bde0c-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="bde0c-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="bde0c-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="bde0c-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="bde0c-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="bde0c-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="bde0c-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bde0c-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="bde0c-444">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="bde0c-444">Command Dynamic Properties</span></span>

<span data-ttu-id="bde0c-445">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bde0c-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bde0c-446">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bde0c-447">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="bde0c-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="bde0c-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="bde0c-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="bde0c-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="bde0c-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="bde0c-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="bde0c-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bde0c-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bde0c-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="bde0c-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="bde0c-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="bde0c-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="bde0c-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="bde0c-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="bde0c-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="bde0c-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="bde0c-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bde0c-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="bde0c-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="bde0c-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="bde0c-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="bde0c-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="bde0c-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="bde0c-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="bde0c-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="bde0c-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="bde0c-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="bde0c-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="bde0c-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="bde0c-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="bde0c-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="bde0c-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="bde0c-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="bde0c-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="bde0c-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bde0c-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="bde0c-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="bde0c-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="bde0c-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="bde0c-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bde0c-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="bde0c-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bde0c-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="bde0c-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="bde0c-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="bde0c-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="bde0c-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="bde0c-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bde0c-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="bde0c-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bde0c-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bde0c-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bde0c-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bde0c-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="bde0c-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bde0c-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="bde0c-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="bde0c-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="bde0c-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="bde0c-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="bde0c-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="bde0c-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bde0c-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="bde0c-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bde0c-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bde0c-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="bde0c-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bde0c-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="bde0c-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bde0c-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bde0c-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="bde0c-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="bde0c-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="bde0c-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="bde0c-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="bde0c-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="bde0c-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="bde0c-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="bde0c-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="bde0c-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="bde0c-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="bde0c-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="bde0c-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="bde0c-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="bde0c-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="bde0c-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="bde0c-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="bde0c-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="bde0c-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bde0c-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bde0c-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="bde0c-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="bde0c-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bde0c-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="bde0c-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="bde0c-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bde0c-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="bde0c-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="bde0c-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="bde0c-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="bde0c-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="bde0c-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="bde0c-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="bde0c-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="bde0c-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="bde0c-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="bde0c-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="bde0c-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="bde0c-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="bde0c-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="bde0c-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="bde0c-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="bde0c-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bde0c-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="bde0c-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="bde0c-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bde0c-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bde0c-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="bde0c-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="bde0c-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="bde0c-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="bde0c-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="bde0c-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="bde0c-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="bde0c-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="bde0c-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bde0c-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="bde0c-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="bde0c-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="bde0c-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="bde0c-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="bde0c-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="bde0c-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="bde0c-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="bde0c-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bde0c-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="bde0c-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="bde0c-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="bde0c-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bde0c-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bde0c-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bde0c-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bde0c-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="bde0c-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="bde0c-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="bde0c-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bde0c-594">XSL</span><span class="sxs-lookup"><span data-stu-id="bde0c-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="bde0c-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="bde0c-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bde0c-596">Weitere Informationen zur Implementierung und zur Funktionsweise des Microsoft OLE DB-Anbieters für SQL Server finden Sie in der Dokumentation zu OLE DB-Anbieter für SQL Server im Abschnitt "OLE DB" im MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="bde0c-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

