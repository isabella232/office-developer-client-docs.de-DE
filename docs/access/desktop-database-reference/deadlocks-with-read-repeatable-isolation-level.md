---
title: Deadlocks bei der Isolationsstufe 'Repeatable Read'
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473237"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="6f4a0-102">Deadlocks bei der Isolationsstufe "Repeatable Read"</span><span class="sxs-lookup"><span data-stu-id="6f4a0-102">Deadlocks With Read Repeatable Isolation Level</span></span>


<span data-ttu-id="6f4a0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f4a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f4a0-p101">Wenn ein benutzerdefiniertes Geschäftsobjekt die Isolationsstufe Repeatable Read für den Zugriff auf einen Computer mit SQL Server verwendet und das Geschäftsobjekt gleichzeitig von zwei Clients aufgerufen wird, die eine Abfrage senden und die gleiche Transaktion aktualisieren, ist ein Deadlock möglich. Mit RDS (Remote Data Service) kann zwar für einen der Vorgänge ein Timeout eintreten, um den Deadlock aufzulösen, aber für diesen Client schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="6f4a0-106">Verwenden Sie die [Microsoft Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)dynamische Eigenschaft**Befehlstimeout** , um die Länge des Timeouts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

