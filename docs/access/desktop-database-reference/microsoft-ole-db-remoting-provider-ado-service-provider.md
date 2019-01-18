---
title: Microsoft OLE DB-Anbieter für Remoting (ADO-Dienstanbieter)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54ea659aa5392dd4404ffb591eba06f1f9c2910b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701900"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="181b3-102">Microsoft OLE DB-Anbieter für Remoting (ADO-Dienstanbieter)</span><span class="sxs-lookup"><span data-stu-id="181b3-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="181b3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="181b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="181b3-p101">Mithilfe des Microsoft OLE DB-Anbieter für Remoting kann ein lokaler Benutzer auf einem Clientcomputer Datenanbieter auf einem Remotecomputer aufrufen. Geben Sie die Parameter des Datenanbieters für den Remotecomputer so an, als wären Sie ein lokaler Benutzer am Remotecomputer. Geben Sie anschließend die Parameter an, die vom Anbieter für Remoting für den Zugriff auf den Remotecomputer verwendet werden. So haben Sie auf den Remotecomputer Zugriff, als wären Sie ein lokaler Benutzer.</span><span class="sxs-lookup"><span data-stu-id="181b3-p101">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine. Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine. Then specify the parameters used by the Remoting Provider to access the remote machine. The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="181b3-108">Schlüsselwort für den Anbieter</span><span class="sxs-lookup"><span data-stu-id="181b3-108">Provider Keyword</span></span>

