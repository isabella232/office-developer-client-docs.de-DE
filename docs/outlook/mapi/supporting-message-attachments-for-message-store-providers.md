---
title: Unterstützen von Nachrichtenanlagen für Store Anbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412135"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Unterstützen von Nachrichtenanlagen für Store Anbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihr Nachrichtenspeicheranbieter muss Keine Nachrichtenanlagen unterstützen. Viele Clientanwendungen erwarten jedoch, dass sie Anlagen zu Nachrichten hinzufügen können. Wenn Ihr Nachrichtenspeicher zum Erstellen oder Speichern von IPM verwendet wird. Notieren Sie nachrichten, dann sollten Sie Nachrichtenanlagen unterstützen. Standardmäßige Nachrichtenspeicheranbieter sollten auch Nachrichtenanlagen unterstützen. Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md)und [Default Message Stores](default-message-stores.md).
  
MapI unterstützt fünf Arten von Anlagen: Dateianlagen, Datenanlagen, Nachrichtenanlagen, OLE-Objektanlagen und Links. Die Anforderungen für die Unterstützung der einzelnen Typen sind unterschiedlich. Clients unterscheiden zwischen den beiden Anlagentypen durch die **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft für Anlagenobjekte.
  
Die Unterstützung von Anlagen bedeutet, [die IAttach : IMAPIProp-Schnittstelle zu](iattachimapiprop.md) implementieren. Die **IAttach-Schnittstelle** verfügt über keine eigenen Methoden. Es gibt nur Methoden, die von der [IMAPIProp-Schnittstelle geerbt](imapipropiunknown.md) werden. Da Ihr Nachrichtenspeicheranbieter bereits Eigenschaften für Nachrichtenobjekte implementieren muss, vereinfacht dies die Unterstützung von Anlagen erheblich. Die **Implementierung von IAttach** bedeutet im Wesentlichen, clients den Zugriff auf eine Tabelle mit Eigenschaften für bestimmte Anlagen für Nachrichten zu bieten. 
  
Datenanlagen sind einfach Anlagen, für die der Inhalt der Anlage direkt in der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft einer Anlage gespeichert wird. Datenanlagen sind in erster Linie vorhanden, um Clients das Anfügen von Dateien an eine Nachricht zu ermöglichen, wenn der Absender und der Empfänger der Nachricht keinen Zugriff auf einen gemeinsamen Dateiserver haben. Weitere Informationen finden Sie unter **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) -Eigenschaft.
  
Nachrichtenanlagen sind Anlagen, bei denen das Anlagenunterobjekt ein anderes [IMessage : MAPIProp-Objekt](imessageimapiprop.md) ist. Da Nachrichtenspeicheranbieter bereits die **IMessage-Schnittstelle** unterstützen, ist die Unterstützung von Nachrichtenanlagen nicht schwierig. 
  
Die Unterstützung von OLE-Objektanlagen bedeutet, die OLE **IStorage-,** **IStream-** und **IStreamDocfile-Schnittstellen zu** implementieren. Ihr Nachrichtenspeicheranbieter muss in der Lage sein, in der Nachricht gespeicherte OLE-Objektdaten in ein aktives OLE-Objekt zu konvertieren, wenn ein Client das Objekt öffnet. 
  
Links gibt es in zwei Typen: Links zu Dateien und Links zu anderen Nachrichten. Links zu Dateien verwenden den ATTACH_BY_REF_ONLY-Wert für die **PR_ATTACH_METHOD-Eigenschaft** zusammen mit **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)), um den Speicherort einer Datei anzugeben.
  
Die Implementierung von Links zu Nachrichten hängt möglicherweise von Aspekten des lokalen Messagingsystems ab und kann daher hier nicht vollständig dokumentiert werden. Beispielsweise ist das Senden eines Links zu einer Nachricht, die in einem serverbasierten Nachrichtenspeicher gespeichert ist, in der Regel nur eine Frage des Sendens der Eintrags-ID der verknüpften Nachricht, vorausgesetzt, dass sowohl der Absender als auch der Empfänger Zugriff auf diesen Server haben. Andere Messagingsystemkonfigurationen stellen andere Anforderungen und Herausforderungen für die Implementierung von Links zu Nachrichten dar.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

