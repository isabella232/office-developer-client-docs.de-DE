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
ms.openlocfilehash: e12f69e3486e5eeb9087b30753735f7f910dc6f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792903"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="3588e-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3588e-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="3588e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3588e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3588e-105">Initialisiert einen Transport-Anbieter-Objekt und das Objekt heruntergefahren, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3588e-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3588e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3588e-106">Header file:</span></span>  <br/> |<span data-ttu-id="3588e-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="3588e-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="3588e-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="3588e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3588e-109">Transport-Anbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="3588e-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="3588e-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3588e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3588e-111">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="3588e-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="3588e-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3588e-112">Called by:</span></span>  <br/> |<span data-ttu-id="3588e-113">Die MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="3588e-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="3588e-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="3588e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3588e-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="3588e-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="3588e-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="3588e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3588e-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="3588e-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3588e-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="3588e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3588e-119">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="3588e-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="3588e-120">In einer bestimmten Reihenfolge eines Transportdienstes wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="3588e-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="3588e-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="3588e-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="3588e-122">Richtet eine Sitzung, in der eine Clientanwendung eines Transportdienstes anmeldet.</span><span class="sxs-lookup"><span data-stu-id="3588e-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

