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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4c758ecd0134ca11ced6f771303896bd885a22c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436223"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="c454c-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c454c-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="c454c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c454c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c454c-105">Diese Schnittstelle bietet Hilfsfunktionen bei der Replikation über die **[IOSTX-Schnittstelle.](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c454c-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c454c-106">Bereitgestellt von</span><span class="sxs-lookup"><span data-stu-id="c454c-106">Provided by</span></span>  <br/> |<span data-ttu-id="c454c-107">Abfrage in [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c454c-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="c454c-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c454c-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c454c-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="c454c-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c454c-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c454c-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c454c-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="c454c-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="c454c-112">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="c454c-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="c454c-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="c454c-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="c454c-114">Ruft die zugeordnete **[IOSTX-Schnittstelle](iostxiunknown.md)** ab.</span><span class="sxs-lookup"><span data-stu-id="c454c-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="c454c-115">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-116">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-117">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-118">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-119">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-120">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-121">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-122">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="c454c-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="c454c-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="c454c-124">Legt einen lokalen Speicher fest, um den Outlook Protokoll-Manager zu emulieren, um ausgehende Nachrichten mit einem Server zu spoolen.</span><span class="sxs-lookup"><span data-stu-id="c454c-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="c454c-125">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-126">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-127">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-128">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-129">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-130">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-131">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-132">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="c454c-133">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="c454c-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c454c-134">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c454c-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c454c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c454c-135">See also</span></span>



[<span data-ttu-id="c454c-136">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="c454c-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c454c-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c454c-137">MAPI Constants</span></span>](mapi-constants.md)