<span data-ttu-id="181b3-p102">Um den OLE DB-Anbieter für Remoting aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein. (Beachten Sie das Leerzeichen im Namen des Anbieters.)</span><span class="sxs-lookup"><span data-stu-id="181b3-p102">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string. (Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="181b3-111">Zusätzliche Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="181b3-111">Additional Keywords</span></span>

<span data-ttu-id="181b3-112">Beim Aufrufen dieses Dienstanbieters sind die folgenden zusätzlichen Schlüsselwörter relevant.</span><span class="sxs-lookup"><span data-stu-id="181b3-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="181b3-113">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="181b3-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="181b3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="181b3-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="181b3-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-116">Gibt den Namen der Remotedatenquelle an.</span><span class="sxs-lookup"><span data-stu-id="181b3-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="181b3-117">Es wird an den OLE DB-Anbieter für Remoting zur Verarbeitung übergeben.</span><span class="sxs-lookup"><span data-stu-id="181b3-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="181b3-118">Dieses Schlüsselwort entspricht der <a href="connect-property-rds.md">Connect</a>-Eigenschaft des <a href="datacontrol-object-rds.md">RDS.DataControl</a>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="181b3-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="181b3-119">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="181b3-119">Dynamic Properties</span></span>

<span data-ttu-id="181b3-120">Beim Aufrufen dieses Dienstanbieters werden der [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts die folgenden dynamischen Eigenschaften hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="181b3-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="181b3-121">Name der dynamischen Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="181b3-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="181b3-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="181b3-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="181b3-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-124">Gibt den DataFactory-Modus.</span><span class="sxs-lookup"><span data-stu-id="181b3-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="181b3-125">Eine Zeichenfolge, die die gewünschte Version des <a href="datafactory-object-rdsserver.md">DataFactory</a> -Objekts gibt an, auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="181b3-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="181b3-126">Legen Sie diese Eigenschaft vor dem Öffnen einer Verbindungs zum Anfordern einer bestimmten Version von <strong>DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="181b3-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="181b3-127">Wenn die angeforderte Version nicht verfügbar ist, wird versucht werden, verwenden Sie die vorhergehende Version.</span><span class="sxs-lookup"><span data-stu-id="181b3-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="181b3-128">Wenn keine vorhergehende Version vorhanden ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="181b3-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="181b3-129">Wenn <strong>DFMode</strong> kleiner als die verfügbare Version ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="181b3-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="181b3-130">Diese Eigenschaft ist schreibgeschützt, nachdem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="181b3-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="181b3-131">Kann einen der folgenden gültigen Werte vom Typ String annehmen:</span><span class="sxs-lookup"><span data-stu-id="181b3-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="181b3-132">&quot;25&quot; – Version 2.5 (Default)</span><span class="sxs-lookup"><span data-stu-id="181b3-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="181b3-133">&quot;21&quot; – Version 2.1</span><span class="sxs-lookup"><span data-stu-id="181b3-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="181b3-134">&quot;20&quot; – Version 2.0</span><span class="sxs-lookup"><span data-stu-id="181b3-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="181b3-135">&quot;15&quot; – Version 1.5</span><span class="sxs-lookup"><span data-stu-id="181b3-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181b3-136"><strong>Command Properties</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-p105">Gibt Werte an, die der Zeichenfolge der Command-Eigenschaften (Rowset) hinzugefügt werden, die vom Microsoft OLE DB-Anbieter für Remoting an den Server gesendet werden. Der Standardwert für diese Zeichenfolge lautet vt_empty.</span><span class="sxs-lookup"><span data-stu-id="181b3-p105">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider. The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181b3-139"><strong>Current DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-140">Gibt die aktuelle Versionsnummer des <strong>DataFactory</strong> auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="181b3-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="181b3-141">Überprüfen Sie diese Eigenschaft, um festzustellen, ob die in der Eigenschaft <strong>DFMode</strong> angeforderte Version berücksichtigt wurde.</span><span class="sxs-lookup"><span data-stu-id="181b3-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="181b3-142">Kann einen der folgenden gültigen Werte vom Typ Long integer annehmen:</span><span class="sxs-lookup"><span data-stu-id="181b3-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="181b3-143">25 – Version 2.5 (Default)</span><span class="sxs-lookup"><span data-stu-id="181b3-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="181b3-144">21 – Version 2.1</span><span class="sxs-lookup"><span data-stu-id="181b3-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="181b3-145">20 – Version 2.0</span><span class="sxs-lookup"><span data-stu-id="181b3-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="181b3-146">15 – Version 1.5</span><span class="sxs-lookup"><span data-stu-id="181b3-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="181b3-147">Hinzufügen von &quot;DFMode = 20; &quot; für Ihre Verbindung bei Verwendung des Providers <strong>MSRemote</strong> Zeichenfolge beim Aktualisieren von Daten die Leistung Ihres Servers verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="181b3-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="181b3-148">Bei dieser Einstellung verwendet das <strong>RDSServer.DataFactory</strong> -Objekt auf dem Server einen weniger ressourcenintensiven Modus.</span><span class="sxs-lookup"><span data-stu-id="181b3-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="181b3-149">In dieser Konfiguration sind die folgenden Features jedoch nicht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="181b3-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="181b3-150">Verwenden parametrisierter Abfragen.</span><span class="sxs-lookup"><span data-stu-id="181b3-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="181b3-151">Abrufen von Parameter- oder Spalteninformationen vor dem Aufrufen der <strong>Execute</strong> -Methode.</span><span class="sxs-lookup"><span data-stu-id="181b3-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="181b3-152">Festlegen von <strong>Transact Updates</strong> auf <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="181b3-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="181b3-153">Abrufen von Zeilenstatus.</span><span class="sxs-lookup"><span data-stu-id="181b3-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="181b3-154">Aufrufen der <strong>Resync</strong>-Methode.</span><span class="sxs-lookup"><span data-stu-id="181b3-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="181b3-155">Aktualisieren (explizit oder automatisch) mithilfe der <strong>Update Resync</strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="181b3-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="181b3-156">Festlegen der Eigenschaften von <strong>Command</strong> oder <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="181b3-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="181b3-157">Verwenden von <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="181b3-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181b3-158"><strong>Ereignishandler</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-159">Gibt den Namen eines serverseitigen Anpassungsprogramms (oder Handler), die die Funktionalität des <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>und keine Parameter vom Handler verwendeten<em>,</em> alle durch Kommas getrennt erweitert (&quot;,&quot;).</span><span class="sxs-lookup"><span data-stu-id="181b3-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="181b3-160">Ein <strong>String</strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="181b3-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181b3-161"><strong>Internet Timeout</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-p109">Gibt die Zeitdauer in Millisekunden an, die verstreicht, bis eine Anforderung vom und zum Server gelangt. (Der Standardwert beträgt 5 Minuten).</span><span class="sxs-lookup"><span data-stu-id="181b3-p109">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server. (The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181b3-164"><strong>Remote Provider</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-165">Gibt den Namen des Datenproviders an, der auf dem Remoteserver verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="181b3-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181b3-166"><strong>Remote Server</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-p110">Gibt den Servernamen und das Kommunikationsprotokoll an, das von dieser Verbindung verwendet werden soll. Diese Eigenschaft entspricht der <a href="server-property-rds.md">Server</a>-Eigenschaft des <a href="datacontrol-object-rds.md">RDS.DataControl</a>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="181b3-p110">Indicates the server name and communication protocol to be used by this connection. This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181b3-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="181b3-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="181b3-p111">Wenn diese Eigenschaft auf True gesetzt ist, gibt dieser Wert an, dass beim Ausführen von UpdateBatch auf dem Server die Ausführung innerhalb einer Transaktion erfolgt. Der Standardwert für diese boolesche dynamische Eigenschaft ist False.</span><span class="sxs-lookup"><span data-stu-id="181b3-p111">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction. The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="181b3-p112">Sie können auch beschreibbare dynamische Eigenschaften festlegen, indem Sie die zugehörigen Namen in der Verbindungszeichenfolge als Schlüsselwörter angeben. Legen Sie beispielsweise die dynamische Eigenschaft **Internet Timeout** auf fünf Sekunden fest, indem Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="181b3-p112">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="181b3-p113">Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die **Properties** -Eigenschaft angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft **Internet Timeout** ab, und drucken Sie diesen. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="181b3-p113">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property. For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="181b3-176">Hinweise</span><span class="sxs-lookup"><span data-stu-id="181b3-176">Remarks</span></span>

<span data-ttu-id="181b3-177">In ADO 2.0 konnte der OLE DB-Anbieter für Remoting nur in der *ActiveConnection* -Parameter der **Open** -Methode des [Recordset](recordset-object-ado.md) -Objekts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="181b3-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="181b3-178">ADO 2.1 ab, kann der Anbieter auch in der *ConnectionString* -Parameter der **Open** -Methode des [Connection](connection-object-ado.md) -Objekts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="181b3-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="181b3-179">Die Entsprechung der **SQL**-Eigenschaft des [RDS.DataControl](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) -Objekts ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="181b3-179">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available.</span></span> <span data-ttu-id="181b3-180">Stattdessen wird das [Recordset](recordset-object-ado.md) -Objekt **Open** *Source* -Argument-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="181b3-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="181b3-181">Wenn Sie "...;Remote Provider=MS Remote;..." angeben, wird ein vierstufiges Szenario erstellt. Szenarien mit mehr als drei Stufen wurden noch nicht getestet und sollten nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="181b3-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="181b3-182">Beispiel</span><span class="sxs-lookup"><span data-stu-id="181b3-182">Example</span></span>

<span data-ttu-id="181b3-p116">Mit diesem Beispiel wird die **Authors**-Tabelle in der **Pubs**-Datenbank auf dem Server *Server* abgefragt. Die Namen der Remotedatenquelle und des Remoteservers werden in der [Open](open-method-ado-connection.md)-Methode des [Connection](connection-object-ado.md)-Objekts bereitgestellt, und die SQL-Abfrage wird in der [Open-Methode](open-method-ado-recordset.md) des [Recordset](recordset-object-ado.md)-Objekts angegeben. Ein **Recordset**-Objekt wird zurückgegeben, bearbeitet und verwendet, um die Datenquelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="181b3-p116">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*. The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method. A **Recordset** object is returned, edited, and used to update the data source.</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

