---
title: Grundlegendes RDS-Programmierungsmodell
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717958"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="cb1a1-102">Grundlegendes RDS-Programmierungsmodell</span><span class="sxs-lookup"><span data-stu-id="cb1a1-102">Basic RDS programming model</span></span>

<span data-ttu-id="cb1a1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb1a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb1a1-p101">RDS ist für Anwendungen in der folgenden Umgebung gedacht: Durch eine Clientanwendung werden ein auf einem Server ausgeführtes Programm und die erforderlichen Parameter zum Rückgeben der gewünschten Informationen angegeben. Das auf dem Server aufgerufene Programm erhält Zugriff auf die angegebene Datenquelle, ruft die Informationen ab, verarbeitet optional die Daten und gibt dann die resultierenden Informationen in einer einfach zu verwendenden Form an die Clientanwendung zurück. Durch RDS werden die Mittel bereitgestellt, die Sie zum Ausführen der folgenden Aktionssequenz benötigen:</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

- <span data-ttu-id="cb1a1-p102">Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit, vom Client darauf zu verweisen. (Dieser Verweis wird manchmal als *Proxy* bezeichnet. Er stellt das Remoteserverprogramm dar. Durch die Clientanwendung wird der Proxy wie ein lokales Programm "aufgerufen", obwohl tatsächlich das Remoteserverprogramm aufgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

- <span data-ttu-id="cb1a1-p103">Rufen Sie das Serverprogramm auf. Übergeben Sie dem Serverprogramm Parameter, durch die die Datenquelle und der auszugebende Befehl identifiziert werden. (Vom Serverprogramm wird tatsächlich ADO für den Zugriff auf die Datenquelle verwendet. Durch ADO wird eine Verbindung mit einem der angegebenen Parameter hergestellt, und dann wird der im anderen Parameter angegebene Befehl ausgegeben.)</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

- <span data-ttu-id="cb1a1-p104">Das Serverprogramm erhält ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle. Optional wird das **Recordset** -Objekt auf dem Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="cb1a1-117">Vom Serverprogramm wird das endgültige **Recordset** -Objekt an die Clientanwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-117">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="cb1a1-118">Auf dem Client wird das **Recordset** -Objekt in eine Form umgewandelt, die von visuellen Steuerelementen problemlos verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="cb1a1-119">Alle Änderungen am **Recordset** -Objekt werden zurück an das Serverprogramm gesendet, von dem sie zum Aktualisieren der Datenquelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="cb1a1-p105">Dieses Programmiermodell enthält bestimmte Komfortfeatures. Wenn Sie für den Zugriff auf die Datenquelle kein komplexes Serverprogramm benötigen und wenn Sie die erforderliche Verbindung und die erforderlichen Befehlsparameter bereitstellen, werden die angegebenen Daten von RDS automatisch mit einem einfachen Standardserverprogramm abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="cb1a1-p106">Wenn Sie eine komplexere Verarbeitung benötigen, können Sie ein eigenes benutzerdefiniertes Serverprogramm angeben. Da ein benutzerdefiniertes Serverprogramm über die volle Leistungsfähigkeit von ADO verfügt, kann damit eine Verbindung mit mehreren anderen Datenquellen hergestellt werden, die Daten können auf komplexe Weise kombiniert werden, und dann kann ein einfaches verarbeitetes Ergebnis an die Clientanwendung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="cb1a1-124">Wenn Ihre Anforderungen irgendwo dazwischen liegen, wird von ADO jetzt das Anpassen des Verhaltens des Standardserverprogramms unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb1a1-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

