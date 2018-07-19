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
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791495"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="2ab82-103">Erstellen eines Nachrichtenbetreffs</span><span class="sxs-lookup"><span data-stu-id="2ab82-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="2ab82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ab82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ab82-105">Der Betreff der Nachricht **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) ist eine optionale-Eigenschaft verwendet, um den Zweck der eine Nachricht zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="2ab82-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="2ab82-106">Wenn diese Liste festgelegt werden soll, stellen Sie es eine Zeichenfolge 128 Byte oder weniger.</span><span class="sxs-lookup"><span data-stu-id="2ab82-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="2ab82-107">Der 128 Byte-Grenzwert ist keiner-Limit MAPI. Es ist eine-Limit Zeichenfolgeneigenschaften einige Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ab82-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="2ab82-108">Einschränken Sie, um die Interoperabilität mit Anbietern zu gewährleisten, die es bedingen Antragsteller 128 Byte.</span><span class="sxs-lookup"><span data-stu-id="2ab82-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="2ab82-109">Beachten Sie, dass einige Anbieter Nachricht **PR_SUBJECT** in ein Stream-Objekt mit der [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben werden nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="2ab82-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="2ab82-110">Stellen Sie keine **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) Diese Eigenschaft ist nur für Antworten festlegen und weitergeleitete Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2ab82-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

