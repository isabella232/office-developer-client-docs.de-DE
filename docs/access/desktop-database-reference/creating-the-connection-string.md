---
title: Erstellen der Verbindungszeichenfolge
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295327"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="8ee1a-102">Erstellen der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8ee1a-102">Creating the connection string</span></span>

<span data-ttu-id="8ee1a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ee1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ee1a-p101">ADO unterstützt direkt fünf Argumente in einer Verbindungszeichenfolge. Andere Argumente werden ohne Verarbeitung durch ADO an den Anbieter übergeben, der im Argument *Provider* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ee1a-106">Argument</span><span class="sxs-lookup"><span data-stu-id="8ee1a-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="8ee1a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ee1a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ee1a-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="8ee1a-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="8ee1a-109">Gibt den Namen eines Anbieters an, der für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee1a-110"><em>File Name</em></span><span class="sxs-lookup"><span data-stu-id="8ee1a-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="8ee1a-111">Gibt den Namen einer anbieterspezifischen Datei an (z. B. ein gespeichertes Datenquellenobjekt), die voreingestellte Verbindungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee1a-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="8ee1a-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="8ee1a-113">Gibt die Verbindungszeichenfolge als absolute URL an, die eine Ressource wie z. B. eine Datei oder ein Verzeichnis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee1a-114"><em>Remote Provider</em></span><span class="sxs-lookup"><span data-stu-id="8ee1a-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="8ee1a-p102">Gibt den Namen eines Anbieters an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="8ee1a-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee1a-117"><em>Remote Server</em></span><span class="sxs-lookup"><span data-stu-id="8ee1a-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="8ee1a-118">Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-118">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="8ee1a-119">(Nur Remote Datendienst.)</span><span class="sxs-lookup"><span data-stu-id="8ee1a-119">(Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="8ee1a-120">In den folgenden Beispielen und im ADO-Programmierhandbuch wird die Benutzer-ID "MyId" mit dem Kennwort "123aBc" zur Authentifizierung beim Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-120">In the following examples and throughout the ADO programmer's guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="8ee1a-121">Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-121">You should substitute these values with valid login credentials for your server.</span></span> <span data-ttu-id="8ee1a-122">Ersetzen Sie außerdem "MySqlServer" durch den Namen Ihres Servers.</span><span class="sxs-lookup"><span data-stu-id="8ee1a-122">Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="8ee1a-123">Für die HelloData-Anwendung in Kapitel 1 wurde die folgende Verbindungszeichenfolge verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ee1a-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="8ee1a-p105">In dieser Verbindungszeichenfolge wurde nur der ADO-Parameter "Provider=SQLOLEDB" bereitgestellt, der für den Microsoft OLE DB-Anbieter für SQL Server steht. Weitere gültige Parameter, die in der Verbindungszeichenfolge übergeben werden können, können mithilfe der Dokumentation des jeweiligen Anbieters bestimmt werden. Gemäß der Dokumentation zum OLE DB-Anbieter für SQL Server können Sie den *Data Source*-Parameter durch "Server" und den *Initial Catalog*-Parameter durch "Database" ersetzen. Die folgende Verbindungszeichenfolge würde demnach die gleichen Ergebnisse wie die erste Verbindungszeichenfolge liefern:</span><span class="sxs-lookup"><span data-stu-id="8ee1a-p105">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server. Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation. According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter. Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="8ee1a-128">Um die Verbindung zu öffnen, übergeben Sie einfach die Verbindungszeichenfolge als erstes Argument in der **Open** -Methode des **Connection** -Objekts:</span><span class="sxs-lookup"><span data-stu-id="8ee1a-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="8ee1a-p106">Viele dieser Informationen können auch bereitgestellt werden, indem Sie Eigenschaften des **Connection** -Objekts vor dem Öffnen der Verbindung festlegen. Beispielsweise könnten Sie mit dem folgenden Code denselben Effekt wie mit der obigen Verbindungszeichenfolge erzielen:</span><span class="sxs-lookup"><span data-stu-id="8ee1a-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

