---
title: Nachrichtenspeicherfunktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e99d9d2e1289ed98ba659e97b05c8ea6d891a74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581811"
---
# <a name="message-store-features"></a>Nachrichtenspeicherfunktionen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Nachricht Anbieter sind komplexer als andere MAPI-Dienstanbieter in diesem Anbieter Nachricht einen größeren Bereich von optionale Features, die sie implementieren können. Die Liste der erforderlichen Features für eine Nachricht Speicheranbieter ist relativ kurz. Eine typische Nachricht Speicheranbieter unterstützt eine Reihe von optionalen Features jedoch, da viele der optionalen Features sehr nützlich oder von den meisten MAPI-Clients erforderlich sind. Die folgende Tabelle enthält die wichtigsten Features, dass Nachricht Anbieter implementieren können und speichern Anbieter und für Standardnachricht speichern-Anbieter, ob jedes Feature erforderlich oder optional für alle Nachricht ist.
  
|**Funktion**|**All**|**Standard**|
|:-----|:-----|:-----|
|Status Bereitstellen der MAPI-Statustabelle.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Implementieren von Folder-Objekten.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Implementieren von Message-Objekten.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Bereitstellen von Lese- und nonread Berichten.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Bereitstellen einer Schnittstelle ausgeführt.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Eine Konfigurationsschnittstelle bereit.  <br/> |Eingabe erforderlich  <br/> |Eingabe erforderlich  <br/> |
|Hilfstabellen zugeordneten Inhalt für Formular- und Support.  <br/> |Optional  <br/> |Optional  <br/> |
|Sendende von Nachrichten mit der Meldung Speicheranbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Empfangen von Nachrichten mit dem Message-Speicher-Anbieter.  <br/> |Optional  <br/> |Erforderlich  <br/> |
|Unterstützung von e-Mail-Anlagen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung für Rich-Text-Format für Nachrichten.  <br/> |Optional  <br/> |Optional  <br/> |
|Bereitstellen von Benachrichtigungen.  <br/> |Optional  <br/> |Optional  <br/> |
|Suchen Sie unterstützen.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung von eng gekoppelt Nachricht Store-Transport-Anbieter.  <br/> |Optional  <br/> |Optional  <br/> |
|Unterstützung für nicht-Wiederverwendung von Eintragsbezeichner.  <br/> |Optional  <br/> |Optional  <br/> |
   
Viele der optionale Features können angekündigt, MAPI und Clientanwendungen durch Festlegen verschiedener Flags in der Nachricht speichern-Eigenschaft des Objekts **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Die erforderlichen Features müssen keine Flags zugeordnet. **PR_STORE_SUPPORT_MASK** muss auf Nachrichtenspeicher, Ordner und Message-Objekten. 
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

