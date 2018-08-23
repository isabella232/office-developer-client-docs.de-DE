---
title: Entwickeln von einem Anbieter MAPI-Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 36233d51f47c53d6a69494c0fcd799a7c83add29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567874"
---
# <a name="developing-a-mapi-message-store-provider"></a>Entwickeln von einem Anbieter MAPI-Nachricht
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wie andere MAPI-Dienstanbieter sind Nachrichtenspeicher Dynamic Link Libraries (DLLs), die die Dienste eines zugrunde liegende Speichermechanismus MAPI-Clientanwendungen und die MAPI-Warteschlange darstellen. Der Nachricht-Speicher-Anbieter bietet den zugrunde liegende Speichermechanismus als hierarchisch strukturierter Satz von Ordnern und Nachrichten, die MAPI-Clients und die MAPI-Warteschlange verwenden können.
  
Die folgende Abbildung zeigt die grundlegende Architektur des Nachrichtenspeichers MAPI.
  
**Architektur des Nachrichtenspeichers**
  
![Architektur des Nachrichtenspeichers] (media/storearc.gif "Architektur des Nachrichtenspeichers")
  
Sie können eine Nachricht Speicheranbieter mithilfe von irgendeiner zugrunde liegende Speichermechanismus aus, die Sie implementieren. Sie müssen jedoch Leistungsbedenken berücksichtigen. Darüber hinaus muss der zugrunde liegende Speichermechanismus als eine hierarchische Auflistung von MAPI-Objekten dargestellt werden. Diese Anforderungen bedeuten, dass Nachrichtenspeicher in der Regel mit einem vorhandenen Datenbankprodukt unterstützt, die hierarchische Speicherung von Objekten in der Datenbank sowie, eine Programmierschnittstelle oder eindeutig definierter Dateistruktur implementiert werden. Microsoft Office Access, SQL und Oracle-Datenbanken können beispielsweise als der zugrunde liegende Speichermechanismus verwendet werden. Einige Datenbankprodukte haben Featuregruppen, mit die leichter MAPI-Funktionen zu implementieren, damit Ihrer Wahl des Datenbankprodukts durch die Features, die Ihre Nachricht Speicheranbieter zur Unterstützung von muss beeinträchtigt werden kann.
  
Verwenden eine vorhandene Datenbank als die zugrunde liegende Speicher Mechanismus speichert, an denen Sie arbeiten, da es in der Regel leichter vorhanden Datenbankobjekte MAPI-Clients als MAPI-Objekten ist als zu implementieren einen eigenen Mechanismus hierarchisches Speicher. Auf diese Weise können Sie MAPI-Vorgänge auf einer höheren Ebene als, wenn Sie einen eigenen Mechanismus hierarchisches Speicher implementieren zu behandeln. Suchen einer Nachricht mit einer bestimmten Betreffzeile wird beispielsweise recht einfach wenigen erstellen und Senden von einer Abfrage für die gewünschte Datenbank, anstatt implementieren komplexe Routinen, um hierarchische Speichermechanismus zu suchen.
  
Nachricht-Anbieter kommunizieren mit MAPI-Clients und die MAPI-Warteschlange zum Ausführen von Vorgängen für Ordner und Objekte. Der Nachricht Speicheranbieter übersetzt diese Vorgänge in die zugrunde liegende Speicher Mechanismus Vorgänge auf niedriger Ebene. Die MAPI-Warteschlange kommuniziert normalerweise mit der Nachricht Informationsdienst beim Senden und Empfangen von Nachrichten. MAPI-Clients kommunizieren normalerweise mit der Nachricht-Anbieter die Ordnerhierarchie bearbeiten und zu lesen, bearbeiten, löschen und Senden von Nachrichten.
  
Die MAPI-Warteschlange und die MAPI-Clients kommunizieren mit dem Anbieter Nachricht anmelden, um neue Nachrichten zu erstellen. Clientanwendungen dazu beim Verfassen einer Nachricht. Die MAPI-Warteschlange führt dies, wenn sie eine eingehende Nachricht empfängt. In beiden Fällen wird die neue Nachricht in der Regel im Ordner Posteingang des Nachrichtenspeichers, erstellt, sofern vorhanden.
  
Nachricht Anbieter stellen Sie bei der umfassenden Verwendung von MAPI-Tabellen, Ordnern, Nachrichten und Eigenschaften. Die Implementierungsdetails für diese Objekte werden in [MAPI-Tabellen](mapi-tables.md), [MAPI-Ordner](mapi-folders.md), [MAPI-Nachrichten](mapi-messages.md)und [MAPI-Eigenschaften im Überblick](mapi-property-overview.md)dokumentiert. Sie sollten sich mit diesem Material vertraut machen bevor Sie versuchen, einen Anbieter für die Nachricht anmelden zu implementieren.
  
Es gibt zwei wichtige Arten von Anbietern Nachricht: diejenigen, die als Standard für einen Benutzer fungieren können e-Mail-Speicher und die nicht. Ein Standardnachrichtenspeicher ist eine der in der sich Client-Anwendungen und die MAPI-Warteschlange alle messaging Aufgaben wie das Empfangen von Nachrichten oder Erstellen von Ordnern ausführen können. Nachricht Store Standardanbieter muss als die für alle Anbieter für Nachricht Store erforderlichen Mindestanzahl Weitere Features unterstützen.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)

