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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321266"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="6123f-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6123f-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="6123f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6123f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6123f-105">Stellt Informationen für ein Offlineobjekt bereit.</span><span class="sxs-lookup"><span data-stu-id="6123f-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6123f-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="6123f-106">Provided by:</span></span>  <br/> |<span data-ttu-id="6123f-107">Abfrage auf [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="6123f-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="6123f-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6123f-108">Called by:</span></span>  <br/> |<span data-ttu-id="6123f-109">Client</span><span class="sxs-lookup"><span data-stu-id="6123f-109">Client</span></span>  <br/> |
|<span data-ttu-id="6123f-110">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6123f-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6123f-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="6123f-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6123f-112">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6123f-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6123f-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="6123f-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="6123f-114">Legt den aktuellen Status eines Offline Objekts auf Online oder offline fest.</span><span class="sxs-lookup"><span data-stu-id="6123f-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="6123f-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="6123f-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="6123f-116">Ruft die Bedingungen ab, für die Rückrufe von einem Offlineobjekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6123f-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="6123f-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="6123f-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="6123f-118">Ruft den aktuellen Online-oder Offlinestatus eines Offline Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="6123f-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="6123f-119">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6123f-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="6123f-120">Dieser Member ist ein Platzhalter und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6123f-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6123f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6123f-121">Remarks</span></span>

<span data-ttu-id="6123f-122">Ein Client verwendet **[HrOpenOfflineObj](hropenofflineobj.md)** zum Öffnen und Abrufen eines Offline Objekts, das **IMAPIOfflineMgr**unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6123f-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="6123f-123">Da **IMAPIOfflineMgr** von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)erbt, kann der Client diese Schnittstelle Abfragen (mithilfe von [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)), um einen Zeiger auf den Schnittstellenzeiger für **IMAPIOffline** für das Offlineobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6123f-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="6123f-124">Der Client kann dann den aktuellen Status des Objekts abrufen oder festlegen oder sich über die Rückruffunktionen des Objekts informieren (durch Aufrufen von **IMAPIOffline:: getCapabilities** ) und das Einrichten von Rückrufen mithilfe von **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="6123f-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="6123f-125">Ein Mitglied dieser Schnittstelle ist ein Platzhalter für die interne Verwendung von Microsoft Outlook 2013 und kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6123f-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="6123f-126">Andere Elemente in dieser Schnittstelle dürfen nur wie dokumentiert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6123f-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6123f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6123f-127">See also</span></span>



[<span data-ttu-id="6123f-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="6123f-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="6123f-129">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="6123f-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="6123f-130">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6123f-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6123f-131">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6123f-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

