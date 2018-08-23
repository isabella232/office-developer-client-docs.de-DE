---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565746"
---
# <a name="attmessagestatus"></a><span data-ttu-id="fa280-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="fa280-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="fa280-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa280-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa280-105">TNEF-Flags Abwärtskompatibilität beibehalten werden MAPI Nachrichtenflags zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fa280-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="fa280-106">Alle Flags werden zusammengefasst und in ein einzelnes Byte codiert.</span><span class="sxs-lookup"><span data-stu-id="fa280-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="fa280-107">Die Zuordnungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa280-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="fa280-108">**MAPI-Nachrichtenflags**</span><span class="sxs-lookup"><span data-stu-id="fa280-108">**MAPI message flags**</span></span>|<span data-ttu-id="fa280-109">**TNEF-Kennzeichen**</span><span class="sxs-lookup"><span data-stu-id="fa280-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa280-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="fa280-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="fa280-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="fa280-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="fa280-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="fa280-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="fa280-113">~ FmsModified</span><span class="sxs-lookup"><span data-stu-id="fa280-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="fa280-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="fa280-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="fa280-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fa280-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="fa280-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="fa280-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="fa280-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="fa280-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="fa280-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="fa280-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="fa280-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="fa280-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="fa280-120">Diese Flags werden in die TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="fa280-120">These flags are defined in the TNEF.H header file.</span></span>
  

