---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils, in dem das Konto erstellt wird, eindeutig identifiziert.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407165"
---
# <a name="prop_acct_id"></a><span data-ttu-id="b4182-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="b4182-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="b4182-104">Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils, in dem das Konto erstellt wird, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b4182-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b4182-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b4182-105">Quick info</span></span>

<span data-ttu-id="b4182-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b4182-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4182-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b4182-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b4182-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="b4182-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="b4182-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="b4182-109">Property type:</span></span>  <br/> |<span data-ttu-id="b4182-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4182-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4182-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="b4182-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b4182-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="b4182-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="b4182-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="b4182-113">Access:</span></span>  <br/> |<span data-ttu-id="b4182-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4182-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4182-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4182-115">Remarks</span></span>

<span data-ttu-id="b4182-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)</span><span class="sxs-lookup"><span data-stu-id="b4182-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="b4182-117">Wenn der Client versucht, diese Eigenschaft zu setzen, gibt diese Eigenschaft **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="b4182-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="b4182-118">Diese Eigenschaft ist anders als [PROP_ACCT_MINI_UID,](prop_acct_mini_uid.md) da ihr Wert nur für alle Konten innerhalb des Profils eindeutig ist, in dem das Konto erstellt wurde, während **PROP \_ ACCT_MINI_UID** das Konto innerhalb und außerhalb des Profils, in dem das Konto erstellt wurde, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b4182-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="b4182-119">Wenn eine Nachricht mit diesen Eigenschaften auf einen zweiten Computer mit einem anderen Outlook-Profil und unterschiedlichen Konten streift, kann **PROP_ACCT_ID** möglicherweise mit einem Konto im Profil des zweiten Computers in Konflikt stehen, und **PROP_ACCT_MINI_UID** kann das ursprüngliche Konto im ursprünglichen Profil eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b4182-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4182-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4182-120">See also</span></span>

- [<span data-ttu-id="b4182-121">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="b4182-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="b4182-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b4182-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

