---
title: Erstellen eines Nachrichtenbetreffs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332963"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="50a65-103">Erstellen eines Nachrichtenbetreffs</span><span class="sxs-lookup"><span data-stu-id="50a65-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="50a65-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50a65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50a65-105">Der Betreff einer Nachricht, **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)), ist eine optionale Eigenschaft, mit der der Zweck einer Nachricht zusammengefasst wird.</span><span class="sxs-lookup"><span data-stu-id="50a65-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="50a65-106">Wenn Sie festlegen, dass es sich um eine Zeichenfolge von 128 Byte oder niedriger.</span><span class="sxs-lookup"><span data-stu-id="50a65-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="50a65-107">Das 128-Byte-Limit ist kein Grenzwert, der von MAPI auferlegt wird. Es handelt sich um eine Grenze, die von einigen Nachrichtenspeicher Anbietern auferlegt wird.</span><span class="sxs-lookup"><span data-stu-id="50a65-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="50a65-108">Um die Interoperabilität mit Anbietern zu gewährleisten, die dies erzwingen, begrenzen Sie die Anzahl der Probanden auf 128 Byte.</span><span class="sxs-lookup"><span data-stu-id="50a65-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="50a65-109">Beachten Sie, dass einige Nachrichtenspeicher Anbieter nicht zulassen, dass **PR_Subject** in einen Stream mit der [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="50a65-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="50a65-110">Legen Sie **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) nicht fest. Diese Eigenschaft wird nur für Antworten und weitergeleitete Nachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50a65-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

