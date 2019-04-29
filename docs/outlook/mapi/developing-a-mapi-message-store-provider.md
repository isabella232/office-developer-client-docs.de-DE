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
  
Wie andere MAPI-Dienstanbieter sind Nachrichtenspeicher auch DLLs (Dynamic Link Libraries), die die Dienste eines zugrunde liegenden Speichermechanismus für MAPI-Clientanwendungen und die MAPI-Spooler darstellen. Der Nachrichtenspeicher Anbieter stellt den zugrunde liegenden Speichermechanismus als hierarchische Gruppe von Ordnern und Nachrichten dar, die MAPI-Clients und der MAPI-Spooler verwenden können.
  
Die folgende Abbildung zeigt die grundlegende MAPI-Nachrichtenspeicher Architektur.
  
**Architektur des Nachrichtenspeichers**
  
![Nachrichtenspeicher Architektur] (media/storearc.gif "Nachrichtenspeicher Architektur")
  
Sie können einen Nachrichtenspeicher Anbieter mit einer beliebigen Art zugrunde liegender Speichermechanismus implementieren. Sie müssen jedoch auf Leistungsprobleme achten. Darüber hinaus muss der zugrunde liegende Speichermechanismus als hierarchische Auflistung von MAPI-Objekten dargestellt werden. Diese Anforderungen bedeuten, dass Nachrichtenspeicher in der Regel mit einem vorhandenen Datenbankprodukt implementiert werden, das die hierarchische Speicherung von Objekten in der Datenbank unterstützt und über eine Programmierschnittstelle oder eine definierte Dateistruktur verfügt. Beispielsweise können Microsoft Office Access-, SQL-und Oracle-Datenbanken als zugrunde liegender Speichermechanismus verwendet werden. Einige Datenbankprodukte verfügen über Featuregruppen, die die Implementierung von MAPI-Funktionen vereinfachen, sodass die Auswahl des Datenbankprodukts von den Features beeinflusst werden kann, die der Nachrichtenspeicher Anbieter unterstützen muss.
  
Die Verwendung einer vorhandenen Datenbank als zugrunde liegender Speichermechanismus spart Ihre Arbeit, da es in der Regel einfacher ist, MAPI-Clients Datenbankobjekte als MAPI-Objekte darzustellen, als ihren eigenen hierarchischen Speichermechanismus zu implementieren. Auf diese Weise können Sie MAPI-Vorgänge auf einer höheren Ebene behandeln, als wenn Sie einen eigenen hierarchischen Speichermechanismus implementieren. Wenn Sie beispielsweise nach einer Nachricht mit einer bestimmten Betreffzeile suchen, wird es relativ einfach, eine entsprechende Datenbankabfrage zu erstellen und zu übermitteln, statt komplexe Routinen zum Durchsuchen des hierarchischen Speichermechanismus zu implementieren.
  
Nachrichtenspeicher Anbieter kommunizieren mit MAPI-Clients und dem MAPI-Spooler, um Vorgänge für Ordner und Objekte auszuführen. Der Nachrichtenspeicher Anbieter übersetzt diese Vorgänge in Vorgänge auf niedrigeren Ebenen des zugrunde liegenden Speichermechanismus. Der MAPI-Spooler kommuniziert beim Senden und empfangen von Nachrichten in der Regel mit dem Nachrichtenspeicher Anbieter. MAPI-Clients kommunizieren in der Regel mit Nachrichtenspeicher Anbietern, um die Ordnerhierarchie zu bearbeiten und Nachrichten zu lesen, zu bearbeiten, zu löschen und zu senden.
  
Sowohl die MAPI-Spooler-als auch die MAPI-Clients kommunizieren mit dem Nachrichtenspeicher Anbieter, um neue Nachrichten zu erstellen. Client Anwendungen tun dies, wenn Benutzer eine Nachricht verfassen. Der MAPI-Spooler führt dies aus, wenn er eine eingehende Nachricht empfängt. In beiden Fällen wird die neue Nachricht in der Regel im Posteingang-Ordner des Nachrichtenspeichers erstellt, sofern vorhanden.
  
Nachrichtenspeicher Anbieter nutzen die MAPI-Tabellen,-Ordner,-Nachrichten und-Eigenschaften stark. Die Implementierungsdetails für diese Objekte sind in [MAPI-Tabellen](mapi-tables.md), [MAPI-Ordnern](mapi-folders.md), MAPI- [Nachrichten](mapi-messages.md)und der [MAPI-Eigenschaftsübersicht](mapi-property-overview.md)dokumentiert. Sie sollten sich mit diesem Material vertraut machen, bevor Sie versuchen, einen Nachrichtenspeicher Anbieter zu implementieren.
  
Es gibt zwei wichtige Arten von Nachrichtenspeicher Anbietern: solche, die als Standardnachrichtenspeicher eines Benutzers fungieren können, und solche, die nicht möglich sind. Ein Standardnachrichtenspeicher ist einer, in dem Clientanwendungen und der MAPI-Spooler beliebige Messagingaufgaben ausführen können, beispielsweise das Empfangen von Nachrichten oder das Erstellen von Ordnern. Ein standardmäßiger Nachrichtenspeicher Anbieter muss mehrere Features unterstützen als die Mindestanzahl, die für alle Nachrichtenspeicher Anbieter erforderlich ist.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)

