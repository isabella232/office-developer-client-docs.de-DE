---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Gibt einen Kontobezeichner zurück, der für alle Outlook ist.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409433"
---
# <a name="prop_acct_mini_uid"></a><span data-ttu-id="1e1d1-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="1e1d1-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="1e1d1-104">Gibt einen Kontobezeichner zurück, der für alle Outlook ist.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1e1d1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1e1d1-105">Quick info</span></span>

<span data-ttu-id="1e1d1-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1e1d1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e1d1-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1e1d1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1e1d1-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="1e1d1-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="1e1d1-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="1e1d1-109">Property type:</span></span>  <br/> |<span data-ttu-id="1e1d1-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e1d1-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e1d1-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="1e1d1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1e1d1-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="1e1d1-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="1e1d1-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="1e1d1-113">Access:</span></span>  <br/> |<span data-ttu-id="1e1d1-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e1d1-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e1d1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e1d1-115">Remarks</span></span>

<span data-ttu-id="1e1d1-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)</span><span class="sxs-lookup"><span data-stu-id="1e1d1-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="1e1d1-117">Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="1e1d1-118">Diese Eigenschaft ist anders als [PROP_ACCT_ID,](prop_acct_id.md) da ihr Wert das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert, während **PROP_ACCT_ID** nur zwischen allen Konten innerhalb dieses profils, in dem das Konto erstellt wurde, eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="1e1d1-119">Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten angezeigt wird, kann **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="1e1d1-120">Die **PROP_ACCT_ID** kann jedoch möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e1d1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e1d1-121">See also</span></span>

- [<span data-ttu-id="1e1d1-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="1e1d1-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="1e1d1-123">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="1e1d1-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="1e1d1-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="1e1d1-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

