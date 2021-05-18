---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326432"
---
# <a name="prop_mapi_identity_entryid"></a><span data-ttu-id="374d1-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="374d1-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="374d1-104">Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="374d1-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="374d1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="374d1-105">Quick info</span></span>

<span data-ttu-id="374d1-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="374d1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="374d1-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="374d1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="374d1-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="374d1-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="374d1-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="374d1-109">Property type:</span></span>  <br/> |<span data-ttu-id="374d1-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="374d1-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="374d1-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="374d1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="374d1-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="374d1-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="374d1-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="374d1-113">Access:</span></span>  <br/> |<span data-ttu-id="374d1-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="374d1-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="374d1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="374d1-115">Remarks</span></span>

 <span data-ttu-id="374d1-116">**PROP \_ MAPI \_ IDENTITY \_ ENTRYID** wird nicht für jedes Konto erwartet.</span><span class="sxs-lookup"><span data-stu-id="374d1-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="374d1-117">Ein Exchange-Konto könnte z. B. **PROP \_ MAPI \_ IDENTITY \_ ENTRYID** und nicht [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)festlegen, während für ein SMTP/POP3-Konto die Situation umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="374d1-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="374d1-118">**PROP \_ MAPI_IDENTITY_ENTRYID** gibt eine Eintrags-ID zurück, die dem wert ähnelt, der von _lppEntryID_ in [IMAPISession::QueryIdentity zurückgegeben wird.](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="374d1-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="374d1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="374d1-119">See also</span></span>

- [<span data-ttu-id="374d1-120">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="374d1-120">About the Account Management API</span></span>](about-the-account-management-api.md)

