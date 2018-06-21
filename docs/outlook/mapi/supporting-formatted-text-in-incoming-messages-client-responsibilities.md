---
title: Unterstützung von formatierten Text in eingehenden Nachrichten Client Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19795669"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Unterstützung von formatierten Text in eingehenden Nachrichten: Client Zuständigkeiten

  
  
**Betrifft**: Outlook 
  
Wie Nachrichten zwischen messaging-Systemen übertragen werden, wird die MAPI-Warteschlange sichergestellt, dass die rich-Text-Formatierung mit den Nachrichtentext synchronisiert bleibt. Die MAPI-Warteschlange Ruft die [RTFSync](rtfsync.md) -Funktion aus einer gepackten Version der Nachricht, die an der Adressbuchhierarchie übergeben. Der Adressbuchhierarchie speichert die Änderungen an der Nachricht durch Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode ab und leitet sie an den neuen Empfänger. 
  
Wenn RTF-fähigen Clientanwendung der Empfänger die Nachricht für die Textanzeige geöffnet wird, müssen sie den Text mit der Formatierung synchronisieren und öffnen **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , je nachdem, welche Eigenschaft verfügbar ist.
  
 **Öffnen eine Nachricht, RTF-fähigen clients**
  
1. Rufen Sie **RTFSync** zum Synchronisieren von des Nachrichtentexts mit der Formatierung an, wenn der Nachrichtenspeicher nicht RTF-kompatibel ist. Das Flag RTF_SYNC_BODY_CHANGED sollte im _UlFlags_ -Parameter übergeben werden, wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))-Eigenschaft ist nicht vorhanden, oder auf FALSE festgelegt. Arbeiten mit RTF-fähigen Nachrichtenspeicher Clients müssen nicht die **RTFSync** aufrufen, da der Nachrichtenspeicher davon kümmert. 
    
2. Rufen Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , wenn der Nachrichtentext aktualisiert wurde. 
    
3. Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie die Eigenschaft **PR_BODY** stattdessen öffnen, um den Nachrichteninhalt anzuzeigen. 
    
4. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion, um eine nicht komprimierten Version der komprimierten RTF-Daten zu erstellen, falls verfügbar. 
    
5. Der nicht komprimierten RTF-Daten oder die nur-Text-Daten für den Benutzer anzuzeigen.
    
 **RTFSync** gibt einen booleschen Wert, der angibt, ob die Nachricht wurde aktualisiert. Wenn dieser Wert "true" zurückgibt, rufen Sie **SaveChanges** zu einem bestimmten Zeitpunkt an das Update dauerhaft entfernt wird. Der Anruf hat keinen getroffen werden, unmittelbar nachdem **RTFSync** zurückgegeben. 
  
> [!NOTE]
> Da so viele Komponenten den formatierten Text behandelt werden, bevor Sie es erhalten, besteht die Möglichkeit, eine Beschädigung. Diese Beschädigung konnte der Informationsdienst Nachricht, einer Drittanbieter-Anwendung, ein Gateway oder ein Fehler bei der Übertragung stammen. 
  

