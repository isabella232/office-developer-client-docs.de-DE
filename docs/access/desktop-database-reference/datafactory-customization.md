---
title: DataFactory-Anpassung
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b805f9d6ff7a1f3b27bb5600d42cabf8fce651cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475332"
---
# <a name="datafactory-customization"></a><span data-ttu-id="ca73e-102">DataFactory-Anpassung</span><span class="sxs-lookup"><span data-stu-id="ca73e-102">DataFactory Customization</span></span>


<span data-ttu-id="ca73e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca73e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca73e-p101">Durch Remote Data Service (RDS) wird eine Möglichkeit bereitgestellt, problemlosen Datenzugriff in einem dreistufigen Client-/Server-System auszuführen. Durch ein Clientdatensteuerelement werden die Parameter für Verbindungs- und Befehlszeichenfolgen zum Ausführen einer Abfrage für eine Remotedatenquelle oder Parameter für Verbindungszeichenfolgen und [Recordset](recordset-object-ado.md)-Objekte zum Ausführen einer Aktualisierung angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca73e-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="ca73e-p102">Die Parameter werden einem Serverprogramm übergeben, durch das die Datenzugriffsoperation für die Remotedatenquelle ausgeführt wird. Durch RDS wird ein Standardserverprogramm, das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt, bereitgestellt. Durch das **RDSServer.DataFactory** -Objekt werden alle von einer Abfrage an den Client erzeugten **Recordset** -Objekte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca73e-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="ca73e-p103">**RDSServer.DataFactory** ist jedoch auf das Ausführen von Abfragen und Aktualisierungen beschränkt. Eine Überprüfung oder Verarbeitung der Verbindungs- oder Befehlszeichenfolgen kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ca73e-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="ca73e-p104">Sie können mit ADO angeben, dass **DataFactory** in Verbindung mit einem anderen Serverprogrammtyp, einem *Handler*, verwendet werden soll. Durch den Handler können Clientverbindungs- und -befehlszeichenfolgen geändert werden, bevor sie zum Zugreifen auf die Datenquelle verwendet werden. Außerdem können durch den Handler Zugriffsrechte erzwungen werden, durch die die Fähigkeit des Clients zum Lesen und Schreiben von Daten in der Datenquelle gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="ca73e-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="ca73e-114">Die vom Handler zum Ändern von Clientparametern und Zugriffsrechten verwendeten Parameter werden in Abschnitten einer Anpassungsdatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca73e-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="ca73e-115">Weitere Informationen zum Anpassen des **DataFactory** -Objekts finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ca73e-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

  - [<span data-ttu-id="ca73e-116">Grundlegendes zur Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca73e-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)

  - [<span data-ttu-id="ca73e-117">Connect-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca73e-117">Customization File Connect Section</span></span>](customization-file-connect-section.md)

  - [<span data-ttu-id="ca73e-118">SQL-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca73e-118">Customization File SQL Section</span></span>](customization-file-sql-section.md)

  - [<span data-ttu-id="ca73e-119">UserList-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca73e-119">Customization File UserList Section</span></span>](customization-file-userlist-section.md)

  - [<span data-ttu-id="ca73e-120">Logs-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca73e-120">Customization File Logs Section</span></span>](customization-file-logs-section.md)

  - <span data-ttu-id="ca73e-121">[Erforderliche Clienteinstellungen](https://msdn.microsoft.com/library/ff836356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ca73e-121">[Required Client Settings](https://msdn.microsoft.com/library/ff836356\(v=office.15\))</span></span>

  - <span data-ttu-id="ca73e-122">[Schreiben eines eigenen benutzerdefinierten Handlers](https://msdn.microsoft.com/library/jj249402\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ca73e-122">[Writing Your Own Customized Handler](https://msdn.microsoft.com/library/jj249402\(v=office.15\))</span></span>

