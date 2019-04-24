---
title: RDS-Programmiermodell mit Objekten
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301050"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="c9d1d-102">RDS-Programmiermodell mit Objekten</span><span class="sxs-lookup"><span data-stu-id="c9d1d-102">RDS programming model with objects</span></span>

<span data-ttu-id="c9d1d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9d1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9d1d-p101">Das Ziel von RDS besteht darin, über einen Vermittler wie IIS (Internet Information Services, Internetinformationsdienste) Zugriff auf Datenquellen zu erhalten und diese zu aktualisieren. Durch das Programmiermodell wird die Reihenfolge der zum Erreichen dieses Ziels notwendigen Aktivitäten angegeben. Durch das Objektmodell werden die Objekte angegeben, deren Methoden und Eigenschaften sich auf das Programmiermodell auswirken.</span><span class="sxs-lookup"><span data-stu-id="c9d1d-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="c9d1d-107">Durch RDS werden die Mittel bereitgestellt, die zum Ausführen der folgenden Aktionssequenz benötigt werden:</span><span class="sxs-lookup"><span data-stu-id="c9d1d-107">RDS provides the means to perform the following sequence of actions:</span></span>

- <span data-ttu-id="c9d1d-108">Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen ([RDS.DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="c9d1d-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

- <span data-ttu-id="c9d1d-p102">Rufen Sie das Serverprogramm auf. Übergeben Sie dem Serverprogramm Parameter, durch die die Datenquelle und der auszugebende Befehl identifiziert werden (Proxy oder [RDS.DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="c9d1d-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

- <span data-ttu-id="c9d1d-p103">Das Serverprogramm erhält ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle, normalerweise mithilfe von ADO. Optional wird das **Recordset**-Objekt auf dem Server verarbeitet ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="c9d1d-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

- <span data-ttu-id="c9d1d-113">Vom Serverprogramm wird das endgültige **Recordset**-Objekt an die Clientanwendung (Proxy) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9d1d-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

- <span data-ttu-id="c9d1d-114">Auf dem Client wird das **Recordset**-Objekt in eine Form umgewandelt, die von visuellen Steuerelementen (visuelles Steuerelement und **RDS.DataControl**) problemlos verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9d1d-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

- <span data-ttu-id="c9d1d-115">Änderungen am **Recordset**-Objekt werden zurück an den Server gesendet und zum Aktualisieren der Datenquelle (**RDS.DataControl** oder **RDSServer.DataFactory**) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9d1d-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

