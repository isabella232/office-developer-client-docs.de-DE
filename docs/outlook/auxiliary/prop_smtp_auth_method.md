---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode für das SMTP-Konto an.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326502"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="41a0d-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="41a0d-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="41a0d-104">Gibt die Authentifizierungsmethode für das SMTP-Konto an.</span><span class="sxs-lookup"><span data-stu-id="41a0d-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="41a0d-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="41a0d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41a0d-106">Kennung:</span><span class="sxs-lookup"><span data-stu-id="41a0d-106">Identifier:</span></span>  <br/> |<span data-ttu-id="41a0d-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="41a0d-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="41a0d-108">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="41a0d-108">Property type:</span></span>  <br/> |<span data-ttu-id="41a0d-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="41a0d-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="41a0d-110">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="41a0d-110">Property tag:</span></span>  <br/> |<span data-ttu-id="41a0d-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="41a0d-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="41a0d-112">Access</span><span class="sxs-lookup"><span data-stu-id="41a0d-112">Access:</span></span>  <br/> |<span data-ttu-id="41a0d-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41a0d-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41a0d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a0d-114">Remarks</span></span>

<span data-ttu-id="41a0d-115">Der Wert ist eine Bitmaske der folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="41a0d-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="41a0d-116">Ihre Werte finden Sie unter [Constants (Account Management API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="41a0d-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="41a0d-117">**SMTP_AUTH_SAME_AS_POP** ist die Verwendung derselben Anmeldeinformationen wie mein Posteingangsserver, wie von [PROP_INET_USER](prop_inet_user.md) und [PROP_INET_PASSWORD](prop_inet_password.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="41a0d-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="41a0d-118">**SMTP_AUTH_USER_PASS** ist die Verwendung der Anmeldeinformationen, die von [PROP_SMTP_USER](prop_smtp_user.md) und [PROP_SMTP_PASSWORD](prop_smtp_password.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="41a0d-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="41a0d-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** : fordert den Benutzer auf, sich vor dem Senden von e-Mails beim Posteingangsserver anzumelden.</span><span class="sxs-lookup"><span data-stu-id="41a0d-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="41a0d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a0d-120">See also</span></span>

- [<span data-ttu-id="41a0d-121">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="41a0d-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="41a0d-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="41a0d-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

