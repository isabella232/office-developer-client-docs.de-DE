---
title: Unterstützen von formatiertem Text in Den Zuständigkeiten des Clients für eingehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 36dc6390fcb3ef7e8d3acc2141fe39a4ae2c3518
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624146"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Unterstützen von formatiertem Text in eingehenden Nachrichten: Verantwortlichkeiten des Clients

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Nachrichten zwischen Messagingsystemen übertragen werden, stellt der MAPI-Spooler sicher, dass die Rich-Text-Formatierung mit dem Nachrichtentext synchronisiert bleibt. Der MAPI-Spooler ruft die [RTFSync-Funktion](rtfsync.md) in einer umschlossenen Version der Nachricht auf, die sie an den Transportanbieter übergibt. Der Transportanbieter speichert die an der Nachricht vorgenommenen Änderungen durch Aufrufen der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) und leitet sie dann an den neuen Empfänger weiter. 
  
Wenn die RTF-fähige Clientanwendung des Empfängers die Nachricht öffnet, um den Text anzuzeigen, muss sie den Text mit der Formatierung synchronisieren und entweder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) öffnen, je nachdem, welche Eigenschaft verfügbar ist.
  
 **RtF-fähige Clients zum Öffnen einer Nachricht**
  
1. Rufen Sie **RTFSync** auf, um den Nachrichtentext mit der Formatierung zu synchronisieren, wenn der Nachrichtenspeicher nicht RTF-fähig ist. The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE. Clients, die mit RTF-fähigen Nachrichtenspeichern arbeiten, müssen den **RTFSync-Aufruf** nicht durchführen, da sich der Nachrichtenspeicher darum kümmert. 
    
2. Rufen Sie [IMAPIProp::SaveChanges auf,](imapiprop-savechanges.md) wenn der Nachrichtentext aktualisiert wurde. 
    
3. Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie stattdessen die **eigenschaft PR_BODY** öffnen, um den Nachrichteninhalt anzuzeigen. 
    
4. Rufen Sie die [WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, falls verfügbar. 
    
5. Zeigt dem Benutzer die nicht komprimierten RTF-Daten oder nur-Text-Daten an.
    
 **RTFSync** gibt einen booleschen Wert zurück, der angibt, ob die Nachricht aktualisiert wurde. Wenn dieser Wert TRUE zurückgibt, rufen **Sie SaveChanges** zu einem bestimmten Zeitpunkt auf, um das Update dauerhaft zu machen. Der Aufruf muss nicht unmittelbar nach der Rückgabe von **RTFSync** ausgeführt werden. 
  
> [!NOTE]
> Da so viele Komponenten den formatierten Text verarbeiten, bevor Sie ihn erhalten, besteht die Möglichkeit einer Beschädigung. Diese Beschädigung kann vom Nachrichtenspeicheranbieter, einer Drittanbieteranwendung, einem Gateway oder einem Übertragungsfehler verursacht werden. 
  

