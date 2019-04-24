---
title: Nachverfolgen von Unterhaltungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349546"
---
# <a name="tracking-conversations"></a>Nachverfolgen von Unterhaltungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Nachverfolgen von Unterhaltungen handelt es sich um das Erfassen von Antworten auf eine Nachricht. Clients sollten zwei Eigenschaften festlegen, die bei der Nachverfolgung von Nachrichten behilflich sind:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** ist der standardisierte Betreff der Nachricht, der Betreff ohne die Präfixzeichenfolgen. Legen Sie diese Eigenschaft auf den Wert der **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft der Nachricht fest. 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI. 
    
 **ScCreateConversationIndex** generiert den Wert eines Indexes Unterhaltung f�r alle ausgehenden Nachrichten. **ScCreateConversationIndex** implementiert den Index als ein Kopfzeilen-Baustein, die 22 Bytes L�nge, gefolgt von NULL ist oder mehrere untergeordnete blockiert jede 5 Bytes L�nge. 
  
Kopfzeilen-Baustein besteht aus 22 Bytes in drei Abschnitte unterteilt:
  
- Ein reserviertes Byte. Der Wert ist 1.
    
- F�nf Bytes f�r die aktuelle Systemzeit in der Struktur [FILETIME](filetime.md) -Format konvertiert. 
    
- Sechzehn Bytes gedr�ckt halten, eine [GUID](guid.md)oder den global eindeutigen Bezeichner.
    
Jeder untergeordneten Block besteht aus 5 Bytes wie folgt unterteilt:
  
- Ein Bit, enth�lt einen Code, die die Differenz zwischen der aktuellen Uhrzeit und die Zeit in die Kopfzeilen-Baustein gespeichert. Dieses Bit ist 0, wenn der Unterschied weniger als.02 zweiten und gr��er als 1 ist der Unterschied weniger als eine Sekunde und zwei Jahre und gr��er als 56 Jahre.
    
- Drei�ig One Bits mit den Unterschied zwischen der aktuellen Zeit und dem Zeitpunkt, der im **FILETIME** Einheiten Kopfzeilen-Baustein. In diesem Teil des untergeordneten Blocks wird erzeugt, mit einer der beiden Strategien, abh�ngig vom Wert des ersten Bits. Wenn dieses Bit 0 (null) ist, verwirft **ScCreateConversationIndex** die 15 Bits und die unteren 18 Bits. Wenn dieses Bit ist, verwirft die Funktion die hohe 10 Bits und die unteren Bits 23. 
    
- Vier Bits mit einer Zufallszahl durch Aufrufen von Win32-Funktion, [z. B.](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx)generiert.
    
- Vier Bits mit einer Sequenz gez�hlt werden, die Teil einer Zufallszahl entnommen wird.
    
Wenn die Unterhaltung Indizes der Nachrichten manuell festgelegt werden sollen, sollten Sie die folgenden Vorschl�ge:
  
1. Behalten Sie unterschiedliche Zeitzonen der Befragten transparent; Verwenden Sie die UTC-Zeiten statt Ortszeit.
    
2. Jede Gruppe Unterhaltung mit der gleichen Zeitspanne einr�cken.
    
3. Antworten auf die Nachricht an denselben Tag zu sortieren.
    
4. Separate Threads gestartet zu unterschiedlichen Zeiten, die im gleiche Thema freigeben auftreten. 
    
5. Um eine kategorisierte Sortierung zu implementieren, sodass Nachrichten nach Thema gruppiert werden, sortieren Sie zuerst nach **PR_CONVERSATION_TOPIC** und dann nach **PR_CONVERSATION_INDEX**. Um die Ergebnisse der Sortierung darzustellen, legen Sie die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft für Nachrichten mit einem Unterhaltungsindex, der 22 Byte lang ist, auf 0 fest. Erhöhen Sie dann für jede Verlängerung um 5 Byte den Wert der **PR_DEPTH**-Eigenschaft um 1. 
    
Die PR_ORIGINAL Gruppe von Eigenschaften kann auch f�r Unterhaltung Nachverfolgen verwendet werden. Legen Sie diese Eigenschaften auf die urspr�ngliche Nachricht antworten oder weitergeleiteten Nachrichten verkn�pfen. Alle PR_ORIGINAL-Eigenschaften sind optional. Wenn Sie zum Beispiel **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) nicht explizit festlegen, kann der Nachrichtenspeicheranbieter den Standardwert oder den Wert der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft verwenden. Wenn Sie gleichermaßen **PR_ORIGINAL_AUTHOR_NAME** oder **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) nicht festlegen, können diese Eigenschaften standardmäßig die Werte der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))- bzw. der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaft verwenden. 
  

