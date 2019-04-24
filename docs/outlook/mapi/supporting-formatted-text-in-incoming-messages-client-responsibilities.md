---
title: Unterstützung von formatiertem Text in eingehenden Nachrichten Client Verantwortlichkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327412"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Unterstützung von formatiertem Text in eingehenden Nachrichten: Aufgaben des Kunden

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei der Übertragung von Nachrichten zwischen Messagingsystemen stellt der MAPI-Spooler sicher, dass die Rich-Text-Formatierung mit dem Nachrichtentext synchronisiert bleibt. Der MAPI-Spooler Ruft die [RTFSync](rtfsync.md) -Funktion innerhalb einer eingebundenen Version der Nachricht auf, die an den Transportanbieter übergeben wird. Der Transportanbieter speichert die an der Nachricht vorgenommenen Änderungen durch Aufrufen der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode und leitet Sie an den neuen Empfänger weiter. 
  
Wenn die RTF-fähige Clientanwendung des Empfängers die Nachricht öffnet, um den Text anzuzeigen, muss Sie den Text mit der Formatierung synchronisieren und entweder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) öffnen. , je nachdem, welche Eigenschaft verfügbar ist.
  
 **So öffnen Sie eine Nachricht: RTF-fähige Clients**
  
1. Rufen Sie **RTFSync** auf, um den Nachrichtentext mit der Formatierung zu synchronisieren, wenn der Nachrichtenspeicher nicht RTF-fähig ist. Das RTF_SYNC_BODY_CHANGED-Flag sollte im _ulFlags_ -Parameter übergeben werden, wenn die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft fehlt oder auf false festgelegt ist. Bei Clients, die mit RTF-fähigen Nachrichten speichern arbeiten, muss der **RTFSync** -Aufruf nicht ausgeführt werden, da der Nachrichtenspeicher dafür sorgt. 
    
2. Rufen Sie [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) auf, wenn der Nachrichtentext aktualisiert wurde. 
    
3. Rufen Sie [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen. Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie stattdessen die **PR_BODY** -Eigenschaft öffnen, um den Nachrichteninhalt anzuzeigen. 
    
4. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion auf, um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar. 
    
5. Zeigt die nicht komprimierten RTF-Daten oder die nur-Text-Daten für den Benutzer an.
    
 **RTFSync** gibt einen booleschen Wert zurück, der angibt, ob die Nachricht aktualisiert wurde. Wenn dieser Wert TRUE zurückgibt, **** rufen Sie SaveChanges an einem bestimmten Punkt auf, um die Aktualisierung dauerhaft zu machen. Der Aufruf muss nicht unmittelbar nach **RTFSync** zurückgegeben werden. 
  
> [!NOTE]
> Da so viele Komponenten den formatierten Text verarbeiten, bevor Sie ihn erhalten, besteht die Möglichkeit einer Beschädigung. Diese Beschädigung kann vom Nachrichtenspeicher Anbieter, einer Drittanbieteranwendung, einem Gateway oder einem Übertragungsfehler verursacht werden. 
  

