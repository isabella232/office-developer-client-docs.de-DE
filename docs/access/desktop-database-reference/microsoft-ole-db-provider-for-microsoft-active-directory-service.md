---
title: Microsoft OLE DB-Anbieter für Microsoft Active Directory-Dienst
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1555883ef8305225d6ddd1969d98de082288a6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887537"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="940b1-102">Microsoft OLE DB-Anbieter für Microsoft Active Directory-Dienst</span><span class="sxs-lookup"><span data-stu-id="940b1-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="940b1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="940b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="940b1-p101">Mithilfe des Microsoft ADSI-Anbieters (Active Directory Service Interfaces) kann ADO über ADSI eine Verbindung mit heterogenen Verzeichnisdiensten herstellen. Dadurch erlangen ADO-Anwendungen schreibgeschützten Zugriff auf die Verzeichnisdienste von Microsoft Windows NT 4.0 und Microsoft Windows 2000 sowie auf sämtliche LDAP-kompatible Verzeichnisdienste und Novell Directory Services. ADSI selbst basiert auf einem Anbietermodell. Wenn also ein neuer Anbieter Zugriff auf ein anderes Verzeichnis gewährt, kann die ADO-Anwendung problemlos auf dieses Verzeichnis zugreifen. Der ADSI-Anbieter ist ein Freethreadanbieter, der Unicode verwendet.</span><span class="sxs-lookup"><span data-stu-id="940b1-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="940b1-108">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="940b1-108">Connection String Parameters</span></span>

<span data-ttu-id="940b1-109">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="940b1-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="940b1-110">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="940b1-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="940b1-111">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="940b1-111">Typical Connection String</span></span>

<span data-ttu-id="940b1-112">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="940b1-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="940b1-113">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="940b1-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="940b1-114">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="940b1-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="940b1-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="940b1-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940b1-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="940b1-117">Gibt den OLE DB-Anbieter für Microsoft Active Directory-Dienst an.</span><span class="sxs-lookup"><span data-stu-id="940b1-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="940b1-p102">Gibt den Benutzernamen an. Wenn dieses Schlüsselwort nicht angegeben ist, werden die aktuellen Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="940b1-p102">Specifies the user name. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="940b1-p103">Gibt das Benutzerkennwort an. Wenn dieses Schlüsselwort nicht angegeben ist, werden die aktuellen Anmeldeinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="940b1-p103">Specifies the user password. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="940b1-124">**Befehlstext**</span><span class="sxs-lookup"><span data-stu-id="940b1-124">**Command Text**</span></span>

<span data-ttu-id="940b1-125">Eine vierteilige Befehlstextzeichenfolge wird durch den Anbieter in der folgenden Syntax erkannt:</span><span class="sxs-lookup"><span data-stu-id="940b1-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="940b1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="940b1-126">Value</span></span></p></th>
<th><p><span data-ttu-id="940b1-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="940b1-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940b1-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="940b1-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="940b1-129">Gibt das <strong>ADsPath</strong>-Objekt an, von dem aus die Suche gestartet werden soll (d. h. den Stamm der Suche).</span><span class="sxs-lookup"><span data-stu-id="940b1-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="940b1-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="940b1-131">Gibt den Suchfilter im Format RFC 1960 an.</span><span class="sxs-lookup"><span data-stu-id="940b1-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-132"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="940b1-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="940b1-133">Gibt eine Liste mit durch Komma getrennten Attributen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="940b1-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="940b1-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="940b1-135">Optional.</span><span class="sxs-lookup"><span data-stu-id="940b1-135">Optional.</span></span> <span data-ttu-id="940b1-136">Eine <strong>Zeichenfolge</strong> , die den Bereich der Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="940b1-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="940b1-137">Kann eine der folgenden sein: Basis – nur das Basisobjekt (Stamm der Suche).</span><span class="sxs-lookup"><span data-stu-id="940b1-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="940b1-138">Ebene – Sucht nur eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="940b1-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="940b1-139">Unterstruktur – Suchen Sie die gesamte Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="940b1-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="940b1-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="940b1-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="940b1-p105">Der Anbieter unterstützt auch SQL SELECT als Befehlstext. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="940b1-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="940b1-p106">Der Anbieter akzeptiert weder Aufrufe gespeicherter Prozeduren noch einfache Tabellennamen (die [CommandType](commandtype-property-ado.md)-Eigenschaft lautet beispielsweise immer **adCmdText**). Eine ausführlichere Beschreibung der Befehlstextelemente finden Sie in der Dokumentation zu ADSI (Active Directory Service Interfaces).</span><span class="sxs-lookup"><span data-stu-id="940b1-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="940b1-145">Recordset-Verhalten</span><span class="sxs-lookup"><span data-stu-id="940b1-145">Recordset Behavior</span></span>

<span data-ttu-id="940b1-146">In den folgenden Tabellen sind die für ein [Recordset](recordset-object-ado.md)-Objekt verfügbaren Features aufgeführt, das mit diesem Anbieter geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="940b1-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="940b1-147">Nur der statische Cursortyp (**AdOpenStatic**) zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="940b1-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="940b1-148">Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die [Properties](properties-collection-ado.md) -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="940b1-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="940b1-149">Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="940b1-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="940b1-150">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="940b1-150">Property</span></span></p></th>
<th><p><span data-ttu-id="940b1-151">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="940b1-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940b1-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="940b1-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-153">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="940b1-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-155">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="940b1-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-157">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="940b1-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-159">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="940b1-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-161">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="940b1-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-163">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="940b1-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-165">immer <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="940b1-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-167">immer <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="940b1-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-169">immer <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="940b1-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="940b1-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-171">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="940b1-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-173">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="940b1-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-175">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="940b1-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-177">Nicht verf?gbar</span><span class="sxs-lookup"><span data-stu-id="940b1-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="940b1-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-179">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="940b1-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-181">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="940b1-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-183">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="940b1-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-185">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="940b1-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-187">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="940b1-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="940b1-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-189">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-190"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="940b1-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-191">nur Lesen</span><span class="sxs-lookup"><span data-stu-id="940b1-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="940b1-192">Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="940b1-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="940b1-193">Methode</span><span class="sxs-lookup"><span data-stu-id="940b1-193">Method</span></span></p></th>
<th><p><span data-ttu-id="940b1-194">Verfügbar?</span><span class="sxs-lookup"><span data-stu-id="940b1-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940b1-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="940b1-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-196">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="940b1-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-198">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="940b1-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-200">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="940b1-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-202">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="940b1-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-204">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="940b1-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-206">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="940b1-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-208">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="940b1-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-210">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="940b1-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-212">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="940b1-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-214">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="940b1-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-216">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="940b1-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-218">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="940b1-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-220">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="940b1-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-222">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="940b1-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-224">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="940b1-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-226">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="940b1-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-228">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-229"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="940b1-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-230">Ja</span><span class="sxs-lookup"><span data-stu-id="940b1-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b1-231"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="940b1-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-232">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b1-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="940b1-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="940b1-234">Nein</span><span class="sxs-lookup"><span data-stu-id="940b1-234">No</span></span></p></td>
</tr>
</tbody>
</table>

