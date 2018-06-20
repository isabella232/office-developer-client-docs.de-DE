---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner, der eindeutig innerhalb des Profils ein Konto in der das Konto erstellt wird.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791189"
---
# <a name="propacctid"></a><span data-ttu-id="a95f5-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="a95f5-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="a95f5-104">Gibt einen Bezeichner, der eindeutig innerhalb des Profils ein Konto in der das Konto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a95f5-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a95f5-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a95f5-105">Quick info</span></span>

<span data-ttu-id="a95f5-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a95f5-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a95f5-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a95f5-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a95f5-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="a95f5-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="a95f5-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="a95f5-109">Property type:</span></span>  <br/> |<span data-ttu-id="a95f5-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a95f5-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a95f5-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="a95f5-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a95f5-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="a95f5-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="a95f5-113">Access:</span><span class="sxs-lookup"><span data-stu-id="a95f5-113">Access:</span></span>  <br/> |<span data-ttu-id="a95f5-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a95f5-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a95f5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a95f5-115">Remarks</span></span>

<span data-ttu-id="a95f5-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a95f5-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="a95f5-117">Wenn der Client versucht, diese Eigenschaft nicht festlegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="a95f5-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="a95f5-118">Diese Eigenschaft unterscheidet sich von [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) , dessen Wert nur für alle Konten innerhalb dieses Profil, in dem das Konto erstellt wurde, eindeutig, sind während die **Eigenschaft\_ACCT_MINI_UID** eindeutig identifiziert den Account innerhalb und außerhalb des Profils ein, in dem das Konto erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a95f5-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="a95f5-119">Wenn eine Nachricht mit diesen Eigenschaften auf einem zweiten Computer mit einem anderen Outlook-Profil wechselt und andere Menge von Konten, **PROP_ACCT_ID** möglicherweise kann Konflikte mit einem Konto im Profil des zweiten Computer und **PROP_ACCT_MINI_UID** das ursprüngliche Konto im ursprünglichen Profil können eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a95f5-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a95f5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a95f5-120">See also</span></span>

- [<span data-ttu-id="a95f5-121">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="a95f5-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a95f5-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="a95f5-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

