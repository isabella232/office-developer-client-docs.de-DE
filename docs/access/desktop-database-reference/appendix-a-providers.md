---
title: 'Anhang A: Anbieter'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbd9536edd15f923af85f2fadad8b696077af4a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475172"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="a0b58-102">Anhang A: Anbieter</span><span class="sxs-lookup"><span data-stu-id="a0b58-102">Appendix A: Providers</span></span>


<span data-ttu-id="a0b58-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0b58-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a0b58-p101">In diesem Abschnitt werden drei Arten von Anbietern beschrieben: Datenprovider, Dienstanbieter und Dienstkomponenten. Anbieter können in zwei Kategorien geteilt werden: diejenigen, die Daten anbieten, und diejenigen, die Dienste anbieten. Ein *Datenprovider* besitzt eigene Daten und stellt diese für Ihre Anwendung in tabellarischer Form bereit. Ein *Dienstanbieter* kapselt einen Dienst durch Erstellen und Verwenden von Daten und Vergrößern von Features in den ADO-Anwendungen. Ein Dienstanbieter kann darüber hinaus auch als *Dienstkomponente* definiert werden, die mit anderen Dienstanbietern oder -komponenten verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a0b58-p101">This section addresses three kinds of providers: data providers, service providers, and service components. Providers fall into two categories: those providing data and those providing services. A *data provider* owns its own data and exposes it in tabular form to your application. A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications. A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="a0b58-109">Datenprovider</span><span class="sxs-lookup"><span data-stu-id="a0b58-109">Data Providers</span></span>

<span data-ttu-id="a0b58-110">ADO ist leistungsfähig und flexibel, da es eine Verbindung mit einem beliebigen Datenprovider herstellen und unabhängig von den spezifischen Features eines bestimmten Anbieters dennoch dasselbe Programmiermodell verfügbar machen kann.</span><span class="sxs-lookup"><span data-stu-id="a0b58-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="a0b58-p102">Da jedoch jeder Datenprovider einzigartig ist, ergeben sich bei der Interaktion der Anwendung mit ADO je nach Datenprovider geringfügige Abweichungen. Die Abweichungen können einer von drei Kategorien zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="a0b58-p102">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider. The differences usually fall into one of three categories:</span></span>

  - <span data-ttu-id="a0b58-113">Connection-Parameter in der ConnectionString-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a0b58-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

  - <span data-ttu-id="a0b58-114">Verwendung des [Command](command-object-ado.md)-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0b58-114">[Command](command-object-ado.md) object usage.</span></span>

  - <span data-ttu-id="a0b58-115">Anbieterspezifisches [Recordset](recordset-object-ado.md)-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="a0b58-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="a0b58-116">Ausführliche Informationen zu den derzeit von Microsoft erhältlichen Datenprovidern finden Sie in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="a0b58-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0b58-117">Bereich</span><span class="sxs-lookup"><span data-stu-id="a0b58-117">Area</span></span></p></th>
<th><p><span data-ttu-id="a0b58-118">Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a0b58-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0b58-119">ODBC-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="a0b58-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="a0b58-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB-Anbieter für ODBC</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b58-121">Microsoft Indexdienst</span><span class="sxs-lookup"><span data-stu-id="a0b58-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="a0b58-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB-Anbieter für Microsoft Indexdienst</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b58-123">Microsoft Active Directory-Dienst</span><span class="sxs-lookup"><span data-stu-id="a0b58-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="a0b58-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB-Anbieter für Microsoft Active Directory-Dienst</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b58-125">Microsoft Jet-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="a0b58-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="a0b58-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB-Anbieter für Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b58-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="a0b58-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="a0b58-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB-Anbieter für SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b58-129">Oracle-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="a0b58-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="a0b58-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB-Anbieter für Oracle</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b58-131">Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="a0b58-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="a0b58-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="a0b58-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="a0b58-133">Anbieterspezifische dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0b58-133">Provider-Specific Dynamic Properties</span></span>

<span data-ttu-id="a0b58-p103">Die [Properties](properties-collection-ado.md)-Auflistungen von [Connection](connection-object-ado.md)-, [Command](command-object-ado.md)- und [Recordset](recordset-object-ado.md)-Objekten enthalten anbieterspezifische dynamische Eigenschaften. Diese Eigenschaften stellen über die von ADO unterstützten integrierten Eigenschaften hinaus Informationen zur anbieterspezifischen Funktionalität bereit.</span><span class="sxs-lookup"><span data-stu-id="a0b58-p103">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider. These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="a0b58-p104">Wenden Sie nach dem Herstellen der Verbindung und dem Erstellen dieser Objekte die Refresh-Methode auf die Properties-Auflistung des Objekts an, um die anbieterspezifischen Eigenschaften zu erhalten. Ausführliche Informationen zu diesen dynamischen Eigenschaften finden Sie in der Dokumentation zum Anbieter sowie in OLE DB Programmer's Reference.</span><span class="sxs-lookup"><span data-stu-id="a0b58-p104">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties. Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="a0b58-138">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a0b58-138">Service Providers</span></span>

<span data-ttu-id="a0b58-p105">Um einen Dienstanbieter zu verwenden, müssen Sie ein Schlüsselwort angeben. Darüber hinaus müssen Sie die anbieterspezifischen dynamischen Eigenschaften kennen, die den einzelnen Dienstanbietern zugeordnet sind. Informationen zu anwenderspezifischen Eigenschaften für die derzeit von Microsoft erhältlichen Dienstanbieter finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="a0b58-p105">To use a service provider, you must supply a keyword. You should also be aware of the provider-specific dynamic properties associated with each service provider. Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

  - [<span data-ttu-id="a0b58-142">Microsoft Data Shaping Dienst für OLE DB</span><span class="sxs-lookup"><span data-stu-id="a0b58-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

  - [<span data-ttu-id="a0b58-143">Microsoft OLE DB-Anbieter für Persistenz</span><span class="sxs-lookup"><span data-stu-id="a0b58-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

  - [<span data-ttu-id="a0b58-144">Microsoft OLE DB-Anbieter für Remoting</span><span class="sxs-lookup"><span data-stu-id="a0b58-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="a0b58-145">Dienstkomponenten</span><span class="sxs-lookup"><span data-stu-id="a0b58-145">Service Components</span></span>

<span data-ttu-id="a0b58-p106">Die Dienstkomponente [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ergänzt die Cursor-Hilfsfunktionen von Datenanbietern. Sie erfordert ebenfalls ein Schlüsselwort und hat dynamische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a0b58-p106">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers. It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="a0b58-148">Weitere Informationen zu Anbietern finden Sie in der Dokumentation für Microsoft OLE DB in Microsoft Data Access Components SDK oder besuchen Sie das [Data Plattform Developer Center](https://msdn.microsoft.com/data/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0b58-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://msdn.microsoft.com/data/default.aspx).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="a0b58-149">Providerbefehle</span><span class="sxs-lookup"><span data-stu-id="a0b58-149">Provider Commands</span></span>

<span data-ttu-id="a0b58-150">Für jeden Anbieter hier aufgeführt, wenn Ihre Anwendung Benutzer SQL-Anweisungen wie die Providerbefehle eingeben können, müssen immer überprüft die Benutzereingabe und seien Sie wachsam von möglichen Hackerangriffen mit potenziell gefährlicher SQL-Anweisung, z. B., als Teil der Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="a0b58-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

