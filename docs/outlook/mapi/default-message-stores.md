---
title: Standard-Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791494"
---
# <a name="default-message-stores"></a>Standard-Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Ein Standardnachrichtenspeicher ist eine, die Client-Anwendungen f�r allgemeine Zwecke messaging Aufgaben verwenden k�nnen. Es gibt eine Reihe von optionalen Features f�r Nachricht Speicher-Anbieter, die erforderlich werden, wenn der Anbieter die Nachricht wird als Standard-Informationsspeicher verwendet werden soll. Sie sind wie folgt:
  
- Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.
    
- Bereitstellen von Lese- und nonread Berichten.
    
- Eingehende und ausgehende Nachrichten�bermittlungen zulassen.
    
- Erm�glicht die Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.
    
- Unterst�tzung f�r benannte und mehrwertige Eigenschaften.
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- Supporting associated contents tables. For more information, see [Inhalt von Tabellen](contents-tables.md).
    
- Benachrichtigung �ber die Warteschlange MAPI-Unterst�tzung f�r Nachrichten in der Warteschlange f�r ausgehende Nachrichten vorhanden sind.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

