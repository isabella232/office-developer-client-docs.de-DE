---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, wenn das Konto ein Exchange-Konto ist.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791176"
---
# <a name="propacctisexch"></a><span data-ttu-id="adbfb-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="adbfb-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="adbfb-104">True, wenn das Konto ein Exchange-Konto ist.</span><span class="sxs-lookup"><span data-stu-id="adbfb-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="adbfb-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="adbfb-105">Quick info</span></span>

<span data-ttu-id="adbfb-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="adbfb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adbfb-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="adbfb-107">Identifier:</span></span>  <br/> |<span data-ttu-id="adbfb-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="adbfb-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="adbfb-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="adbfb-109">Property type:</span></span>  <br/> |<span data-ttu-id="adbfb-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="adbfb-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="adbfb-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="adbfb-111">Property tag:</span></span>  <br/> |<span data-ttu-id="adbfb-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="adbfb-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="adbfb-113">Access:</span><span class="sxs-lookup"><span data-stu-id="adbfb-113">Access:</span></span>  <br/> |<span data-ttu-id="adbfb-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="adbfb-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adbfb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adbfb-115">Remarks</span></span>

<span data-ttu-id="adbfb-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="adbfb-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="adbfb-117">Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="adbfb-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adbfb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adbfb-118">See also</span></span>

- [<span data-ttu-id="adbfb-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="adbfb-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="adbfb-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="adbfb-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

