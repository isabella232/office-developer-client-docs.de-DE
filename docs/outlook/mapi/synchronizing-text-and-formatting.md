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
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435103"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="05a4d-103">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="05a4d-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="05a4d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05a4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05a4d-105">Die größte Herausforderung beim Senden von Rich Text Format (RTF)-Nachrichten besteht darin, den Text mit der Formatierung zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="05a4d-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="05a4d-106">Um sicherzustellen, dass Nachrichten, wenn sie am Ziel ankommen, wie ihre Ermittler vorgesehen sind und dass Text und Formatierung synchronisiert werden, stellt MAPI die [RTFSync-Funktion](rtfsync.md) zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="05a4d-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="05a4d-107">**RTFSync wird** in der Regel von RTF-unterstützenden Clients aufgerufen, bevor eingehende Nachrichten angezeigt werden, und vom MAPI-Spooler, wenn Nachrichten an einen Transportanbieter heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="05a4d-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="05a4d-108">Anrufer geben den Bereich möglicher Abweichungen an, indem sie ein oder zwei Flags an **RTFSync übergeben:**</span><span class="sxs-lookup"><span data-stu-id="05a4d-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="05a4d-109">RTF_SYNC_BODY_CHANGED, um eine Änderung im Nachrichtentext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05a4d-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="05a4d-110">RTF_SYNC_RTF_CHANGED, um eine Änderung der Nachrichtenformatierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05a4d-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="05a4d-111">Der Synchronisierungsprozess in **RTFSync** ist eine ausgefeilte zyklische Redundanzprüfung (CrC) des Nachrichtentexts, die einige Zeichen ignoriert und andere konvertiert.</span><span class="sxs-lookup"><span data-stu-id="05a4d-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="05a4d-112">Zeichen, die wahrscheinlich von Transportanbietern hinzugefügt wurden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="05a4d-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="05a4d-113">MAPI definiert verschiedene Eigenschaften für die Arbeit mit RTF, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="05a4d-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="05a4d-114">**RTF-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="05a4d-114">**RTF property**</span></span>|<span data-ttu-id="05a4d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05a4d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05a4d-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-117">Gibt den Anfang des tatsächlichen Nachrichtentexts an.</span><span class="sxs-lookup"><span data-stu-id="05a4d-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="05a4d-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-119">Enthält das Ergebnis der zyklischen Redundanzüberprüfung des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="05a4d-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="05a4d-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-121">Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="05a4d-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="05a4d-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-123">Wird auf TRUE festgelegt, wenn der Nachrichtentext und die Formatierung synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="05a4d-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="05a4d-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-125">Enthält die Anzahl der Nicht-Whitespace-Zeichen, die dem Nachrichtentext voraus waren.</span><span class="sxs-lookup"><span data-stu-id="05a4d-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="05a4d-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="05a4d-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="05a4d-127">Enthält die Anzahl der Nicht-Whitespace-Zeichen, die dem Nachrichtentext nachgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="05a4d-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

