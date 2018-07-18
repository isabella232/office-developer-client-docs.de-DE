---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Ruft ab oder legt die Address Book Eintrags-ID für das Konto.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791191"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="10091-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="10091-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="10091-104">Ruft ab oder legt die Address Book Eintrags-ID für das Konto.</span><span class="sxs-lookup"><span data-stu-id="10091-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="10091-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="10091-105">Quick info</span></span>

<span data-ttu-id="10091-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="10091-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10091-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="10091-107">Identifier:</span></span>  <br/> |<span data-ttu-id="10091-108">0 x 2002</span><span class="sxs-lookup"><span data-stu-id="10091-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="10091-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="10091-109">Property type:</span></span>  <br/> |<span data-ttu-id="10091-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="10091-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="10091-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="10091-111">Property tag:</span></span>  <br/> |<span data-ttu-id="10091-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="10091-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="10091-113">Access:</span><span class="sxs-lookup"><span data-stu-id="10091-113">Access:</span></span>  <br/> |<span data-ttu-id="10091-114">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="10091-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10091-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10091-115">Remarks</span></span>

 <span data-ttu-id="10091-116">**Eigenschaft\_MAPI\_Identität\_ENTRYID** voraussichtlich nicht auf jedem Konto vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="10091-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="10091-117">Beispielsweise könnte ein Exchange-Konto haben **Eigenschaft\_MAPI\_Identität\_ENTRYID** festgelegt und nicht [Eigenschaft\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), während für ein SMTP/POP3-Konto die Situation umgekehrt wurde.</span><span class="sxs-lookup"><span data-stu-id="10091-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="10091-118">**Eigenschaft\_MAPI_IDENTITY_ENTRYID** gibt eine Eintrags-ID, die auf den Wert von _LppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)zurückgegebene ähnlich ist.</span><span class="sxs-lookup"><span data-stu-id="10091-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10091-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10091-119">See also</span></span>

- [<span data-ttu-id="10091-120">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="10091-120">About the Account Management API</span></span>](about-the-account-management-api.md)

