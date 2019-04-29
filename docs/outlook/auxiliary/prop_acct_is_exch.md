---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True, wenn das Konto ein Exchange-Konto ist.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418232"
---
# <a name="propacctisexch"></a><span data-ttu-id="e1c5f-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="e1c5f-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="e1c5f-104">True, wenn das Konto ein Exchange-Konto ist.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1c5f-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e1c5f-105">Quick info</span></span>

<span data-ttu-id="e1c5f-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="e1c5f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1c5f-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="e1c5f-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="e1c5f-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="e1c5f-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-109">Property type:</span></span>  <br/> |<span data-ttu-id="e1c5f-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1c5f-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1c5f-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="e1c5f-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="e1c5f-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="e1c5f-113">Access</span><span class="sxs-lookup"><span data-stu-id="e1c5f-113">Access:</span></span>  <br/> |<span data-ttu-id="e1c5f-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1c5f-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1c5f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1c5f-115">Remarks</span></span>

<span data-ttu-id="e1c5f-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="e1c5f-117">Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1c5f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1c5f-118">See also</span></span>

- [<span data-ttu-id="e1c5f-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="e1c5f-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e1c5f-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

