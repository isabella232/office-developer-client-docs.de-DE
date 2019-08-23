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
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338045"
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

