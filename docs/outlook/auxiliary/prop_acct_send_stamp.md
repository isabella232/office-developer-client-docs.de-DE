---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Gibt die Accountsendstamp zurück.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791180"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="9b53c-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="9b53c-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="9b53c-104">Gibt den Konto-Stempel "Senden" zurück.</span><span class="sxs-lookup"><span data-stu-id="9b53c-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9b53c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9b53c-105">Quick info</span></span>

<span data-ttu-id="9b53c-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="9b53c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b53c-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9b53c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="9b53c-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="9b53c-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="9b53c-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="9b53c-109">Property type:</span></span>  <br/> |<span data-ttu-id="9b53c-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b53c-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b53c-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="9b53c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="9b53c-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="9b53c-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="9b53c-113">Access:</span><span class="sxs-lookup"><span data-stu-id="9b53c-113">Access:</span></span>  <br/> |<span data-ttu-id="9b53c-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9b53c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b53c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b53c-115">Remarks</span></span>

<span data-ttu-id="9b53c-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="9b53c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="9b53c-117">Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="9b53c-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b53c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b53c-118">See also</span></span>

- [<span data-ttu-id="9b53c-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="9b53c-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="9b53c-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="9b53c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

