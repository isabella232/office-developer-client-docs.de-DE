---
title: DataFactory-Anpassung
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700024"
---
# <a name="datafactory-customization"></a><span data-ttu-id="251cd-102">DataFactory-Anpassung</span><span class="sxs-lookup"><span data-stu-id="251cd-102">DataFactory customization</span></span>


<span data-ttu-id="251cd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="251cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="251cd-p101">Durch Remote Data Service (RDS) wird eine Möglichkeit bereitgestellt, problemlosen Datenzugriff in einem dreistufigen Client-/Server-System auszuführen. Durch ein Clientdatensteuerelement werden die Parameter für Verbindungs- und Befehlszeichenfolgen zum Ausführen einer Abfrage für eine Remotedatenquelle oder Parameter für Verbindungszeichenfolgen und [Recordset](recordset-object-ado.md)-Objekte zum Ausführen einer Aktualisierung angegeben.</span><span class="sxs-lookup"><span data-stu-id="251cd-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="251cd-p102">Die Parameter werden einem Serverprogramm übergeben, durch das die Datenzugriffsoperation für die Remotedatenquelle ausgeführt wird. Durch RDS wird ein Standardserverprogramm, das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt, bereitgestellt. Durch das **RDSServer.DataFactory** -Objekt werden alle von einer Abfrage an den Client erzeugten **Recordset** -Objekte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="251cd-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="251cd-p103">**RDSServer.DataFactory** ist jedoch auf das Ausführen von Abfragen und Aktualisierungen beschränkt. Eine Überprüfung oder Verarbeitung der Verbindungs- oder Befehlszeichenfolgen kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="251cd-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="251cd-p104">Sie können mit ADO angeben, dass **DataFactory** in Verbindung mit einem anderen Serverprogrammtyp, einem *Handler*, verwendet werden soll. Durch den Handler können Clientverbindungs- und -befehlszeichenfolgen geändert werden, bevor sie zum Zugreifen auf die Datenquelle verwendet werden. Außerdem können durch den Handler Zugriffsrechte erzwungen werden, durch die die Fähigkeit des Clients zum Lesen und Schreiben von Daten in der Datenquelle gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="251cd-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="251cd-114">Die vom Handler zum Ändern von Clientparametern und Zugriffsrechten verwendeten Parameter werden in Abschnitten einer Anpassungsdatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="251cd-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="251cd-115">Weitere Informationen zum Anpassen des **DataFactory** -Objekts finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="251cd-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="251cd-116">Grundlegendes zur Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="251cd-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="251cd-117">Verbinden von Datei-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="251cd-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="251cd-118">Anpassungsdatei – SQL-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="251cd-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="251cd-119">Anpassungsdatei – UserList-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="251cd-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="251cd-120">Anpassungsdatei – Protokollabschnitt</span><span class="sxs-lookup"><span data-stu-id="251cd-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="251cd-121">Erforderliche Clienteinstellungen</span><span class="sxs-lookup"><span data-stu-id="251cd-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="251cd-122">Schreiben eines eigenen benutzerdefinierten Handlers</span><span class="sxs-lookup"><span data-stu-id="251cd-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
