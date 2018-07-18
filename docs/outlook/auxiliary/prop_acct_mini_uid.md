---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt ein Konto-ID, die Outlook-Profilen eindeutig ist.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791190"
---
# <a name="propacctminiuid"></a><span data-ttu-id="b54fd-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="b54fd-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="b54fd-104">Gibt ein Konto-ID, die Outlook-Profilen eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="b54fd-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b54fd-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b54fd-105">Quick info</span></span>

<span data-ttu-id="b54fd-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b54fd-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b54fd-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b54fd-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b54fd-108">0 x 0003</span><span class="sxs-lookup"><span data-stu-id="b54fd-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="b54fd-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="b54fd-109">Property type:</span></span>  <br/> |<span data-ttu-id="b54fd-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b54fd-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b54fd-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="b54fd-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b54fd-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="b54fd-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="b54fd-113">Access:</span><span class="sxs-lookup"><span data-stu-id="b54fd-113">Access:</span></span>  <br/> |<span data-ttu-id="b54fd-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b54fd-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b54fd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b54fd-115">Remarks</span></span>

<span data-ttu-id="b54fd-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="b54fd-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="b54fd-117">Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="b54fd-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="b54fd-118">Diese Eigenschaft unterscheidet sich von [PROP_ACCT_ID](prop_acct_id.md) , dessen Wert das Konto innerhalb und außerhalb der Profil, in dem das Konto erstellt wurde, eindeutig identifiziert wird, während **PROP_ACCT_ID** nur für alle Konten in diesem Profil eine eindeutig ist. in dem das Konto erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b54fd-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="b54fd-119">Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil und andere Menge von Konten wechselt, kann das ursprüngliche Konto im ursprünglichen Profil von **PROP_ACCT_MINI_UID** eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b54fd-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="b54fd-120">**PROP_ACCT_ID** können jedoch möglicherweise über ein Konto im Profil des zweiten Computer Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="b54fd-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b54fd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b54fd-121">See also</span></span>

- [<span data-ttu-id="b54fd-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="b54fd-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="b54fd-123">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="b54fd-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="b54fd-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b54fd-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

