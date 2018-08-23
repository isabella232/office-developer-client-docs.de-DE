---
title: Nachverfolgen von Unterhaltungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae8b5a474675c0afd771f4e8dfd060d0b379c8f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572221"
---
# <a name="tracking-conversations"></a>Nachverfolgen von Unterhaltungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Nachverfolgen der Unterhaltung sammelt Antworten auf eine Nachricht. Clients sollte zwei Eigenschaften, mit denen in Unterhaltungen nachverfolgen festgelegt:
  
- **PR_CONVERSATION_TOPIC** ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** ist der normalisierte Betreff der Nachricht, den Betreff ohne das Pr�fixzeichenfolgen. Legen Sie diese Eigenschaft auf den Wert, der die Nachricht **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft. 
    
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
    
- Vier Bits mit einer Zufallszahl durch Aufrufen von Win32-Funktion, [z. B.](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx)generiert.
    
- Vier Bits mit einer Sequenz gez�hlt werden, die Teil einer Zufallszahl entnommen wird.
    
Wenn die Unterhaltung Indizes der Nachrichten manuell festgelegt werden sollen, sollten Sie die folgenden Vorschl�ge:
  
1. Behalten Sie unterschiedliche Zeitzonen der Befragten transparent; Verwenden Sie die UTC-Zeiten statt Ortszeit.
    
2. Jede Gruppe Unterhaltung mit der gleichen Zeitspanne einr�cken.
    
3. Antworten auf die Nachricht an denselben Tag zu sortieren.
    
4. Separate Threads gestartet zu unterschiedlichen Zeiten, die im gleiche Thema freigeben auftreten. 
    
5. Um eine kategorisierte Sortierung zu implementieren, damit Nachrichten nach Thema gruppiert sind, sortiert nach **PR_CONVERSATION_TOPIC** erste und dann nach **PR_CONVERSATION_INDEX**. Um die Ergebnisse der Sortierung darzustellen, legen Sie die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft auf 0 für Nachrichten mit einem Unterhaltung Index, der 22 Bytes lang ist. Erh�hen Sie f�r jede in der L�nge 5-Byte-Inkrement, klicken Sie dann den Wert der Eigenschaft **PR_DEPTH** um eins. 
    
Die PR_ORIGINAL Gruppe von Eigenschaften kann auch f�r Unterhaltung Nachverfolgen verwendet werden. Legen Sie diese Eigenschaften auf die urspr�ngliche Nachricht antworten oder weitergeleiteten Nachrichten verkn�pfen. Alle Eigenschaften PR_ORIGINAL sind optional. Wenn Sie nicht explizit, beispielsweise **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) festlegen kann der Nachricht Speicheranbieter der Standardwert oder der Wert der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) verwenden -Eigenschaft. Dienstanbieter entscheidet auch, wenn Sie nicht **PR_ORIGINAL_AUTHOR_NAME** oder **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) festlegen, können diese Eigenschaften auf die Werte der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und **PR_ Standard CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaften fest. 
  

