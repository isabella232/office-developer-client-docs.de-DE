---
title: Datenbindungsobjekt des Adressbuchs
TOCTitle: Address Book Data-Binding Object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfa95c05ac87648c4d69e3d781614d9cd553bc02
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474834"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="a141b-102">Datenbindungsobjekt des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="a141b-102">Address Book Data-Binding Object</span></span>


<span data-ttu-id="a141b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a141b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a141b-p101">In der Adressbuchanwendung wird das [RDS.DataControl](datacontrol-object-rds.md)-Objekt zum Binden von Daten von der SQL Server-Datenbank an visuelle Objekte (in diesem Fall eine DHTML-Tabelle) in der Client-HTML-Seite der Anwendung verwendet. Die ereignisgesteuerte VBScript-Programmlogik verwendet [RDS.DataControl](datacontrol-object-rds.md) für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a141b-p101">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page. The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="a141b-106">Die Datenbank abfragen, Aktualisierungen an die Datenbank senden, und das Datenraster aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a141b-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="a141b-107">Es Benutzern ermöglichen, zum ersten, zum nächsten, zum vorherigen oder zum letzten Datensatz im Datenraster zu springen.</span><span class="sxs-lookup"><span data-stu-id="a141b-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="a141b-108">Mit dem folgenden Code wird die Komponente **RDS.DataControl** definiert:</span><span class="sxs-lookup"><span data-stu-id="a141b-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="a141b-p102">Mit dem OBJECT-Tag wird die Komponente **RDS.DataControl** im Programm definiert. Das Tag umfasst zwei Arten von Parametern:</span><span class="sxs-lookup"><span data-stu-id="a141b-p102">The OBJECT tag defines the **RDS.DataControl** component in the program. The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="a141b-111">Parameter, die dem generischen OBJECT-Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a141b-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="a141b-112">Parameter, die nur für das **RDS.DataControl** -Objekt gelten.</span><span class="sxs-lookup"><span data-stu-id="a141b-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="a141b-113">Generische Parameter des OBJECT-Tags</span><span class="sxs-lookup"><span data-stu-id="a141b-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="a141b-114">In der folgenden Tabellen werden die Parameter beschrieben, die dem OBJECT-Tag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a141b-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a141b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a141b-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="a141b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a141b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a141b-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="a141b-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="a141b-p103">Eine eindeutige 128-Bit-Nummer, mit der der Typ des eingebetteten Objekts für das System definiert wird. Dieser Bezeichner wird in der Systemregistrierung des lokalen Computers verwaltet. (Informationen zu den Klassen-IDs des <strong>RDS.DataControl</strong>-Objekts finden Sie unter <a href="datacontrol-object-rds.md">RDS.DataControl-Objekt</a>.)</span><span class="sxs-lookup"><span data-stu-id="a141b-p103">A unique, 128-bit number that identifies the type of embedded object to the system. This identifier is maintained in the local computer's system registry. (For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a141b-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="a141b-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="a141b-122">Definiert einen dokumentweiten Bezeichner für das eingebettete Objekt, der verwendet wird, um das Objekt im Code zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a141b-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="a141b-123">RDS.DataControl-Tagparameter</span><span class="sxs-lookup"><span data-stu-id="a141b-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="a141b-p104">In der folgenden Tabelle werden die Parameter beschrieben, die für das **RDS.DataControl** -Objekt gelten. (Eine vollständige Liste der **RDS.DataControl** -Objektparameter und Informationen zu deren Implementierung finden Sie unter [RDS.DataControl-Objekt](datacontrol-object-rds.md).)</span><span class="sxs-lookup"><span data-stu-id="a141b-p104">The following table describes the parameters specific to the **RDS.DataControl** object. (For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a141b-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="a141b-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="a141b-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a141b-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a141b-128"><a href="server-property-rds.md">SERVER</a></span><span class="sxs-lookup"><span data-stu-id="a141b-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="a141b-129">Wenn Sie HTTP verwenden, ist der Wert der Name des Servercomputers mit https://.</span><span class="sxs-lookup"><span data-stu-id="a141b-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a141b-130"><a href="connect-property-rds.md">EINE VERBINDUNG HERSTELLEN</a></span><span class="sxs-lookup"><span data-stu-id="a141b-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="a141b-131">Bietet die erforderlichen Verbindungsinformationen für <strong>RDS.DataControl</strong>, um eine Verbindung mit SQL Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a141b-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a141b-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span><span class="sxs-lookup"><span data-stu-id="a141b-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="a141b-133">Legt die Abfragezeichenfolge fest oder gibt sie zurück, mit der das <a href="recordset-object-ado.md">Recordset</a>-Objekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a141b-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

