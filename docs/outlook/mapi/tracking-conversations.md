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
# <a name="tracking-conversations"></a><span data-ttu-id="ba0e0-103">Nachverfolgen von Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="ba0e0-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="ba0e0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba0e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba0e0-p101">Nachverfolgen der Unterhaltung sammelt Antworten auf eine Nachricht. Clients sollte zwei Eigenschaften, mit denen in Unterhaltungen nachverfolgen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="ba0e0-107">**PR_CONVERSATION_TOPIC** ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ba0e0-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="ba0e0-108">**PR_CONVERSATION_TOPIC** ist der normalisierte Betreff der Nachricht, den Betreff ohne das Pr�fixzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="ba0e0-109">Legen Sie diese Eigenschaft auf den Wert, der die Nachricht **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="ba0e0-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ba0e0-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="ba0e0-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="ba0e0-p104">**ScCreateConversationIndex** generiert den Wert eines Indexes Unterhaltung f�r alle ausgehenden Nachrichten. **ScCreateConversationIndex** implementiert den Index als ein Kopfzeilen-Baustein, die 22 Bytes L�nge, gefolgt von NULL ist oder mehrere untergeordnete blockiert jede 5 Bytes L�nge.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="ba0e0-116">Kopfzeilen-Baustein besteht aus 22 Bytes in drei Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="ba0e0-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="ba0e0-p105">Ein reserviertes Byte. Der Wert ist 1.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="ba0e0-119">F�nf Bytes f�r die aktuelle Systemzeit in der Struktur [FILETIME](filetime.md) -Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="ba0e0-120">Sechzehn Bytes gedr�ckt halten, eine [GUID](guid.md)oder den global eindeutigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="ba0e0-121">Jeder untergeordneten Block besteht aus 5 Bytes wie folgt unterteilt:</span><span class="sxs-lookup"><span data-stu-id="ba0e0-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="ba0e0-p106">Ein Bit, enth�lt einen Code, die die Differenz zwischen der aktuellen Uhrzeit und die Zeit in die Kopfzeilen-Baustein gespeichert. Dieses Bit ist 0, wenn der Unterschied weniger als.02 zweiten und gr��er als 1 ist der Unterschied weniger als eine Sekunde und zwei Jahre und gr��er als 56 Jahre.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="ba0e0-p107">Drei�ig One Bits mit den Unterschied zwischen der aktuellen Zeit und dem Zeitpunkt, der im **FILETIME** Einheiten Kopfzeilen-Baustein. In diesem Teil des untergeordneten Blocks wird erzeugt, mit einer der beiden Strategien, abh�ngig vom Wert des ersten Bits. Wenn dieses Bit 0 (null) ist, verwirft **ScCreateConversationIndex** die 15 Bits und die unteren 18 Bits. Wenn dieses Bit ist, verwirft die Funktion die hohe 10 Bits und die unteren Bits 23.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="ba0e0-127">Vier Bits mit einer Zufallszahl durch Aufrufen von Win32-Funktion, [z. B.](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx)generiert.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="ba0e0-128">Vier Bits mit einer Sequenz gez�hlt werden, die Teil einer Zufallszahl entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="ba0e0-129">Wenn die Unterhaltung Indizes der Nachrichten manuell festgelegt werden sollen, sollten Sie die folgenden Vorschl�ge:</span><span class="sxs-lookup"><span data-stu-id="ba0e0-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="ba0e0-130">Behalten Sie unterschiedliche Zeitzonen der Befragten transparent; Verwenden Sie die UTC-Zeiten statt Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="ba0e0-131">Jede Gruppe Unterhaltung mit der gleichen Zeitspanne einr�cken.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="ba0e0-132">Antworten auf die Nachricht an denselben Tag zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="ba0e0-133">Separate Threads gestartet zu unterschiedlichen Zeiten, die im gleiche Thema freigeben auftreten.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="ba0e0-134">Um eine kategorisierte Sortierung zu implementieren, damit Nachrichten nach Thema gruppiert sind, sortiert nach **PR_CONVERSATION_TOPIC** erste und dann nach **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="ba0e0-135">Um die Ergebnisse der Sortierung darzustellen, legen Sie die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft auf 0 für Nachrichten mit einem Unterhaltung Index, der 22 Bytes lang ist.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="ba0e0-136">Erh�hen Sie f�r jede in der L�nge 5-Byte-Inkrement, klicken Sie dann den Wert der Eigenschaft **PR_DEPTH** um eins.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="ba0e0-137">Die PR_ORIGINAL Gruppe von Eigenschaften kann auch f�r Unterhaltung Nachverfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="ba0e0-138">Legen Sie diese Eigenschaften auf die urspr�ngliche Nachricht antworten oder weitergeleiteten Nachrichten verkn�pfen.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="ba0e0-139">Alle Eigenschaften PR_ORIGINAL sind optional.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="ba0e0-140">Wenn Sie nicht explizit, beispielsweise **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)) festlegen kann der Nachricht Speicheranbieter der Standardwert oder der Wert der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) verwenden -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="ba0e0-141">Dienstanbieter entscheidet auch, wenn Sie nicht **PR_ORIGINAL_AUTHOR_NAME** oder **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)) festlegen, können diese Eigenschaften auf die Werte der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und **PR_ Standard CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="ba0e0-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

