---
title: Trennen und Wiederherstellen der Verbindung für des Recordset-Objekts
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac1bc4c9c9d6d149faeb18d73f17539e63a4147e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943941"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="e098e-102">Trennen und Wiederherstellen der Verbindung für des Recordset-Objekts</span><span class="sxs-lookup"><span data-stu-id="e098e-102">Disconnecting and reconnecting the Recordset</span></span>


<span data-ttu-id="e098e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e098e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="e098e-104">Disconnecting and Reconnecting the Recordset</span><span class="sxs-lookup"><span data-stu-id="e098e-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="e098e-p101">Eine der leistungsstärksten Features in ADO ist die Funktion zum Öffnen eines clientseitigen **Recordset**-Objekts in einer Datenquelle und das anschließende *Trennen* des **Recordset**-Objekts von der Datenquelle. Nachdem das **Recordset**-Objekt getrennt wurde, kann die Verbindung zur Datenquelle geschlossen werden, wodurch die auf dem Server vorhandenen Ressourcen zur Verwaltung der Verbindung freigegeben werden. Sie können die Daten im **Recordset**-Objekt weiterhin bearbeiten und anzeigen, wenn keine Verbindung besteht. Später können Sie dann erneut eine Verbindung mit der Datenquelle herstellen und Ihre Aktualisierungen im Batchmodus senden.</span><span class="sxs-lookup"><span data-stu-id="e098e-p101">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source. Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it. You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="e098e-p102">Zum Trennen eines **Recordset**-Objekts, öffnen Sie dieses mit der Cursorplatzierung **adUseClient**, und legen Sie dann die **ActiveConnection**-Eigenschaft auf *Nothing* fest. (C++-Benutzer sollten zum Trennen die **ActiveConnection**-Eigenschaft auf NULL festlegen.)</span><span class="sxs-lookup"><span data-stu-id="e098e-p102">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*. (C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="e098e-110">Weiter unten in diesem Kapitel bei der Behandlung der permanenten Verfügbarkeit des **Recordset** -Objekts werden wir ein getrenntes **Recordset** -Objekt verwenden, um die Daten in einem **Recordset** -Objekt für eine Anwendung bereitzustellen, während der Clientcomputer mit keinem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e098e-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

