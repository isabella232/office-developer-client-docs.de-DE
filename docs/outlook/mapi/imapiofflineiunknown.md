---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 616bb4774e2ca5385e7da867477cb8849d94336b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568385"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="fbc88-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbc88-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="fbc88-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbc88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbc88-105">Enthält Informationen für eine offline-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbc88-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbc88-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="fbc88-106">Provided by:</span></span>  <br/> |<span data-ttu-id="fbc88-107">Abfrage für [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="fbc88-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="fbc88-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fbc88-108">Called by:</span></span>  <br/> |<span data-ttu-id="fbc88-109">Client</span><span class="sxs-lookup"><span data-stu-id="fbc88-109">Client</span></span>  <br/> |
|<span data-ttu-id="fbc88-110">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="fbc88-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fbc88-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="fbc88-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fbc88-112">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="fbc88-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbc88-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc88-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="fbc88-114">Legt den aktuellen Zustand eines offline-Objekts zu online oder offline.</span><span class="sxs-lookup"><span data-stu-id="fbc88-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="fbc88-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc88-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="fbc88-116">Ruft die Bedingungen für die Rückrufe durch eine offline-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fbc88-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="fbc88-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc88-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="fbc88-118">Ruft den aktuellen online oder offline-Status eines offline-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="fbc88-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="fbc88-119">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="fbc88-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="fbc88-120">Dieser Member ist ein Platzhalter und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbc88-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbc88-121">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fbc88-121">Remarks</span></span>

<span data-ttu-id="fbc88-122">Ein Client verwendet **[HrOpenOfflineObj](hropenofflineobj.md)** zu öffnen, und erhalten eine offline-Objekt, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbc88-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="fbc88-123">Da **IMAPIOfflineMgr** von [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)erbt, kann der Client (mithilfe von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) diese Schnittstelle Abfragen um einen Zeiger auf den Zeiger der Schnittstelle für **IMAPIOffline** für das offline-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fbc88-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="fbc88-124">Der Client kann dann abzurufen oder festzulegen den aktuellen Status des Objekts zugreifen, oder informieren Sie sich über die Callback-Funktionen des Objekts (durch Aufrufen von **IMAPIOffline::GetCapabilities** ) und auf Rückrufe mithilfe von **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fbc88-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="fbc88-125">Ein Element in dieser Schnittstelle ist ein Platzhalter für die interne Verwendung von Microsoft Outlook 2013 reserviert und kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fbc88-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="fbc88-126">Andere Member in dieser Schnittstelle müssen nur gemäß Dokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbc88-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fbc88-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc88-127">See also</span></span>



[<span data-ttu-id="fbc88-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="fbc88-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="fbc88-129">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="fbc88-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="fbc88-130">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="fbc88-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fbc88-131">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fbc88-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

