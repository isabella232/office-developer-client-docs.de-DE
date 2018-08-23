---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588818"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="353ae-103">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="353ae-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="353ae-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="353ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="353ae-105">Die größte Herausforderung beim Senden von Nachrichten Rich Text Format (RTF) wird den Text mit der Formatierung synchronisiert halten.</span><span class="sxs-lookup"><span data-stu-id="353ae-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="353ae-106">Um sicherzustellen, dass beim Empfang von Nachrichten an ihrem Ziel wie für ihre Ersteller für die direkte Verwendung und sind die Text und Formatierung werden synchronisiert, MAPI bietet die [RTFSync](rtfsync.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="353ae-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="353ae-107">**RTFSync** wird beim Download von Nachrichten mit einem Dienstanbieter Transport in der Regel durch RTF-fähigen Clients vor dem eingehende Nachrichten anzeigen und die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="353ae-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="353ae-108">Anrufer Geben Sie den Bereich der möglichen Abweichung, indem Sie ein oder zwei Flags zu **RTFSync**übergeben:</span><span class="sxs-lookup"><span data-stu-id="353ae-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="353ae-109">RTF_SYNC_BODY_CHANGED an, dass eine Änderung im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="353ae-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="353ae-110">RTF_SYNC_RTF_CHANGED an, dass eine Änderung in der Nachricht formatieren.</span><span class="sxs-lookup"><span data-stu-id="353ae-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="353ae-111">Synchronisierungsvorgangs, das in **RTFSync** auftritt, ist eine anspruchsvolle CRC-Prüfung (CRC) des Texts Nachricht, die einige Zeichen ignoriert und andere konvertiert.</span><span class="sxs-lookup"><span data-stu-id="353ae-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="353ae-112">Zeichen, die in den meisten Fällen von Transportanbieter hinzugefügt wurden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="353ae-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="353ae-113">MAPI definiert verschiedene Eigenschaften für die Arbeit mit RTF, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="353ae-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="353ae-114">**RTF-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="353ae-114">**RTF property**</span></span>|<span data-ttu-id="353ae-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="353ae-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="353ae-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-117">Gibt den Anfang des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="353ae-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="353ae-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-119">Das Ergebnis der CRC-Prüfung von den Nachrichtentext enthält.</span><span class="sxs-lookup"><span data-stu-id="353ae-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="353ae-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-121">Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="353ae-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="353ae-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-123">Legen Sie TRUE, wenn die Nachricht Text und Formatierung synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="353ae-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="353ae-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-125">Enthält der Anzahl der Zeichen Nonwhitespace, Länderkürzel den Nachrichtentext an.</span><span class="sxs-lookup"><span data-stu-id="353ae-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="353ae-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="353ae-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="353ae-127">Enthält die Anzahl der Zeichen Nonwhitespace, die den Nachrichtentext aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="353ae-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

