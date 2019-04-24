---
title: Unterstützen von Nachrichtenanlagen für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350624"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>Unterstützen von Nachrichtenanlagen für Nachrichtenspeicher Anbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Nachrichtenspeicher Anbieter muss keine Nachrichtenanlagen unterstützen. Viele Clientanwendungen erwarten jedoch, dass Sie Anlagen zu Nachrichten hinzufügen können. Wenn der Nachrichtenspeicher zum Erstellen oder Speichern von IPM verwendet wird. Hinweis Nachrichten, dann sollten Sie Nachrichtenanlagen unterstützen. Standardmäßige Nachrichtenspeicher Anbieter sollten auch Nachrichtenanlagen unterstützen. Weitere Informationen finden Sie unter [MAPI-Nachrichtenklassen](mapi-message-classes.md)und [Standardnachrichtenspeicher](default-message-stores.md).
  
Es gibt fünf Typen von Anlagen, die von MAPI unterstützt werden: Dateianhänge, Daten Anlagen, Nachrichtenanlagen, OLE-Objekt Anlagen und Links. Die Anforderungen für die Unterstützung der einzelnen Typen sind unterschiedlich. Clients unterscheiden zwischen den beiden Typen von Anlagen mithilfe der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft für Attachment-Objekte.
  
Unterstützende Anlagen beinhaltet die Implementierung der [IAttach: IMAPIProp](iattachimapiprop.md) -Schnittstelle. Die **IAttach** -Schnittstelle verfügt über keine eigenen Methoden; Es verfügt nur über Methoden, die von der [IMAPIProp](imapipropiunknown.md) -Schnittstelle geerbt werden. Da der Nachrichtenspeicher Anbietereigenschaften für Nachrichtenobjekte bereits implementieren muss, vereinfacht dies die Unterstützung von Anlagen erheblich. Die Implementierung von **IAttach** bedeutet im Grunde eine Möglichkeit für Clients, auf eine Tabelle mit Eigenschaften für bestimmte Anlagen für Nachrichten zuzugreifen. 
  
Bei Daten Anlagen handelt es sich lediglich um Anlagen, für die der Inhalt der Anlage direkt in der **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage gespeichert wird. Daten Anlagen sind hauptsächlich vorhanden, um Clients das Anfügen von Dateien an eine Nachricht zu gestatten, wenn der Absender und der Empfänger der Nachricht keinen Zugriff auf einen gemeinsamen Dateiserver haben. Weitere Informationen finden Sie unter der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft.
  
Nachrichtenanlagen sind Anlagen, für die das Attachment-Unterobjekt ein weiteres [IMessage: mapiProp](imessageimapiprop.md) -Objekt ist. Da Nachrichtenspeicher Anbieter die **IMessage** -Schnittstelle bereits unterstützen, ist das unterstützen von Nachrichtenanlagen nicht schwierig. 
  
Die Unterstützung von OLE-Objekt Anlagen beinhaltet die Implementierung der OLE- **IStorage**-, **IStream**-und **IStreamDocfile** -Schnittstellen. Der Nachrichtenspeicher Anbieter muss in der Lage sein, in der Nachricht gespeicherte OLE-Objektdaten in ein aktives OLE-Objekt umzuwandeln, wenn ein Client das Objekt öffnet. 
  
Links gibt es in zwei Arten: Links zu Dateien und Links zu anderen Nachrichten. Links zu Dateien verwenden Sie den ATTACH_BY_REF_ONLY-Wert für die **PR_ATTACH_METHOD** -Eigenschaft zusammen mit **PR_ATTACH_PATHNAME** ([pidtagattachpathname (](pidtagattachpathname-canonical-property.md)) oder **PR_ATTACH_LONG_PATHNAME** ([pidtagattachlongpathname (](pidtagattachlongpathname-canonical-property.md)), um anzugeben der Speicherort einer Datei.
  
Die Implementierung von Links zu Nachrichten kann von Aspekten des lokalen Messagingsystems abhängig sein und kann daher nicht vollständig dokumentiert werden. Wenn Sie beispielsweise einen Link zu einer Nachricht senden, die in einem Server basierten Nachrichtenspeicher gespeichert ist, ist es in der Regel nur eine Frage des Sendens der Eintrags-ID der verknüpften Nachricht, wobei der Absender und der Empfänger Zugriff auf diesen Server haben. Andere Messagingsystem Konfigurationen stellen andere Anforderungen und Herausforderungen für die Implementierung von Links zu Nachrichten dar.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

