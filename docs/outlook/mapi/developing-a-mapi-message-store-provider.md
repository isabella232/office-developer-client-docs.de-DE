---
title: Entwickeln eines MAPI-Nachrichtenspeicheranbieteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 76332b57b2957b5682efb415121ea6db42409c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412611"
---
# <a name="developing-a-mapi-message-store-provider"></a>Entwickeln eines MAPI-Nachrichtenspeicheranbieteres
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie andere MAPI-Dienstanbieter sind Nachrichtenspeicher Dynamic Link Libraries (DLLs), die die Dienste eines zugrunde liegenden Speichermechanismus für MAPI-Clientanwendungen und den MAPI-Spooler präsentieren. Der Nachrichtenspeicheranbieter stellt den zugrunde liegenden Speichermechanismus als hierarchischen Satz von Ordnern und Nachrichten vor, die MAPI-Clients und der MAPI-Spooler verwenden können.
  
Die folgende Abbildung zeigt die grundlegende ARCHITEKTUR des MAPI-Nachrichtenspeichers.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers](media/storearc.gif "Nachrichtenspeicherarchitektur")
  
Sie können einen Nachrichtenspeicheranbieter mithilfe eines beliebigen zugrunde liegenden Speichermechanismus implementieren. Allerdings müssen Sie sich der Leistungsbedenken bewusst sein. Darüber hinaus muss der zugrunde liegende Speichermechanismus als hierarchische Auflistung von MAPI-Objekten dargestellt werden. Diese Anforderungen bedeuten, dass Nachrichtenspeicher in der Regel mithilfe eines vorhandenen Datenbankprodukts implementiert werden, das die hierarchische Speicherung von Objekten in der Datenbank unterstützt und über eine Programmierschnittstelle oder eine klar definierte Dateistruktur verfügt. Beispielsweise können Microsoft Office Access-, SQL- und Oracle-Datenbanken als zugrunde liegender Speichermechanismus verwendet werden. Einige Datenbankprodukte verfügen über Featuresätze, die die Implementierung von MAPI-Features vereinfachen, sodass Ihre Auswahl des Datenbankprodukts von den Features betroffen sein kann, die Ihr Nachrichtenspeicheranbieter unterstützen muss.
  
Die Verwendung einer vorhandenen Datenbank als zugrunde liegender Speichermechanismus erspart Ihnen Arbeit, da es in der Regel einfacher ist, MapI-Clients Datenbankobjekte als MAPI-Objekte zu präsentieren, als einen eigenen hierarchischen Speichermechanismus zu implementieren. Auf diese Weise können Sie MAPI-Vorgänge auf einer höheren Ebene behandeln, als wenn Sie einen eigenen hierarchischen Speichermechanismus implementieren. Beispielsweise wird die Suche nach einer Nachricht mit einer bestimmten Betreffzeile zu einer ziemlich einfachen Aufgabe, eine entsprechende Datenbankabfrage zu erstellen und zu übermitteln, anstatt komplexe Routinen zu implementieren, um Ihren hierarchischen Speichermechanismus zu durchsuchen.
  
Nachrichtenspeicheranbieter kommunizieren mit MAPI-Clients und dem MAPI-Spooler, um Vorgänge für Ordner und Objekte durchzuführen. Der Nachrichtenspeicheranbieter übersetzt diese Vorgänge in Vorgänge auf niedrigerer Ebene für den zugrunde liegenden Speichermechanismus. Der MAPI-Spooler kommuniziert normalerweise beim Senden und Empfangen von Nachrichten mit dem Nachrichtenspeicheranbieter. MAPI-Clients kommunizieren in der Regel mit Nachrichtenspeicheranbietern, um die Ordnerhierarchie zu bearbeiten und Nachrichten zu lesen, zu bearbeiten, zu löschen und zu senden.
  
Sowohl die MAPI-Spooler- als auch die MAPI-Clients kommunizieren mit dem Nachrichtenspeicheranbieter, um neue Nachrichten zu erstellen. Clientanwendungen tun dies, wenn Benutzer eine Nachricht verfassen. Der MAPI-Spooler führt dies aus, wenn er eine eingehende Nachricht empfängt. In beiden Fällen wird die neue Nachricht in der Regel im Posteingangsordner des Nachrichtenspeichers erstellt, wenn es eine gibt.
  
Nachrichtenspeicheranbieter nutzen MAPI-Tabellen, Ordner, Nachrichten und Eigenschaften stark. Die Implementierungsdetails für diese Objekte sind in [MAPI Tables,](mapi-tables.md) [MAPI Folders,](mapi-folders.md) [MAPI Messages](mapi-messages.md)und [MAPI Property Overview dokumentiert.](mapi-property-overview.md) Sie sollten sich mit diesem Material vertraut machen, bevor Sie versuchen, einen Nachrichtenspeicheranbieter zu implementieren.
  
Es gibt zwei wichtige Typen von Nachrichtenspeicheranbietern: solche, die als Standardnachrichtenspeicher eines Benutzers fungieren können, und solche, die nicht verwendet werden können. Ein Standardnachrichtenspeicher ist ein Nachrichtenspeicher, in dem Clientanwendungen und der MAPI-Spooler jede Messagingaufgabe ausführen können, z. B. das Empfangen von Nachrichten oder das Erstellen von Ordnern. Ein Standardmäßiger Nachrichtenspeicheranbieter muss mehrere weitere Features als die für alle Nachrichtenspeicheranbieter erforderliche Mindestanzahl unterstützen.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)

