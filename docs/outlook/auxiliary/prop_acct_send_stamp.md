---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Gibt die accountsendstamp zurück.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327608"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="64bc1-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="64bc1-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="64bc1-104">Gibt das Konto "Send"-Stempel zurück.</span><span class="sxs-lookup"><span data-stu-id="64bc1-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="64bc1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="64bc1-105">Quick info</span></span>

<span data-ttu-id="64bc1-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="64bc1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64bc1-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="64bc1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="64bc1-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="64bc1-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="64bc1-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="64bc1-109">Property type:</span></span>  <br/> |<span data-ttu-id="64bc1-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64bc1-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64bc1-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="64bc1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="64bc1-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="64bc1-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="64bc1-113">Access</span><span class="sxs-lookup"><span data-stu-id="64bc1-113">Access:</span></span>  <br/> |<span data-ttu-id="64bc1-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64bc1-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64bc1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64bc1-115">Remarks</span></span>

<span data-ttu-id="64bc1-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab.</span><span class="sxs-lookup"><span data-stu-id="64bc1-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="64bc1-117">Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück.</span><span class="sxs-lookup"><span data-stu-id="64bc1-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64bc1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64bc1-118">See also</span></span>

- [<span data-ttu-id="64bc1-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="64bc1-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="64bc1-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="64bc1-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

