---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt eine Konto-ID zurück, die in Outlook-Profilen eindeutig ist.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409433"
---
# <a name="propacctminiuid"></a><span data-ttu-id="97b86-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="97b86-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="97b86-104">Gibt eine Konto-ID zurück, die in Outlook-Profilen eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="97b86-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="97b86-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="97b86-105">Quick info</span></span>

<span data-ttu-id="97b86-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="97b86-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97b86-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="97b86-107">Identifier:</span></span>  <br/> |<span data-ttu-id="97b86-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="97b86-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="97b86-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="97b86-109">Property type:</span></span>  <br/> |<span data-ttu-id="97b86-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97b86-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97b86-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="97b86-111">Property tag:</span></span>  <br/> |<span data-ttu-id="97b86-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="97b86-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="97b86-113">Access</span><span class="sxs-lookup"><span data-stu-id="97b86-113">Access:</span></span>  <br/> |<span data-ttu-id="97b86-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="97b86-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b86-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97b86-115">Remarks</span></span>

<span data-ttu-id="97b86-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab.</span><span class="sxs-lookup"><span data-stu-id="97b86-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="97b86-117">Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück.</span><span class="sxs-lookup"><span data-stu-id="97b86-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="97b86-118">Diese Eigenschaft unterscheidet sich von [PROP_ACCT_ID](prop_acct_id.md) dadurch, dass ihr Wert das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert, wohingegen **PROP_ACCT_ID** nur unter allen Konten innerhalb dieses einen Profils eindeutig ist. in der das Konto erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="97b86-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="97b86-119">Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten Sätzen durchwandert, kann **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="97b86-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="97b86-120">**PROP_ACCT_ID** können jedoch möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="97b86-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97b86-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97b86-121">See also</span></span>

- [<span data-ttu-id="97b86-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="97b86-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="97b86-123">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="97b86-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="97b86-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="97b86-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

