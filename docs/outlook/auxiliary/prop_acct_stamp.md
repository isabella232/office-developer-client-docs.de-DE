---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Gibt den Kontostempel zurück.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408250"
---
# <a name="prop_acct_stamp"></a><span data-ttu-id="d309f-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="d309f-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="d309f-104">Gibt den Kontostempel zurück.</span><span class="sxs-lookup"><span data-stu-id="d309f-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d309f-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d309f-105">Quick info</span></span>

<span data-ttu-id="d309f-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d309f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d309f-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d309f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d309f-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="d309f-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="d309f-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="d309f-109">Property type:</span></span>  <br/> |<span data-ttu-id="d309f-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d309f-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d309f-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="d309f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d309f-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="d309f-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="d309f-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="d309f-113">Access:</span></span>  <br/> |<span data-ttu-id="d309f-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d309f-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d309f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d309f-115">Remarks</span></span>

<span data-ttu-id="d309f-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)</span><span class="sxs-lookup"><span data-stu-id="d309f-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d309f-117">Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="d309f-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d309f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d309f-118">See also</span></span>

- [<span data-ttu-id="d309f-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="d309f-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="d309f-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="d309f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

