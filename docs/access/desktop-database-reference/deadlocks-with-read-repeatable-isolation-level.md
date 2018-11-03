---
title: Deadlocks bei Lesen wiederholbare Isolationsstufe
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742a9157c3f2f26d70351fc05afa35472654af9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944327"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="d6222-102">Deadlocks bei Lesen wiederholbare Isolationsstufe</span><span class="sxs-lookup"><span data-stu-id="d6222-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="d6222-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6222-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6222-p101">Wenn ein benutzerdefiniertes Geschäftsobjekt die Isolationsstufe Repeatable Read für den Zugriff auf einen Computer mit SQL Server verwendet und das Geschäftsobjekt gleichzeitig von zwei Clients aufgerufen wird, die eine Abfrage senden und die gleiche Transaktion aktualisieren, ist ein Deadlock möglich. Mit RDS (Remote Data Service) kann zwar für einen der Vorgänge ein Timeout eintreten, um den Deadlock aufzulösen, aber für diesen Client schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="d6222-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="d6222-106">Verwenden Sie die [Microsoft Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)dynamische Eigenschaft**Befehlstimeout** , um die Länge des Timeouts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d6222-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

