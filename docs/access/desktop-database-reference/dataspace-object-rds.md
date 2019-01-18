---
title: DataSpace-Objekt (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716566"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="6ff4f-102">DataSpace-Objekt (RDS)</span><span class="sxs-lookup"><span data-stu-id="6ff4f-102">DataSpace object (RDS)</span></span>

<span data-ttu-id="6ff4f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ff4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ff4f-104">Erstellt clientseitige Proxys für angepasste Geschäftsobjekte, die sich auf der mittleren Ebene befinden.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff4f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ff4f-105">Remarks</span></span>

<span data-ttu-id="6ff4f-p101">Remote Data Service benötigt Proxys für Geschäftsobjekte, damit clientseitige Komponenten mit Geschäftsobjekten kommunizieren können, die sich auf der mittleren Ebene befinden. Proxys vereinfachen das Verpacken, Entpacken und Übertragen (Marshalling) der [Recordset](recordset-object-ado.md)-Daten der Anwendung über Prozess- oder Computergrenzen.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-p101">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier. Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="6ff4f-p102">Remote Data Service verwendet die **CreateObject**-Methode des [RDS.DataSpace](createobject-method-rds.md) -Objekts, um Geschäftsobjektproxys zu erstellen. Der Geschäftsobjektproxy wird dynamisch erstellt, wenn eine Instanz eines Gegenstücks seines Geschäftsobjekts der mittleren Ebene erstellt wird. Remote Data unterstützt die folgenden Protokolle: HTTP, HTTPS (HTTP Secure Sockets), DCOM und In-Process (die Clientkomponenten und das Geschäftsobjekt befinden sich auf demselben Computer).</span><span class="sxs-lookup"><span data-stu-id="6ff4f-p102">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies. The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created. Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="6ff4f-p103">[!HINWEIS] RDS verhält sich "zustandslos", wenn das **RDS.DataSpace** -Objekt das HTTP- oder HTTPS-Protokoll verwendet. Das heißt, alle internen Informationen über eine Clientanforderung werden gelöscht, nachdem der Server eine Antwort zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-p103">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols. That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="6ff4f-p104">Obwohl das Geschäftsobjekt während der Lebensdauer des Geschäftsobjektproxys vorhanden zu sein scheint, ist das Geschäftsobjekt tatsächlich nur vorhanden, bis eine Antwort auf die Anforderung gesendet wird. Wenn eine Anforderung ausgegeben wird (d. h. es wird eine Methode für das Geschäftsobjekt aufgerufen), öffnet der Proxy eine neue Verbindung zum Server, und der Server erstellt eine neue Instanz des Geschäftsobjekts. Nachdem das Geschäftsobjekt auf die Anforderung geantwortet hat, löscht der Server das Geschäftsobjekt und schließt die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-p104">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request. When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object. After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="6ff4f-p105">Dieses Verhalten bedeutet, dass Sie keine Daten mithilfe einer Geschäftsobjekteigenschaft oder einer Variablen von einer Anforderung an eine andere übergeben können. Sie müssen zum Speichern von Zustandsdaten ein anderes Verfahren verwenden, wie etwa eine Datei oder ein Methodenargument.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-p105">This behavior means you cannot pass data from one request to another using a business object property or variable. You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="6ff4f-118">Die Klassen-ID für das **RDS.DataSpace** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="6ff4f-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

