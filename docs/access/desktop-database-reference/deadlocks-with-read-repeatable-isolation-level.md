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
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Deadlocks bei der Isolationsstufe "Repeatable Read"


**Betrifft**: Access 2013 | Office 2013

Wenn ein benutzerdefiniertes Geschäftsobjekt die Isolationsstufe Repeatable Read für den Zugriff auf einen Computer mit SQL Server verwendet und das Geschäftsobjekt gleichzeitig von zwei Clients aufgerufen wird, die eine Abfrage senden und die gleiche Transaktion aktualisieren, ist ein Deadlock möglich. Mit RDS (Remote Data Service) kann zwar für einen der Vorgänge ein Timeout eintreten, um den Deadlock aufzulösen, aber für diesen Client schlägt die Aktualisierung fehl.

Verwenden Sie die [Microsoft Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)dynamische Eigenschaft**Befehlstimeout** , um die Länge des Timeouts zu ändern.

