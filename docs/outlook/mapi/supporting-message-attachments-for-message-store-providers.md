---
title: Unterstützen von Nachrichtenanlagen für Nachrichtenanbieter Store
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: b7b71a55a334ef763fa9c9117b0b218b585d87df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619666"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Unterstützen von Nachrichtenanlagen für Nachrichtenanbieter Store

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihr Nachrichtenspeicheranbieter muss Nachrichtenanlagen nicht unterstützen. Viele Clientanwendungen erwarten jedoch, dass Nachrichten Anlagen hinzugefügt werden können. Wenn Ihr Nachrichtenspeicher zum Erstellen oder Speichern von IPM verwendet wird. Notieren Sie sich Nachrichten, dann sollten Sie Nachrichtenanlagen unterstützen. Standardmäßige Nachrichtenspeicheranbieter sollten auch Nachrichtenanlagen unterstützen. Weitere Informationen finden Sie unter [MAPI-Nachrichtenklassen](mapi-message-classes.md)und [Standardnachrichtenspeicher.](default-message-stores.md)
  
MapI unterstützt fünf Arten von Anlagen: Dateianlagen, Datenanlagen, Nachrichtenanlagen, OLE-Objektanlagen und Verknüpfungen. Die Anforderungen für die Unterstützung der einzelnen Typen sind unterschiedlich. Clients unterscheiden zwischen den beiden Arten von Anlagen anhand der **eigenschaft PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) für Anlagenobjekte.
  
Das Unterstützen von Anlagen bedeutet, dass die [IAttach : IMAPIProp-Schnittstelle](iattachimapiprop.md) implementiert wird. Die **IAttach-Schnittstelle** verfügt über keine eigenen Methoden. Es verfügt nur über Methoden, die von der [IMAPIProp-Schnittstelle](imapipropiunknown.md) geerbt werden. Da Ihr Nachrichtenspeicheranbieter bereits Eigenschaften für Nachrichtenobjekte implementieren muss, vereinfacht dies die Unterstützung von Anlagen erheblich. Das Implementieren von **IAttach** bedeutet im Wesentlichen, dass Clients auf eine Tabelle mit Eigenschaften für bestimmte Anlagen in Nachrichten zugreifen können. 
  
Datenanlagen sind einfach Anlagen, für die der Inhalt der Anlage direkt in der **eigenschaft PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) einer Anlage gespeichert wird. Datenanlagen dienen in erster Linie dazu, Clients das Anfügen von Dateien an eine Nachricht zu ermöglichen, wenn der Absender und der Empfänger der Nachricht keinen Zugriff auf einen gemeinsamen Dateiserver haben. Weitere Informationen finden Sie in der **Eigenschaft PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
  
Nachrichtenanlagen sind Anlagen, für die das Anlagenunterobjekt eine weitere [IMessage ist: MAPIProp-Objekt.](imessageimapiprop.md) Da Nachrichtenspeicheranbieter die **IMessage-Schnittstelle** bereits unterstützen, ist das Unterstützen von Nachrichtenanlagen nicht schwierig. 
  
Das Unterstützen von OLE-Objektanlagen bedeutet, dass die **OLE-IStorage-,** **IStream-** und **IStreamDocfile-Schnittstellen** implementiert werden. Ihr Nachrichtenspeicheranbieter muss in der Lage sein, in der Nachricht gespeicherte OLE-Objektdaten in ein aktives OLE-Objekt zu konvertieren, wenn ein Client das Objekt öffnet. 
  
Links werden in zwei Typen angezeigt: Links zu Dateien und Links zu anderen Nachrichten. Links zu Dateien verwenden den ATTACH_BY_REF_ONLY-Wert für die **PR_ATTACH_METHOD-Eigenschaft** zusammen mit **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)), um den Speicherort einer Datei anzugeben.
  
Wie Links zu Nachrichten implementiert werden, hängt möglicherweise von Aspekten des lokalen Messagingsystems ab und kann daher hier nicht vollständig dokumentiert werden. Beispielsweise ist das Senden eines Links zu einer Nachricht, die in einem serverbasierten Nachrichtenspeicher gespeichert ist, in der Regel nur eine Frage des Sendens der Eintrags-ID der verknüpften Nachricht, vorausgesetzt, dass sowohl der Absender als auch der Empfänger Zugriff auf diesen Server haben. Andere Konfigurationen des Messagingsystems stellen andere Anforderungen und Herausforderungen bei der Implementierung von Links zu Nachrichten dar.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

