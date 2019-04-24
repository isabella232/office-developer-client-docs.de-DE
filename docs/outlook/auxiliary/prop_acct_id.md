---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327657"
---
# <a name="propacctid"></a><span data-ttu-id="be749-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="be749-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="be749-104">Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="be749-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="be749-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="be749-105">Quick info</span></span>

<span data-ttu-id="be749-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="be749-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be749-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="be749-107">Identifier:</span></span>  <br/> |<span data-ttu-id="be749-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="be749-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="be749-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="be749-109">Property type:</span></span>  <br/> |<span data-ttu-id="be749-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be749-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be749-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="be749-111">Property tag:</span></span>  <br/> |<span data-ttu-id="be749-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="be749-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="be749-113">Access</span><span class="sxs-lookup"><span data-stu-id="be749-113">Access:</span></span>  <br/> |<span data-ttu-id="be749-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be749-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be749-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be749-115">Remarks</span></span>

<span data-ttu-id="be749-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab.</span><span class="sxs-lookup"><span data-stu-id="be749-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="be749-117">Wenn der Client versucht, diese Eigenschaft festzulegen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**zurück.</span><span class="sxs-lookup"><span data-stu-id="be749-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="be749-118">Diese Eigenschaft unterscheidet sich von [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) dadurch, dass ihr Wert nur unter allen Konten innerhalb dieses Profils eindeutig ist, in dem das Konto erstellt wurde, während **Prop\_ACCT_MINI_UID** das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="be749-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="be749-119">Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten Sätzen wechselt, kann **PROP_ACCT_ID** möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen, und **PROP_ACCT_MINI_UID** das ursprüngliche Konto kann eindeutig im ursprünglichen Profil identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="be749-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be749-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be749-120">See also</span></span>

- [<span data-ttu-id="be749-121">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="be749-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="be749-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="be749-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

