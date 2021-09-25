---
title: Nachrichten-Store-Features
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0fe0e9d4e64659f09d314731e72b0048177e8fa8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551100"
---
# <a name="message-store-features"></a>Nachrichten-Store-Features

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter sind komplexer als andere MAPI-Dienstanbieter, da Nachrichtenspeicheranbieter über eine größere Palette optionaler Features verfügen, die sie implementieren können. Die Liste der erforderlichen Features für einen Nachrichtenspeicheranbieter ist relativ kurz. Ein typischer Nachrichtenspeicheranbieter unterstützt jedoch eine Reihe optionaler Features, da viele der optionalen Features für die meisten MAPI-Clients sehr nützlich oder erforderlich sind. In der folgenden Tabelle sind die wichtigsten Features aufgeführt, die Nachrichtenspeicheranbieter implementieren können, und ob jedes Feature für alle Nachrichtenspeicheranbieter und für Standardnachrichtenspeicheranbieter erforderlich oder optional ist.
  
|**Feature**|**All**|**Default**|
|:-----|:-----|:-----|
|Bereitstellen des Status mit der MAPI-Statustabelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Ordnerobjekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Nachrichtenobjekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen von Lese- und nonread Berichten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen einer Statusschnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen einer Konfigurationsschnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Unterstützen zugeordneter Inhaltstabellen für die Unterstützung von Formularen und Ansichten.  <br/> |Optional  <br/> |Optional  <br/> |
|Senden von Nachrichten mit dem Nachrichtenspeicheranbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Empfangen von Nachrichten beim Nachrichtenspeicheranbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Unterstützen von Nachrichtenanlagen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung des Rich-Text-Formats für Nachrichten.  <br/> |Optional  <br/> |Optional  <br/> |
|Bereitstellen von Benachrichtigungen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützen von Suchvorgängen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung eng gekoppelter Nachrichtenspeicher-/Transportanbieter.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung der Nichtwiederverwendung von Eintragsbezeichnern.  <br/> |Optional  <br/> |Optional  <br/> |
   
Viele der optionalen Features können MAPI- und Clientanwendungen durch Festlegen verschiedener Flags in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Nachrichtenspeicherobjekts angekündigt werden. Den erforderlichen Features sind keine Flags zugeordnet. PR_STORE_SUPPORT_MASK ist für Nachrichtenspeicher-, **Ordner-** und Nachrichtenobjekte erforderlich. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

