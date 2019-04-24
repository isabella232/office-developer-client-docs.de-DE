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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288890"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="42ace-102">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="42ace-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="42ace-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42ace-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42ace-104">SQLOLEDB, der OLE DB-Anbieter für SQL Server, ermöglicht ADO den Zugriff auf Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="42ace-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="42ace-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="42ace-105">Connection String Parameters</span></span>

<span data-ttu-id="42ace-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider*-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="42ace-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="42ace-107">Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft gesetzt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="42ace-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="42ace-108">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="42ace-108">Typical Connection String</span></span>

<span data-ttu-id="42ace-109">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="42ace-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="42ace-110">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="42ace-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42ace-111">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="42ace-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="42ace-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42ace-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42ace-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="42ace-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="42ace-114">Gibt den OLE DB-Anbieter für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="42ace-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-115"><strong>Data Source</strong> oder <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="42ace-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42ace-116">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="42ace-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-117"><strong>Initial Catalog</strong> oder <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="42ace-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="42ace-118">Gibt den Namen einer Datenbank auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="42ace-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-119"><strong>User ID</strong> oder <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="42ace-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="42ace-120">Gibt den Benutzernamen (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="42ace-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-121"><strong>Password</strong> oder <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="42ace-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="42ace-122">Gibt das Benutzerkennwort (für die SQL Server-Authentifizierung) an.</span><span class="sxs-lookup"><span data-stu-id="42ace-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="42ace-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="42ace-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="42ace-p101">Der Anbieter unterstützt neben den von ADO definierten verschiedene anbieterspezifische Verbindungsparameter. Wie die ADO-Verbindungseigenschaften können diese anbieterspezifischen Eigenschaften über die [Properties](properties-collection-ado.md)-Auflistung eines [Connection](connection-object-ado.md)-Objekts oder als Teil der **ConnectionString**-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="42ace-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42ace-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ace-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="42ace-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42ace-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42ace-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="42ace-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="42ace-p102">Gibt den Benutzerauthentifizierungsmodus an. Dieser kann auf <strong>Yes</strong> oder <strong>No</strong> gesetzt werden. Der Standardwert ist <strong>No</strong>. Wenn diese Eigenschaft auf <strong>Yes</strong> gesetzt ist, verwendet SQLOLEDB den Microsoft Windows NT-Authentifizierungsmodus, um den Benutzerzugriff auf die in den Eigenschaftswerten <strong>Location</strong> und <a href="datasource-property-ado.md">Datasource</a> angegebene SQL Server-Datenbank zu autorisieren. Wenn diese Eigenschaft auf <strong>No</strong> gesetzt ist, verwendet SQLOLEDB den gemischten Modus, um den Benutzerzugriff auf die SQL Server-Datenbank zu autorisieren. Der Anmeldename und das Kennwort für SQL Server sind in den Eigenschaften <strong>User Id</strong> und <strong>Password</strong> angegeben.</span><span class="sxs-lookup"><span data-stu-id="42ace-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="42ace-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="42ace-p103">Gibt den Namen einer SQL Server-Sprache an. Erkennt die Sprache, die für die Auswahl und Formatierung von Systemmeldungen verwendet wird. Die Sprache muss auf dem Computer mit SQL Server installiert sein, da die Verbindung sonst nicht geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42ace-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="42ace-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="42ace-140">Gibt die Netzwerkadresse des Computers mit SQL Server an, die in der <strong>Location</strong>-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="42ace-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="42ace-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="42ace-142">Gibt den Namen der Netzwerkbibliothek (Dynamic Link Libraries) an, die für die Kommunikation mit dem Computer mit SQL Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42ace-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="42ace-143">Der Name darf weder den Pfad noch die Dateinamenerweiterung (DLL) enthalten.</span><span class="sxs-lookup"><span data-stu-id="42ace-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="42ace-144">Der Standardwert wird von der SQL Server-Clientkonfiguration bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="42ace-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="42ace-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="42ace-146">Gibt an, ob SQL Server temporäre gespeicherte Prozeduren erstellt, wenn Befehle (von der <strong>Prepared</strong>-Eigenschaft) vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="42ace-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="42ace-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="42ace-p105">Gibt an, ob OEM/ANSI-Zeichen konvertiert werden. Diese Eigenschaft kann auf <strong>True</strong> oder <strong>False</strong> festgelegt werden. Der Standardwert lautet <strong>True</strong>. Wenn diese Eigenschaft auf <strong>True</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen beim Empfangen oder Senden von Mehrbyte-Zeichenfolgen von oder an den Computer mit SQL Server. Wenn diese Eigenschaft auf <strong>False</strong> festgelegt ist, konvertiert SQLOLEDB OEM/ANSI-Zeichen in Daten mit Mehrbyte-Zeichenfolgen nicht.</span><span class="sxs-lookup"><span data-stu-id="42ace-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="42ace-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="42ace-p106">Gibt eine Netzwerkpaketgröße in Bytes an. Der Wert für die Eigenschaft der Paketgröße muss zwischen 512 und 32767 liegen. Der Standardwert für die Größe von SQLOLEDB-Netzwerkpaketen beträgt 4096.</span><span class="sxs-lookup"><span data-stu-id="42ace-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="42ace-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-158">Gibt den Namen der Clientanwendung an.</span><span class="sxs-lookup"><span data-stu-id="42ace-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="42ace-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="42ace-160">Eine Zeichenfolge, die die Arbeitsstation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42ace-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="42ace-161">Verwendung des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="42ace-161">Command Object Usage</span></span>

<span data-ttu-id="42ace-p107">SQLOLEDB akzeptiert eine Mischung aus ODBC, ANSI und SQL Server-spezifischem Transact-SQL als gültige Syntax. In der folgenden SQL-Anweisung wird beispielsweise eine ODBC SQL-Escapesequenz zum Angeben der LCASE-Zeichenfolgenfunktion verwendet:</span><span class="sxs-lookup"><span data-stu-id="42ace-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="42ace-p108">LCASE gibt eine Zeichenfolge zurück und konvertiert dabei alle Großbuchstaben in die entsprechenden Kleinbuchstaben. Die ANSI SQL-Zeichenfolgenfunktion LOWER führt denselben Vorgang aus. Die folgende SQL-Anweisung ist somit die Entsprechung der oben dargestellten ODBC-Anweisung in ANSI:</span><span class="sxs-lookup"><span data-stu-id="42ace-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="42ace-166">SQLOLEDB verarbeitet beide Formen der Anweisung, sofern diese als Text für einen Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="42ace-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="42ace-167">Gespeicherte Prozeduren</span><span class="sxs-lookup"><span data-stu-id="42ace-167">Stored Procedures</span></span>

<span data-ttu-id="42ace-p109">Verwenden Sie beim Ausführen einer gespeicherten SQL Server-Prozedur mit einem SQLOLEDB-Befehl die Escapesequenz des ODBC-Prozeduraufrufs im Befehlstext. SQLOLEDB verwendet dann den Remoteprozeduraufruf von SQL Server, um die Befehlsverarbeitung zu optimieren. So sollte beispielsweise die folgende ODBC SQL-Anweisung anstelle der Transact-SQL-Anweisung als Befehlstext verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="42ace-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="42ace-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="42ace-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="42ace-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="42ace-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="42ace-173">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="42ace-173">Recordset Behavior</span></span>

<span data-ttu-id="42ace-p110">SQLOLEDB kann keine SQL Server-Cursor verwenden, um die mehrfachen Ergebnisse, die von mehreren Befehlen generiert werden, zu unterstützen. Wenn ein Consumer eine Datensatzgruppe anfordert und die Unterstützung von SQL Server-Cursor erforderlich ist, tritt ein Fehler auf, sofern der verwendete Befehlstext mehrere Datensatzgruppen als Ergebnis generiert.</span><span class="sxs-lookup"><span data-stu-id="42ace-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="42ace-p111">SQL Server-Cursor unterstützen scrollfähige SQLOLEDB-Datensatzgruppen. SQL Server legt Einschränkungen für Cursor fest, die von Änderungen abhängen, die andere Benutzer an der Datenbank vornehmen. So können insbesondere die Zeilen in einigen Cursorn nicht sortiert werden, und beim Erstellen einer Datensatzgruppe mit einem Befehl, der eine ORDER BY-Klausel von SQL enthält, tritt möglicherweise ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="42ace-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="42ace-179">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42ace-179">Dynamic Properties</span></span>

<span data-ttu-id="42ace-180">Der Microsoft OLE DB-Anbieter für SQL Server fügt verschiedene Eigenschaften in die **Properties**-Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.</span><span class="sxs-lookup"><span data-stu-id="42ace-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="42ace-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span><span class="sxs-lookup"><span data-stu-id="42ace-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="42ace-185">Dynamische Eigenschaften von "Connection"</span><span class="sxs-lookup"><span data-stu-id="42ace-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="42ace-186">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Connection**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42ace-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42ace-187">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="42ace-188">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42ace-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="42ace-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="42ace-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="42ace-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="42ace-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="42ace-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="42ace-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="42ace-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="42ace-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="42ace-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="42ace-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="42ace-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="42ace-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="42ace-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="42ace-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="42ace-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="42ace-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="42ace-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="42ace-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="42ace-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="42ace-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="42ace-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="42ace-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="42ace-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="42ace-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="42ace-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="42ace-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="42ace-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="42ace-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="42ace-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="42ace-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="42ace-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="42ace-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="42ace-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="42ace-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="42ace-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="42ace-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="42ace-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="42ace-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="42ace-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="42ace-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="42ace-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="42ace-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="42ace-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="42ace-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="42ace-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="42ace-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="42ace-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="42ace-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="42ace-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="42ace-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="42ace-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="42ace-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="42ace-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="42ace-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="42ace-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="42ace-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="42ace-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="42ace-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="42ace-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="42ace-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="42ace-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="42ace-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="42ace-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="42ace-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="42ace-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="42ace-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="42ace-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="42ace-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="42ace-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="42ace-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="42ace-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="42ace-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="42ace-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="42ace-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="42ace-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="42ace-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="42ace-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="42ace-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="42ace-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="42ace-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="42ace-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="42ace-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="42ace-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="42ace-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="42ace-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="42ace-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="42ace-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="42ace-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="42ace-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="42ace-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="42ace-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="42ace-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="42ace-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="42ace-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="42ace-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="42ace-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="42ace-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="42ace-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="42ace-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="42ace-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="42ace-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="42ace-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="42ace-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="42ace-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="42ace-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="42ace-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-265">Password</span><span class="sxs-lookup"><span data-stu-id="42ace-265">Password</span></span></p></td>
<td><p><span data-ttu-id="42ace-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="42ace-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="42ace-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="42ace-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="42ace-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="42ace-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="42ace-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="42ace-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="42ace-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="42ace-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="42ace-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="42ace-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="42ace-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="42ace-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="42ace-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="42ace-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="42ace-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="42ace-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="42ace-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="42ace-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="42ace-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="42ace-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="42ace-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="42ace-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="42ace-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="42ace-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="42ace-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="42ace-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="42ace-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="42ace-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="42ace-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="42ace-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="42ace-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="42ace-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="42ace-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="42ace-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="42ace-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="42ace-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="42ace-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="42ace-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="42ace-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="42ace-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="42ace-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="42ace-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="42ace-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="42ace-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="42ace-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="42ace-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="42ace-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="42ace-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="42ace-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="42ace-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="42ace-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-303">User ID</span><span class="sxs-lookup"><span data-stu-id="42ace-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="42ace-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="42ace-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-305">User Name</span><span class="sxs-lookup"><span data-stu-id="42ace-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="42ace-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="42ace-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="42ace-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="42ace-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="42ace-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="42ace-309">Dynamische Eigenschaften von "Recordset"</span><span class="sxs-lookup"><span data-stu-id="42ace-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="42ace-310">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Recordset**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42ace-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42ace-311">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="42ace-312">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42ace-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="42ace-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="42ace-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="42ace-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="42ace-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="42ace-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="42ace-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="42ace-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="42ace-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="42ace-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="42ace-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="42ace-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="42ace-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="42ace-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="42ace-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="42ace-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="42ace-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="42ace-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="42ace-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="42ace-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="42ace-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="42ace-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="42ace-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="42ace-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="42ace-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="42ace-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="42ace-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="42ace-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="42ace-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="42ace-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="42ace-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="42ace-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="42ace-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="42ace-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="42ace-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="42ace-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="42ace-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="42ace-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="42ace-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="42ace-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="42ace-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="42ace-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="42ace-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="42ace-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="42ace-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="42ace-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="42ace-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="42ace-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="42ace-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="42ace-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="42ace-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="42ace-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="42ace-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="42ace-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="42ace-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="42ace-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="42ace-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="42ace-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="42ace-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="42ace-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="42ace-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="42ace-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="42ace-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="42ace-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="42ace-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="42ace-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="42ace-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="42ace-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="42ace-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="42ace-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="42ace-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="42ace-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="42ace-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="42ace-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="42ace-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="42ace-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="42ace-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="42ace-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="42ace-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="42ace-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="42ace-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="42ace-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="42ace-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="42ace-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="42ace-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="42ace-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="42ace-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="42ace-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="42ace-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="42ace-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="42ace-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="42ace-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="42ace-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="42ace-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="42ace-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="42ace-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="42ace-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="42ace-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="42ace-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="42ace-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="42ace-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="42ace-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="42ace-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="42ace-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="42ace-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="42ace-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="42ace-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="42ace-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="42ace-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="42ace-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="42ace-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="42ace-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="42ace-444">Dynamische Eigenschaften von "Command"</span><span class="sxs-lookup"><span data-stu-id="42ace-444">Command Dynamic Properties</span></span>

<span data-ttu-id="42ace-445">Die folgenden Eigenschaften werden der **Properties**-Auflistung des **Command**-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42ace-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42ace-446">ADO-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="42ace-447">OLE DB-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="42ace-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42ace-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="42ace-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="42ace-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="42ace-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="42ace-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="42ace-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="42ace-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="42ace-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="42ace-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="42ace-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="42ace-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="42ace-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="42ace-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="42ace-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="42ace-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="42ace-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="42ace-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="42ace-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="42ace-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="42ace-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="42ace-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="42ace-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="42ace-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="42ace-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="42ace-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="42ace-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="42ace-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="42ace-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="42ace-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="42ace-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="42ace-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="42ace-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="42ace-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="42ace-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="42ace-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="42ace-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="42ace-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="42ace-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="42ace-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="42ace-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="42ace-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="42ace-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="42ace-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="42ace-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="42ace-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="42ace-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="42ace-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="42ace-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="42ace-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="42ace-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="42ace-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="42ace-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="42ace-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="42ace-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="42ace-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="42ace-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="42ace-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="42ace-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="42ace-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="42ace-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="42ace-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="42ace-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="42ace-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="42ace-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="42ace-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="42ace-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="42ace-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="42ace-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="42ace-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="42ace-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="42ace-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="42ace-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="42ace-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="42ace-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="42ace-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="42ace-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="42ace-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="42ace-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="42ace-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="42ace-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="42ace-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="42ace-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="42ace-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="42ace-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="42ace-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="42ace-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="42ace-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="42ace-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="42ace-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="42ace-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="42ace-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="42ace-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="42ace-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="42ace-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="42ace-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="42ace-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="42ace-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="42ace-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="42ace-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="42ace-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="42ace-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="42ace-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="42ace-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="42ace-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="42ace-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="42ace-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="42ace-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="42ace-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="42ace-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="42ace-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="42ace-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="42ace-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="42ace-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="42ace-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="42ace-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="42ace-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="42ace-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="42ace-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="42ace-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="42ace-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="42ace-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="42ace-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="42ace-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="42ace-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="42ace-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="42ace-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="42ace-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="42ace-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="42ace-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="42ace-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="42ace-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="42ace-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="42ace-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="42ace-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="42ace-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="42ace-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="42ace-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="42ace-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="42ace-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="42ace-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="42ace-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="42ace-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="42ace-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="42ace-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="42ace-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="42ace-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="42ace-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="42ace-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="42ace-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="42ace-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42ace-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="42ace-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="42ace-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="42ace-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42ace-594">XSL</span><span class="sxs-lookup"><span data-stu-id="42ace-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="42ace-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="42ace-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42ace-596">Weitere Informationen zur Implementierung und zur Funktionsweise des Microsoft OLE DB-Anbieters für SQL Server finden Sie in der Dokumentation zu OLE DB-Anbieter für SQL Server im Abschnitt "OLE DB" im MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="42ace-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

