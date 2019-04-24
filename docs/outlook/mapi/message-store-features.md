---
title: Nachrichtenspeicher Features
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356903"
---
# <a name="message-store-features"></a>Nachrichtenspeicher Features

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter sind komplexer als andere MAPI-Dienstanbieter, da Nachrichtenspeicher Anbieter über eine breitere Auswahl von Features verfügen, die Sie implementieren können. Die Liste der erforderlichen Funktionen für einen Nachrichtenspeicher Anbieter ist relativ kurz. Ein typischer Nachrichtenspeicher Anbieter unterstützt jedoch eine Reihe von optionalen Features, da viele der optionalen Features für die meisten MAPI-Clients sehr nützlich oder erforderlich sind. In der folgenden Tabelle sind die wichtigsten Features aufgeführt, die von Nachrichtenspeicher Anbietern implementiert werden können, und die Angabe, ob jedes Feature für alle Nachrichtenspeicher Anbieter und für standardmäßige Nachrichtenspeicher Anbieter erforderlich oder optional ist.
  
|**Feature**|**All**|**Default**|
|:-----|:-----|:-----|
|Status wird mit der MAPI-Statustabelle bereitgestellt.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Folder-Objekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Implementieren von Message-Objekten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstellen von Lese- und nonread Berichten.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstelleneiner Fortschritts Schnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Bereitstelleneiner Konfigurationsschnittstelle.  <br/> |Erforderlich  <br/> |Erforderlich  <br/> |
|Unterstützen von Tabellen für verknüpfte Inhalte für Formular-und Ansichts Unterstützung.  <br/> |Optional  <br/> |Optional  <br/> |
|Senden von Nachrichten mit dem Nachrichtenspeicher Anbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Empfangen von Nachrichten mit dem Nachrichtenspeicher Anbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Unterstützen von Nachrichtenanlagen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung des Rich-Text-Formats für Nachrichten.  <br/> |Optional  <br/> |Optional  <br/> |
|Bereitstellen von Benachrichtigungen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützen von Suchvorgängen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung eng gekoppelter Nachrichtenspeicher/Transportanbieter.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung der nicht Wiederverwendung von Eintrags-IDs.  <br/> |Optional  <br/> |Optional  <br/> |
   
Viele der optionalen Features können MAPI-und Clientanwendungen angekündigt werden, indem verschiedene Flags in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts festgelegt werden. Den erforderlichen Features sind keine Flags zugeordnet. **PR_STORE_SUPPORT_MASK** ist für Nachrichtenspeicher-, Ordner-und Nachrichtenobjekte erforderlich. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

