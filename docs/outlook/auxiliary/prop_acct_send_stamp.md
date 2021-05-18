---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Gibt den accountsendstamp zurück.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423006"
---
# <a name="prop_acct_send_stamp"></a><span data-ttu-id="9c1e4-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="9c1e4-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="9c1e4-104">Gibt den Kontostempel "Senden" zurück.</span><span class="sxs-lookup"><span data-stu-id="9c1e4-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9c1e4-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9c1e4-105">Quick info</span></span>

<span data-ttu-id="9c1e4-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="9c1e4-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c1e4-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9c1e4-107">Identifier:</span></span>  <br/> |<span data-ttu-id="9c1e4-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="9c1e4-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="9c1e4-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="9c1e4-109">Property type:</span></span>  <br/> |<span data-ttu-id="9c1e4-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c1e4-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9c1e4-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="9c1e4-111">Property tag:</span></span>  <br/> |<span data-ttu-id="9c1e4-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="9c1e4-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="9c1e4-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="9c1e4-113">Access:</span></span>  <br/> |<span data-ttu-id="9c1e4-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c1e4-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c1e4-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c1e4-115">Remarks</span></span>

<span data-ttu-id="9c1e4-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)</span><span class="sxs-lookup"><span data-stu-id="9c1e4-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="9c1e4-117">Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="9c1e4-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c1e4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c1e4-118">See also</span></span>

- [<span data-ttu-id="9c1e4-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="9c1e4-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="9c1e4-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="9c1e4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

