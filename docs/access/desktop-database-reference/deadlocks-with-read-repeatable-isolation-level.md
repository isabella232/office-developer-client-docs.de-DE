---
title: Deadlocks mit lesbarer wiederholbarer Isolationsstufe
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c3b28c8d9be6a81ecc03ccf02d5361110de32f07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558408"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Deadlocks mit lesbarer wiederholbarer Isolationsstufe


**Gilt für**: Access 2013, Office 2013

If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.

Verwenden Sie die dynamische **TimeOut-Eigenschaft** des [Cursordienstbefehls,](microsoft-cursor-service-for-ole-db-ado-service-component.md)um die Länge des Timeouts zu ändern.

