---
title: IPSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX
api_type:
- COM
ms.assetid: 73752f57-6fbc-0201-bf95-0e75c56c04e6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4c758ecd0134ca11ced6f771303896bd885a22c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278799"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="9b8bd-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b8bd-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="9b8bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b8bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b8bd-105">Diese Schnittstelle bietet Hilfsfunktionen bei der Replikation über die **[IOSTX](iostxiunknown.md)** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b8bd-106">Bereitgestellt von</span><span class="sxs-lookup"><span data-stu-id="9b8bd-106">Provided by</span></span>  <br/> |<span data-ttu-id="9b8bd-107">Abfrage auf [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9b8bd-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="9b8bd-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9b8bd-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9b8bd-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="9b8bd-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9b8bd-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9b8bd-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b8bd-111">**[Getlasterroraufzurufen](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="9b8bd-112">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="9b8bd-113">**[GetSyncobject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="9b8bd-114">Ruft die zugeordnete **[IOSTX](iostxiunknown.md)** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="9b8bd-115">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-116">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-117">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-118">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-119">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-120">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-121">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-122">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9b8bd-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="9b8bd-124">Legt einen lokalen Speicher für die Emulation des Outlook-Protokoll-Managers zum Spoolen ausgehender Nachrichten an einen Server fest.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="9b8bd-125">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-126">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-127">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-128">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-129">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-130">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-131">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-132">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9b8bd-133">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9b8bd-134">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="9b8bd-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b8bd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b8bd-135">See also</span></span>



[<span data-ttu-id="9b8bd-136">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="9b8bd-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9b8bd-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9b8bd-137">MAPI Constants</span></span>](mapi-constants.md)

