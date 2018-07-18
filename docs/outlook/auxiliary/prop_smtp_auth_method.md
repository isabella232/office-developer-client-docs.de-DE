---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode für die SMTP-Konto verwenden.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791206"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="ae2fe-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="ae2fe-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="ae2fe-104">Gibt die Authentifizierungsmethode für die SMTP-Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ae2fe-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ae2fe-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae2fe-106">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ae2fe-106">Identifier:</span></span>  <br/> |<span data-ttu-id="ae2fe-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="ae2fe-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="ae2fe-108">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="ae2fe-108">Property type:</span></span>  <br/> |<span data-ttu-id="ae2fe-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="ae2fe-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="ae2fe-110">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="ae2fe-110">Property tag:</span></span>  <br/> |<span data-ttu-id="ae2fe-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="ae2fe-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="ae2fe-112">Access:</span><span class="sxs-lookup"><span data-stu-id="ae2fe-112">Access:</span></span>  <br/> |<span data-ttu-id="ae2fe-113">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae2fe-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2fe-114">Remarks</span></span>

<span data-ttu-id="ae2fe-115">Der Wert ist eine Bitmaske der folgenden Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="ae2fe-116">Ihren Werten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2fe-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="ae2fe-117">**SMTP_AUTH_SAME_AS_POP** bedeutet als Posteingangsserver, die dieselben Anmeldeinformationen verwenden, wie von [PROP_INET_USER](prop_inet_user.md) und [PROP_INET_PASSWORD](prop_inet_password.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="ae2fe-118">**SMTP_AUTH_USER_PASS** bedeutet, dass mit den Anmeldeinformationen von [PROP_SMTP_USER](prop_smtp_user.md) und [PROP_SMTP_PASSWORD](prop_smtp_password.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="ae2fe-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** bedeutet, dass den Benutzer zum Server für eingehende e-Mail-Nachrichten melden Sie sich vor dem Senden von e-Mail-Nachrichten anfordern.</span><span class="sxs-lookup"><span data-stu-id="ae2fe-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ae2fe-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae2fe-120">See also</span></span>

- [<span data-ttu-id="ae2fe-121">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="ae2fe-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="ae2fe-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="ae2fe-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

