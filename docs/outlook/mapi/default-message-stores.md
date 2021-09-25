---
title: Standard-Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f25fdeb176b2d885a4ba3fbf2bfb8b094de223f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576415"
---
# <a name="default-message-stores"></a>Standardnachrichtentspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Standardnachrichtentspeicher ist ein Speicher, den Clientanwendungen für allgemeine Aufgaben im Zusammenhang mit Nachrichten verwenden können. Es gibt eine Reihe optionaler Features für Nachrichtenspeicheranbieter, die erforderlich werden, wenn der Nachrichtenspeichernanbieter als Standardnachrichtentspeicher verwendet werden soll. Dies sind wie folgt:
  
- Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.
    
- Bereitstellen von Lese- und nonread Berichten.
    
- Eingehende und ausgehende Nachrichten�bermittlungen zulassen.
    
- Erm�glicht die Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.
    
- Unterst�tzung f�r benannte und mehrwertige Eigenschaften.
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- Supporting associated contents tables. For more information, see [Inhalt von Tabellen](contents-tables.md).
    
- Unterstützung der Benachrichtigung des MAPI-Spoolers, wenn sich Nachrichten in der Warteschlange für ausgehende Nachrichten befinden.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

