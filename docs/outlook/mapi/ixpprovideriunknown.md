---
title: IXPProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49cb500279540317059cde2d9baba28fcbf06165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574111"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="b9c52-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9c52-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="b9c52-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9c52-105">Initialisiert einen Transport-Anbieter-Objekt und das Objekt heruntergefahren, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9c52-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9c52-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b9c52-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9c52-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="b9c52-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="b9c52-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="b9c52-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b9c52-109">Transport-Anbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="b9c52-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="b9c52-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b9c52-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9c52-111">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="b9c52-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="b9c52-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b9c52-112">Called by:</span></span>  <br/> |<span data-ttu-id="b9c52-113">Die MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="b9c52-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="b9c52-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b9c52-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b9c52-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="b9c52-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="b9c52-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="b9c52-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b9c52-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="b9c52-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b9c52-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b9c52-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b9c52-119">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="b9c52-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="b9c52-120">In einer bestimmten Reihenfolge eines Transportdienstes wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9c52-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="b9c52-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="b9c52-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="b9c52-122">Richtet eine Sitzung, in der eine Clientanwendung eines Transportdienstes anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b9c52-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

