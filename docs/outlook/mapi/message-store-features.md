---
title: Nachrichten-Store-Features
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439520"
---
# <a name="message-store-features"></a>Nachrichten-Store-Features

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter sind komplexer als andere MAPI-Dienstanbieter in diesem Nachrichtenspeicheranbieter verfügen über eine größere Palette optionaler Features, die sie implementieren können. Die Liste der erforderlichen Features für einen Nachrichtenspeicheranbieter ist relativ kurz. Ein typischer Nachrichtenspeicheranbieter unterstützt jedoch eine Reihe optionaler Features, da viele der optionalen Features sehr nützlich oder für die meisten MAPI-Clients erforderlich sind. In der folgenden Tabelle sind die wichtigsten Features aufgeführt, die Nachrichtenspeicheranbieter implementieren können, und ob jedes Feature für alle Nachrichtenspeicheranbieter und für Standardnachrichtenspeicheranbieter erforderlich oder optional ist.
  
|**Feature**|**All**|**Default**|
|:-----|:-----|:-----|
|Bereitstellen des Status mit der MAPI-Statustabelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Ordnerobjekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Nachrichtenobjekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen von Lese- und nonread Berichten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen einer Statusschnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen einer Konfigurationsschnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Unterstützung zugeordneter Inhaltstabellen für die Unterstützung von Formularen und Anzeigen.  <br/> |Optional  <br/> |Optional  <br/> |
|Senden von Nachrichten mit dem Nachrichtenspeicheranbieter.  <br/> |Optional.  <br/> |Erforderlich  <br/> |
|Empfangen von Nachrichten mit dem Nachrichtenspeicheranbieter.  <br/> |Optional.  <br/> |Erforderlich  <br/> |
|Unterstützen von Nachrichtenanlagen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung des Rich-Text-Formats für Nachrichten.  <br/> |Optional  <br/> |Optional  <br/> |
|Bereitstellen von Benachrichtigungen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützen von Suchen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung von eng gekoppelten Nachrichtenspeicher-/Transportanbietern.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung der Nichtwiederverwendung von Eintragsbezeichnern.  <br/> |Optional  <br/> |Optional  <br/> |
   
Viele der optionalen Features können MAPI- und Clientanwendungen angekündigt werden, indem sie verschiedene Flags in der PR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft des **Nachrichtenspeicherobjekts** festlegen. Den erforderlichen Features sind keine Kennzeichen zugeordnet. **PR_STORE_SUPPORT_MASK** für Nachrichtenspeicher, Ordner und Nachrichtenobjekte erforderlich. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

