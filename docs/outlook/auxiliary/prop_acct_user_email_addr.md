---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Gibt die e-Mail-Adresse für das Konto an.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791194"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="2a7d0-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="2a7d0-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="2a7d0-104">Gibt die e-Mail-Adresse für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="2a7d0-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2a7d0-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2a7d0-105">Quick info</span></span>

<span data-ttu-id="2a7d0-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2a7d0-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a7d0-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2a7d0-107">Identifier:</span></span>  <br/> |<span data-ttu-id="2a7d0-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="2a7d0-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="2a7d0-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="2a7d0-109">Property type:</span></span>  <br/> |<span data-ttu-id="2a7d0-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a7d0-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2a7d0-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="2a7d0-111">Property tag:</span></span>  <br/> |<span data-ttu-id="2a7d0-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="2a7d0-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="2a7d0-113">Access:</span><span class="sxs-lookup"><span data-stu-id="2a7d0-113">Access:</span></span>  <br/> |<span data-ttu-id="2a7d0-114">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="2a7d0-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a7d0-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a7d0-115">Remarks</span></span>

 <span data-ttu-id="2a7d0-116">**PROP_ACCT_USER_EMAIL_ADDR** voraussichtlich nicht auf jedem Konto vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2a7d0-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="2a7d0-117">Beispielsweise konnte ein Exchange-Konto verfügen, [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) jedoch nicht **PROP_ACCT_USER_EMAIL_ADDR**, während für ein SMTP/POP3-Konto an, die über diese Situation rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="2a7d0-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a7d0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a7d0-118">See also</span></span>

- [<span data-ttu-id="2a7d0-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="2a7d0-119">About the Account Management API</span></span>](about-the-account-management-api.md)

