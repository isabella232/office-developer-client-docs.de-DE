---
title: Unterstützen von formatierten Text in Clientaufgaben für eingehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434501"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Unterstützen von formatierten Text in eingehenden Nachrichten: Clientzu zuständigkeiten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Nachrichten zwischen Messagingsystemen übertragen werden, stellt der MAPI-Spooler sicher, dass die Rich-Text-Formatierung mit dem Nachrichtentext synchronisiert bleibt. Der MAPI-Spooler ruft die [RTFSync-Funktion](rtfsync.md) innerhalb einer umschlossenen Version der Nachricht auf, die er an den Transportanbieter übergibt. Der Transportanbieter speichert die an der Nachricht vorgenommenen Änderungen, indem er die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aufruft und diese dann an den neuen Empfänger weiter leitet. 
  
Wenn die **#A0** des Empfängers die Nachricht zum Anzeigen des Texts öffnet, muss sie den Text mit der Formatierung synchronisieren und entweder PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) öffnen, je nachdem, welche Eigenschaft verfügbar ist.
  
 **Um eine Nachricht zu öffnen, verwenden RTF-bewusste Clients**
  
1. Rufen **Sie RTFSync** auf, um den Nachrichtentext mit der Formatierung zu synchronisieren, wenn der Nachrichtenspeicher nicht RTF-bewusst ist. Das RTF_SYNC_BODY_CHANGED sollte im  _ulFlags-Parameter_ übergeben werden, wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) -Eigenschaft fehlt oder auf FALSE festgelegt ist. Clients, die mit RTF-benachrichtigungsspeichern arbeiten, müssen den **RTFSync-Aufruf** nicht senden, da der Nachrichtenspeicher ihn übernimmt. 
    
2. Rufen [Sie IMAPIProp::SaveChanges auf,](imapiprop-savechanges.md) wenn der Nachrichtentext aktualisiert wurde. 
    
3. Rufen [Sie IMAPIProp::OpenProperty auf,](imapiprop-openproperty.md) um die **PR_RTF_COMPRESSED** öffnen. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie die **PR_BODY** öffnen, um den Nachrichteninhalt anzuzeigen. 
    
4. Rufen Sie [die WrapCompressedRTFStream-Funktion auf,](wrapcompressedrtfstream.md) um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar. 
    
5. Zeigen Sie dem Benutzer die nicht komprimierten RTF-Daten oder die Nur-Text-Daten an.
    
 **RTFSync** gibt einen booleschen Wert zurück, der angibt, ob die Nachricht aktualisiert wurde. Wenn dieser Wert TRUE zurückgibt, rufen **Sie SaveChanges** an einem bestimmten Punkt auf, um das Update dauerhaft zu machen. Der Aufruf muss nicht unmittelbar nach der Rückgabe von **RTFSync** vorgenommen werden. 
  
> [!NOTE]
> Da so viele Komponenten den formatierten Text verarbeiten, bevor Sie ihn erhalten, besteht die Möglichkeit einer Beschädigung. Diese Beschädigung kann vom Nachrichtenspeicheranbieter, einer Drittanbieteranwendung, einem Gateway oder einem Übertragungsfehler stammen. 
  

