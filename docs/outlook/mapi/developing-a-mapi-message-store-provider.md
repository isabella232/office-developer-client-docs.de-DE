---
title: Entwickeln eines MAPI-Nachrichtenspeicheranbieteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aaf4e986b72c4ba34489f5880e95866436580172
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561831"
---
# <a name="developing-a-mapi-message-store-provider"></a>Entwickeln eines MAPI-Nachrichtenspeicheranbieteres
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie andere MAPI-Dienstanbieter sind Nachrichtenspeicher Dynamic Link Libraries (DLLs), die die Dienste eines zugrunde liegenden Speichermechanismus für MAPI-Clientanwendungen und den MAPI-Spooler darstellen. Der Nachrichtenspeicheranbieter stellt den zugrunde liegenden Speichermechanismus als hierarchischen Satz von Ordnern und Nachrichten dar, die MAPI-Clients und der MAPI-Spooler verwenden können.
  
Die folgende Abbildung zeigt die grundlegende ARCHITEKTUR DES MAPI-Nachrichtenspeichers.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers](media/storearc.gif "Architektur des Nachrichtenspeichers")
  
Sie können einen Nachrichtenspeicheranbieter mithilfe eines beliebigen zugrunde liegenden Speichermechanismus implementieren. Sie müssen sich jedoch über Leistungsaspekte im Klaren sein. Darüber hinaus muss der zugrunde liegende Speichermechanismus als hierarchische Sammlung von MAPI-Objekten dargestellt werden. Diese Anforderungen bedeuten, dass Nachrichtenspeicher in der Regel mithilfe eines vorhandenen Datenbankprodukts implementiert werden, das die hierarchische Speicherung von Objekten in der Datenbank unterstützt und über eine Programmierschnittstelle oder eine definierte Dateistruktur verfügt. Beispielsweise können Microsoft Office Access-, SQL- und Oracle-Datenbanken als zugrunde liegender Speichermechanismus verwendet werden. Einige Datenbankprodukte verfügen über Featuresätze, die die Implementierung von MAPI-Features vereinfachen, sodass die Auswahl des Datenbankprodukts von den Features betroffen sein kann, die Ihr Nachrichtenspeicheranbieter unterstützen muss.
  
Die Verwendung einer vorhandenen Datenbank als zugrunde liegender Speichermechanismus spart Ihnen Arbeit, da es in der Regel einfacher ist, MapI-Clients Datenbankobjekte als MAPI-Objekte darzustellen, als ihren eigenen hierarchischen Speichermechanismus zu implementieren. Auf diese Weise können Sie MAPI-Vorgänge auf einer höheren Ebene behandeln, als wenn Sie Einen eigenen hierarchischen Speichermechanismus implementieren. Beispielsweise wird die Suche nach einer Nachricht mit einer bestimmten Betreffzeile zu einer relativ einfachen Aufgabe, eine entsprechende Datenbankabfrage zu erstellen und zu übermitteln, anstatt komplexe Routinen zum Durchsuchen des hierarchischen Speichermechanismus zu implementieren.
  
Nachrichtenspeicheranbieter kommunizieren mit MAPI-Clients und dem MAPI-Spooler, um Vorgänge für Ordner und Objekte auszuführen. Der Nachrichtenspeicheranbieter übersetzt diese Vorgänge in Vorgänge auf niedrigerer Ebene für den zugrunde liegenden Speichermechanismus. Der MAPI-Spooler kommuniziert in der Regel beim Senden und Empfangen von Nachrichten mit dem Nachrichtenspeicheranbieter. MAPI-Clients kommunizieren in der Regel mit Nachrichtenspeicheranbietern, um die Ordnerhierarchie zu bearbeiten und Nachrichten zu lesen, zu bearbeiten, zu löschen und zu senden.
  
Sowohl die MAPI-Spooler- als auch die MAPI-Clients kommunizieren mit dem Nachrichtenspeicheranbieter, um neue Nachrichten zu erstellen. Clientanwendungen tun dies, wenn Benutzer eine Nachricht verfassen. Der MAPI-Spooler führt dies aus, wenn er eine eingehende Nachricht empfängt. In beiden Fällen wird die neue Nachricht in der Regel im Posteingangsordner des Nachrichtenspeichers erstellt, sofern vorhanden.
  
Nachrichtenspeicheranbieter nutzen MAPI-Tabellen, -Ordner, -Nachrichten und -Eigenschaften stark. Die Implementierungsdetails für diese Objekte sind in [MAPI-Tabellen,](mapi-tables.md) [MAPI-Ordnern,](mapi-folders.md) [MAPI-Nachrichten](mapi-messages.md)und [MAPI-Eigenschaftsübersicht](mapi-property-overview.md)dokumentiert. Machen Sie sich mit diesem Material vertraut, bevor Sie versuchen, einen Nachrichtenspeicheranbieter zu implementieren.
  
Es gibt zwei wichtige Typen von Nachrichtenspeicheranbietern: anbieter, die als Standardnachrichtenspeicher eines Benutzers fungieren können, und solche, die nicht möglich sind. Ein Standardnachrichtenspeicher ist einer, in dem Clientanwendungen und der MAPI-Spooler eine beliebige Messagingaufgabe ausführen können, z. B. nachrichten empfangen oder Ordner erstellen. Ein Standardmäßiger Nachrichtenspeicheranbieter muss mehrere weitere Features unterstützen als die Mindestanzahl, die für alle Nachrichtenspeicheranbieter erforderlich ist.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)

