---
title: DataFactory-Anpassung
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f058dd76d9ae4f95b6a3d051e741039eb7609f5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860868"
---
# <a name="datafactory-customization"></a><span data-ttu-id="6f4a3-102">DataFactory-Anpassung</span><span class="sxs-lookup"><span data-stu-id="6f4a3-102">DataFactory Customization</span></span>


<span data-ttu-id="6f4a3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f4a3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f4a3-p101">Durch Remote Data Service (RDS) wird eine Möglichkeit bereitgestellt, problemlosen Datenzugriff in einem dreistufigen Client-/Server-System auszuführen. Durch ein Clientdatensteuerelement werden die Parameter für Verbindungs- und Befehlszeichenfolgen zum Ausführen einer Abfrage für eine Remotedatenquelle oder Parameter für Verbindungszeichenfolgen und [Recordset](recordset-object-ado.md)-Objekte zum Ausführen einer Aktualisierung angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="6f4a3-p102">Die Parameter werden einem Serverprogramm übergeben, durch das die Datenzugriffsoperation für die Remotedatenquelle ausgeführt wird. Durch RDS wird ein Standardserverprogramm, das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt, bereitgestellt. Durch das **RDSServer.DataFactory** -Objekt werden alle von einer Abfrage an den Client erzeugten **Recordset** -Objekte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="6f4a3-p103">**RDSServer.DataFactory** ist jedoch auf das Ausführen von Abfragen und Aktualisierungen beschränkt. Eine Überprüfung oder Verarbeitung der Verbindungs- oder Befehlszeichenfolgen kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="6f4a3-p104">Sie können mit ADO angeben, dass **DataFactory** in Verbindung mit einem anderen Serverprogrammtyp, einem *Handler*, verwendet werden soll. Durch den Handler können Clientverbindungs- und -befehlszeichenfolgen geändert werden, bevor sie zum Zugreifen auf die Datenquelle verwendet werden. Außerdem können durch den Handler Zugriffsrechte erzwungen werden, durch die die Fähigkeit des Clients zum Lesen und Schreiben von Daten in der Datenquelle gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="6f4a3-114">Die vom Handler zum Ändern von Clientparametern und Zugriffsrechten verwendeten Parameter werden in Abschnitten einer Anpassungsdatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="6f4a3-115">Weitere Informationen zum Anpassen des **DataFactory** -Objekts finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6f4a3-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

  - [<span data-ttu-id="6f4a3-116">Grundlegendes zur Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f4a3-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)

  - [<span data-ttu-id="6f4a3-117">Connect-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f4a3-117">Customization File Connect Section</span></span>](customization-file-connect-section.md)

  - [<span data-ttu-id="6f4a3-118">SQL-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f4a3-118">Customization File SQL Section</span></span>](customization-file-sql-section.md)

  - [<span data-ttu-id="6f4a3-119">UserList-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f4a3-119">Customization File UserList Section</span></span>](customization-file-userlist-section.md)

  - [<span data-ttu-id="6f4a3-120">Logs-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f4a3-120">Customization File Logs Section</span></span>](customization-file-logs-section.md)

  - [<span data-ttu-id="6f4a3-121">Erforderliche Clienteinstellungen</span><span class="sxs-lookup"><span data-stu-id="6f4a3-121">Required Client Settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)

  - [<span data-ttu-id="6f4a3-122">Schreiben eines eigenen benutzerdefinierten Handlers</span><span class="sxs-lookup"><span data-stu-id="6f4a3-122">Writing Your Own Customized Handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
