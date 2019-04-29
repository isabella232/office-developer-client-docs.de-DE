---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Gibt die e-Mail-Adresse für das Konto an.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436776"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="b6ffd-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="b6ffd-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="b6ffd-104">Gibt die e-Mail-Adresse für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="b6ffd-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b6ffd-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b6ffd-105">Quick info</span></span>

<span data-ttu-id="b6ffd-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b6ffd-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6ffd-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b6ffd-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b6ffd-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="b6ffd-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="b6ffd-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="b6ffd-109">Property type:</span></span>  <br/> |<span data-ttu-id="b6ffd-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6ffd-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b6ffd-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="b6ffd-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b6ffd-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="b6ffd-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="b6ffd-113">Access</span><span class="sxs-lookup"><span data-stu-id="b6ffd-113">Access:</span></span>  <br/> |<span data-ttu-id="b6ffd-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffd-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6ffd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6ffd-115">Remarks</span></span>

 <span data-ttu-id="b6ffd-116">**PROP_ACCT_USER_EMAIL_ADDR** wird nicht in jedem Konto vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b6ffd-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="b6ffd-117">Ein Exchange-Konto kann beispielsweise [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , aber nicht **PROP_ACCT_USER_EMAIL_ADDR**haben, während bei einem SMTP/POP3-Konto die Situation umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="b6ffd-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6ffd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ffd-118">See also</span></span>

- [<span data-ttu-id="b6ffd-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="b6ffd-119">About the Account Management API</span></span>](about-the-account-management-api.md)

