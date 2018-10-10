---
title: Microsoft OLE DB-Anbieter für SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f999f9268511fd23f1fc6a20c8459d11345ceb4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473665"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="fcfc5-102">Microsoft OLE DB-Anbieter für SQL Server</span><span class="sxs-lookup"><span data-stu-id="fcfc5-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="fcfc5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcfc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fcfc5-104">SQLOLEDB, der OLE DB-Anbieter für SQL Server, ermöglicht ADO den Zugriff auf Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="fcfc5-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="fcfc5-105">Connection String Parameters</span></span>

<span data-ttu-id="fcfc5-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="fcfc5-107">Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft gesetzt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="fcfc5-108">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fcfc5-108">Typical Connection String</span></span>

<span data-ttu-id="fcfc5-109">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="fcfc5-110">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfc5-111">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="fcfc5-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="fcfc5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcfc5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="fcfc5-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfc5-114">Gibt den OLE DB-Anbieter für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-115"><strong>Data Source</strong> oder <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fcfc5-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfc5-116">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-117"><strong>Initial Catalog</strong> oder <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="fcfc5-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfc5-118">Gibt den Namen einer Datenbank auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-119"><strong>User ID</strong> oder <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="fcfc5-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfc5-120">Gibt den Benutzernamen (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-121"><strong>Password</strong> oder <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="fcfc5-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfc5-122">Gibt das Benutzerkennwort (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="fcfc5-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="fcfc5-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="fcfc5-p101">Der Anbieter unterstützt neben den von ADO definierten verschiedene anbieterspezifische Verbindungsparameter. Wie die ADO-Verbindungseigenschaften können diese anbieterspezifischen Eigenschaften über die [Properties](properties-collection-ado.md)-Auflistung eines [Connection](connection-object-ado.md)-Objekts oder als Teil der **ConnectionString** -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfc5-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcfc5-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="fcfc5-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcfc5-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="fcfc5-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-p102">Gibt den Benutzerauthentifizierungsmodus an. Dieser kann auf <strong>Yes</strong> oder <strong>No</strong> gesetzt werden. Der Standardwert ist <strong>No</strong>. Wenn diese Eigenschaft auf <strong>Yes</strong> gesetzt ist, verwendet SQLOLEDB den Microsoft Windows NT-Authentifizierungsmodus, um den Benutzerzugriff auf die in den Eigenschaftswerten <strong>Location</strong> und <a href="datasource-property-ado.md">Datasource</a> angegebene SQL Server-Datenbank zu autorisieren. Wenn diese Eigenschaft auf <strong>No</strong> gesetzt ist, verwendet SQLOLEDB den gemischten Modus, um den Benutzerzugriff auf die SQL Server-Datenbank zu autorisieren. Der Anmeldename und das Kennwort für SQL Server sind in den Eigenschaften <strong>User Id</strong> und <strong>Password</strong> angegeben.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="fcfc5-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-p103">Gibt den Namen einer SQL Server-Sprache an. Erkennt die Sprache, die für die Auswahl und Formatierung von Systemmeldungen verwendet wird. Die Sprache muss auf dem Computer mit SQL Server installiert sein, da die Verbindung sonst nicht geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="fcfc5-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-140">Gibt die Netzwerkadresse des Computers mit SQL Server an, die in der <strong>Location</strong>-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="fcfc5-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-142">Gibt den Namen der Netzwerkbibliothek (Dynamic Link Libraries) verwendet, um eine Kommunikation mit dem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="fcfc5-143">Der Name darf nicht den Pfad oder der DLL-Erweiterung enthalten.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="fcfc5-144">Der Standardwert ist von der SQL Server-Clientkonfigurationsprogramm bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="fcfc5-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-146">Gibt an, ob SQL Server temporäre gespeicherte Prozeduren erstellt, wenn Befehle (von der <strong>Prepared</strong>-Eigenschaft) vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-p105">Gibt an, ob OEM/ANSI-Zeichen konvertiert werden. Diese Eigenschaft kann auf <strong>True</strong> oder <strong>False</strong> festgelegt werden. Der Standardwert lautet <strong>True</strong>. Wenn diese Eigenschaft auf <strong>True</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen beim Empfangen oder Senden von Mehrbyte-Zeichenfolgen von oder an den Computer mit SQL Server. Wenn diese Eigenschaft auf <strong>False</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen in Daten mit Mehrbyte-Zeichenfolgen nicht.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="fcfc5-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-p106">Gibt eine Netzwerkpaketgröße in Bytes an. Der Wert für die Eigenschaft der Paketgröße muss zwischen 512 und 32767 liegen. Der Standardwert für die Größe von SQLOLEDB-Netzwerkpaketen beträgt 4096.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-158">Gibt den Namen der Clientanwendung an.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="fcfc5-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-160">Eine Zeichenfolge, die die Arbeitsstation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="fcfc5-161">Verwendung des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="fcfc5-161">Command Object Usage</span></span>

<span data-ttu-id="fcfc5-p107">SQLOLEDB akzeptiert eine Mischung aus ODBC, ANSI und SQL Server-spezifischem Transact-SQL als gültige Syntax. In der folgenden SQL-Anweisung wird beispielsweise eine ODBC SQL-Escapesequenz zum Angeben der LCASE-Zeichenfolgenfunktion verwendet:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="fcfc5-p108">LCASE gibt eine Zeichenfolge zurück und konvertiert dabei alle Großbuchstaben in die entsprechenden Kleinbuchstaben. Die ANSI SQL-Zeichenfolgenfunktion LOWER führt denselben Vorgang aus. Die folgende SQL-Anweisung ist somit die Entsprechung der oben dargestellten ODBC-Anweisung in ANSI:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="fcfc5-166">SQLOLEDB verarbeitet beide Formen der Anweisung, sofern diese als Text für einen Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="fcfc5-167">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="fcfc5-167">Stored Procedures</span></span>

<span data-ttu-id="fcfc5-p109">Verwenden Sie beim Ausführen einer gespeicherten SQL Server-Prozedur mit einem SQLOLEDB-Befehl die Escapesequenz des ODBC-Prozeduraufrufs im Befehlstext. SQLOLEDB verwendet dann den Remoteprozeduraufruf von SQL Server, um die Befehlsverarbeitung zu optimieren. So sollte beispielsweise die folgende ODBC SQL-Anweisung anstelle der Transact-SQL-Anweisung als Befehlstext verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="fcfc5-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="fcfc5-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="fcfc5-173">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="fcfc5-173">Recordset Behavior</span></span>

<span data-ttu-id="fcfc5-p110">SQLOLEDB kann keine SQL Server-Cursor verwenden, um die mehrfachen Ergebnisse, die von mehreren Befehlen generiert werden, zu unterstützen. Wenn ein Consumer eine Datensatzgruppe anfordert und die Unterstützung von SQL Server-Cursor erforderlich ist, tritt ein Fehler auf, sofern der verwendete Befehlstext mehrere Datensatzgruppen als Ergebnis generiert.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="fcfc5-p111">SQL Server-Cursor unterstützen scrollfähige SQLOLEDB-Datensatzgruppen. SQL Server legt Einschränkungen für Cursor fest, die von Änderungen abhängen, die andere Benutzer an der Datenbank vornehmen. So können insbesondere die Zeilen in einigen Cursorn nicht sortiert werden, und beim Erstellen einer Datensatzgruppe mit einem Befehl, der eine ORDER BY-Klausel von SQL enthält, tritt möglicherweise ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="fcfc5-179">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fcfc5-179">Dynamic Properties</span></span>

<span data-ttu-id="fcfc5-180">Der Microsoft OLE DB-Anbieter für SQL Server fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="fcfc5-p112">Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties (in Englisch).</span><span class="sxs-lookup"><span data-stu-id="fcfc5-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="fcfc5-185">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="fcfc5-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="fcfc5-186">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfc5-187">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fcfc5-188">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="fcfc5-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="fcfc5-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="fcfc5-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="fcfc5-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="fcfc5-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="fcfc5-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="fcfc5-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="fcfc5-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="fcfc5-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="fcfc5-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="fcfc5-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="fcfc5-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="fcfc5-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="fcfc5-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="fcfc5-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="fcfc5-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="fcfc5-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="fcfc5-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="fcfc5-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="fcfc5-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="fcfc5-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="fcfc5-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-226">NULL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="fcfc5-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="fcfc5-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="fcfc5-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="fcfc5-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="fcfc5-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="fcfc5-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="fcfc5-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="fcfc5-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="fcfc5-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="fcfc5-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="fcfc5-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fcfc5-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="fcfc5-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="fcfc5-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="fcfc5-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="fcfc5-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fcfc5-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="fcfc5-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="fcfc5-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="fcfc5-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="fcfc5-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="fcfc5-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-265">Password</span><span class="sxs-lookup"><span data-stu-id="fcfc5-265">Password</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="fcfc5-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="fcfc5-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="fcfc5-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="fcfc5-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="fcfc5-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fcfc5-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="fcfc5-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="fcfc5-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="fcfc5-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="fcfc5-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="fcfc5-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="fcfc5-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="fcfc5-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="fcfc5-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="fcfc5-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="fcfc5-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="fcfc5-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="fcfc5-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="fcfc5-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="fcfc5-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="fcfc5-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="fcfc5-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="fcfc5-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="fcfc5-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="fcfc5-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-303">User ID</span><span class="sxs-lookup"><span data-stu-id="fcfc5-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="fcfc5-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-305">User Name</span><span class="sxs-lookup"><span data-stu-id="fcfc5-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="fcfc5-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="fcfc5-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="fcfc5-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="fcfc5-309">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="fcfc5-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="fcfc5-310">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfc5-311">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fcfc5-312">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="fcfc5-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="fcfc5-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fcfc5-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="fcfc5-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="fcfc5-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="fcfc5-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="fcfc5-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="fcfc5-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="fcfc5-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="fcfc5-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="fcfc5-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="fcfc5-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fcfc5-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fcfc5-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="fcfc5-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="fcfc5-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fcfc5-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fcfc5-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="fcfc5-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fcfc5-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fcfc5-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fcfc5-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fcfc5-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="fcfc5-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="fcfc5-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="fcfc5-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="fcfc5-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="fcfc5-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="fcfc5-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="fcfc5-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="fcfc5-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="fcfc5-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="fcfc5-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="fcfc5-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="fcfc5-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="fcfc5-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="fcfc5-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="fcfc5-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="fcfc5-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="fcfc5-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="fcfc5-444">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="fcfc5-444">Command Dynamic Properties</span></span>

<span data-ttu-id="fcfc5-445">Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfc5-446">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="fcfc5-447">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fcfc5-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="fcfc5-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="fcfc5-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="fcfc5-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="fcfc5-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="fcfc5-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="fcfc5-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="fcfc5-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="fcfc5-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="fcfc5-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="fcfc5-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="fcfc5-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="fcfc5-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="fcfc5-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="fcfc5-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="fcfc5-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="fcfc5-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="fcfc5-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fcfc5-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="fcfc5-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="fcfc5-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="fcfc5-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="fcfc5-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fcfc5-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="fcfc5-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="fcfc5-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="fcfc5-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fcfc5-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="fcfc5-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="fcfc5-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fcfc5-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="fcfc5-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="fcfc5-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="fcfc5-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="fcfc5-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="fcfc5-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="fcfc5-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="fcfc5-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="fcfc5-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="fcfc5-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="fcfc5-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="fcfc5-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="fcfc5-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="fcfc5-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="fcfc5-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="fcfc5-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="fcfc5-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="fcfc5-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="fcfc5-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="fcfc5-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="fcfc5-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="fcfc5-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="fcfc5-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="fcfc5-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="fcfc5-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="fcfc5-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="fcfc5-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="fcfc5-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="fcfc5-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="fcfc5-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="fcfc5-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="fcfc5-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="fcfc5-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="fcfc5-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="fcfc5-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="fcfc5-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfc5-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="fcfc5-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="fcfc5-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfc5-594">XSL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="fcfc5-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="fcfc5-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fcfc5-596">Weitere Informationen zur Implementierung und zur Funktionsweise des Microsoft OLE DB-Anbieters für SQL Server finden Sie in der Dokumentation zu OLE DB-Anbieter für SQL Server im Abschnitt "OLE DB" im MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="fcfc5-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

