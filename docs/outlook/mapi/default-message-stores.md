---
title: Standardnachrichtentspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576911"
---
# <a name="default-message-stores"></a>Standardnachrichtentspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Standardnachrichtentspeicher ist ein Speicher, den Clientanwendungen für allgemeine Aufgaben im Zusammenhang mit Nachrichten verwenden können. Es gibt eine Reihe optionaler Features für Nachrichtenspeicheranbieter, die erforderlich werden, wenn der Nachrichtenspeichernanbieter als Standardnachrichtentspeicher verwendet werden soll. Dies sind wie folgt:
  
- Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.
    
- Bereitstellen von Lese- und nonread Berichten.
    
- Zulassen der Übermittlung von eingehenden und ausgehenden Nachrichten.
    
- Zulassen der Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.
    
- Unterstützung benannter und mehrwertige Eigenschaften.
    
- Unterstützung der [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)-Methode, auch dann, wenn der Nachrichtenspeicheranbieter eng mit einem Transportanbieter verknüpft ist. 
    
- Unterstützung zugehöriger Inhaltstabellen. Weitere Informationen finden Sie unter [Inhaltstabellen](contents-tables.md).
    
- Unterstützung der Benachrichtigung des MAPI-Spoolers, wenn sich Nachrichten in der Warteschlange für ausgehende Nachrichten befinden.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

