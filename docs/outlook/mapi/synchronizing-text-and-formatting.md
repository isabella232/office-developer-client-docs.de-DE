---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346599"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="144ad-103">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="144ad-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="144ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="144ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="144ad-105">Die wichtigste Herausforderung beim Senden von RTF-Nachrichten (Rich Text Format) ist, dass der Text mit der Formatierung synchronisiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="144ad-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="144ad-106">Um sicherzustellen, dass Nachrichten an Ihrem Ziel ankommen, werden Sie als ihre Absender beabsichtigt, und der Text und die Formatierung werden synchronisiert, MAPI stellt die [RTFSync](rtfsync.md) -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="144ad-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="144ad-107">**RTFSync** wird in der Regel von RTF-fähigen Clients aufgerufen, bevor eingehende Nachrichten und der MAPI-Spooler angezeigt werden, wenn Nachrichten an einen Transportanbieter heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="144ad-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="144ad-108">Anrufer geben den Bereich möglicher Diskrepanz an, indem Sie ein oder zwei Flags an **RTFSync**übergeben:</span><span class="sxs-lookup"><span data-stu-id="144ad-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="144ad-109">RTF_SYNC_BODY_CHANGED, um eine Änderung im Nachrichtentext anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="144ad-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="144ad-110">RTF_SYNC_RTF_CHANGED, um eine Änderung der Nachrichtenformatierung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="144ad-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="144ad-111">Beim Synchronisierungsvorgang in **RTFSync** handelt es sich um eine ausgeklügelte zyklische Redundanzprüfung des Nachrichtentexts, der einige Zeichen ignoriert und andere konvertiert.</span><span class="sxs-lookup"><span data-stu-id="144ad-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="144ad-112">Zeichen, die von Transportanbietern höchstwahrscheinlich hinzugefügt wurden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="144ad-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="144ad-113">MAPI definiert mehrere Eigenschaften für das Arbeiten mit RTF, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="144ad-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="144ad-114">**RTF-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="144ad-114">**RTF property**</span></span>|<span data-ttu-id="144ad-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="144ad-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="144ad-116">**PR_RTF_SYNC_BODY_TAG** ([Pidtagrtfsyncbodytag (](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-117">Gibt den Anfang des eigentlichen Nachrichtentexts an.</span><span class="sxs-lookup"><span data-stu-id="144ad-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="144ad-118">**PR_RTF_SYNC_BODY_CRC** ([Pidtagrtfsyncbodycrc (](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-119">Enthält das Ergebnis der Überprüfung der zyklischen Redundanz des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="144ad-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="144ad-120">**PR_RTF_SYNC_BODY_COUNT** ([Pidtagrtfsyncbodycount (](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-121">Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="144ad-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="144ad-122">**PR_RTF_IN_SYNC** ([Pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-123">Wird auf TRUE festgelegt, wenn der Nachrichtentext und die Formatierung synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="144ad-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="144ad-124">**PR_RTF_SYNC_PREFIX_COUNT** ([Pidtagrtfsyncprefixcount (](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-125">Enthält die Anzahl von Leerzeichen, die den Nachrichtentext bevorstehen.</span><span class="sxs-lookup"><span data-stu-id="144ad-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="144ad-126">**PR_RTF_SYNC_TRAILING_COUNT** ([Pidtagrtfsynctrailingcount (](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="144ad-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="144ad-127">Enthält die Anzahl von Leerzeichen, die den Nachrichtentext nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="144ad-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

