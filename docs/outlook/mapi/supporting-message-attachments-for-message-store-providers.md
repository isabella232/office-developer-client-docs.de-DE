---
title: Unterstützen von Nachrichtenanlagen für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: a94d1230f4f26d080976fd15768bdfeb6ea04748
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576099"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Unterstützen von Nachrichtenanlagen für Nachrichtenspeicheranbieter

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ihre Nachricht Speicheranbieter muss nicht zur Unterstützung von e-Mail-Anlagen. Erwarten jedoch viele Clientanwendungen Anlagen zu Nachrichten hinzufügen können. Wenn Ihre Nachrichtenspeicher zum Erstellen oder IPM Speichern verwendet wird. Beachten Sie Nachrichten, und klicken Sie dann Sie e-Mail-Anlagen unterstützen soll. Standard-Nachricht Anbieter sollten auch e-Mail-Anlagen unterstützen. Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md)und [Nachrichtenspeicher Standard](default-message-stores.md).
  
Es gibt fünf Typen von Anlagen, die MAPI unterstützt: file, Anlagen, Daten Anlagen, e-Mail-Anlagen, OLE-Objekt-Anlagen und Links. Die Anforderungen für die Unterstützung von jedem Typ unterscheiden. Clients unterscheiden zwischen den beiden Typen von Anlagen mit der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft auf Attachment-Objekte.
  
Unterstützung von Anlagen bedeutet die Implementierung der [IAttach: IMAPIProp](iattachimapiprop.md) Schnittstelle. Die Schnittstelle **IAttach** verfügt über keine Methoden eigenen; Es hat nur Methoden, die von der Schnittstelle [IMAPIProp](imapipropiunknown.md) vererbt werden. Da Ihre Nachricht Speicheranbieter Eigenschaften für Nachrichtenobjekte bereits implementiert werden muss, vereinfacht dies das erheblich Unterstützung für Anlagen. Implementieren **IAttach** im Wesentlichen bedeutet das Bereitstellen der Möglichkeit für Clients Zugriff auf eine Tabelle von Eigenschaften für die Anlagen auf Nachrichten. 
  
Daten Anlagen sind einfach Anlagen, die den Inhalt der Anlage direkt in eine Anlage **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft gespeichert werden. Daten Anlagen vorhanden und kann in erster Linie damit Clients So fügen Sie Dateien auf eine Nachricht an, wenn der Absender und Empfänger der Nachricht nicht über Zugriff auf einen gemeinsamen Dateiserver verfügen. Weitere Informationen finden Sie unter der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft.
  
E-Mail-Anlagen sind für die das-Unterobjekt Anlage eine andere ist Anlagen [IMessage: ' mapiProp '](imessageimapiprop.md) Objekt. Da Nachricht Anbieter bereits die **IMessage** -Schnittstelle unterstützt, ist die Unterstützung von e-Mail-Anlagen nicht schwierig. 
  
OLE-Objekt Anlagen unterstützen bedeutet, dass die OLE- **IStorage** **IStream**und **IStreamDocfile** Schnittstellen implementieren. Ihre Nachricht Speicheranbieter muss möglicherweise konvertieren OLE-Objektdaten in der Nachricht in einer aktiven OLE-Objekt gespeichert wird, wenn ein Client das Objekt geöffnet wird. 
  
Links gibt zwei Arten: Links zu Dateien und Links zu anderen Nachrichten. Links zu Dateien mithilfe den ATTACH_BY_REF_ONLY-Wert für die **PR_ATTACH_METHOD** -Eigenschaft zusammen mit **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) an die Position einer Datei.
  
Eine Implementierung von Links zu Nachrichten möglicherweise hängen Aspekte des lokalen Messagingsystem bereit und, daher kann nicht vollständig dokumentiert werden hier. Senden eine Verknüpfung mit einer Meldung, die auf einem Server-basierten Nachrichtenspeicher gespeichert ist ist beispielsweise in der Regel nur darum, die Eintrags-ID der verknüpften Nachricht, vorausgesetzt, dass Absender und Empfänger Zugriff auf diesem Server haben zu senden. Andere messaging Systemkonfigurationen-Präsentation vor anderen Anforderungen und Herausforderungen für die Implementierung von Links zu Nachrichten.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

