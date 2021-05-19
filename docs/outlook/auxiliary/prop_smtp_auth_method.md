---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434641"
---
# <a name="prop_smtp_auth_method"></a><span data-ttu-id="7fc74-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="7fc74-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="7fc74-104">Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fc74-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7fc74-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7fc74-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fc74-106">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7fc74-106">Identifier:</span></span>  <br/> |<span data-ttu-id="7fc74-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="7fc74-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="7fc74-108">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="7fc74-108">Property type:</span></span>  <br/> |<span data-ttu-id="7fc74-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="7fc74-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="7fc74-110">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="7fc74-110">Property tag:</span></span>  <br/> |<span data-ttu-id="7fc74-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="7fc74-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="7fc74-112">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="7fc74-112">Access:</span></span>  <br/> |<span data-ttu-id="7fc74-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fc74-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fc74-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fc74-114">Remarks</span></span>

<span data-ttu-id="7fc74-115">Der Wert ist eine Bitmaske der folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="7fc74-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="7fc74-116">Ihre Werte finden Sie unter [Konstanten (Kontoverwaltungs-API).](constants-account-management-api.md)</span><span class="sxs-lookup"><span data-stu-id="7fc74-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="7fc74-117">**SMTP_AUTH_SAME_AS_POP** bedeutet die Verwendung der gleichen Anmeldeinformationen wie mein eingehender E-Mail-Server, wie von PROP_INET_USER [und](prop_inet_user.md) [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="7fc74-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="7fc74-118">**SMTP_AUTH_USER_PASS** bedeutet die Verwendung der Anmeldeinformationen, wie sie von PROP_SMTP_USER [und](prop_smtp_user.md) [PROP_SMTP_PASSWORD.](prop_smtp_password.md)</span><span class="sxs-lookup"><span data-stu-id="7fc74-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="7fc74-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** bedeutet, dass der Benutzer zur Anmeldung beim server für eingehende E-Mails vor dem Senden von E-Mails anfordert.</span><span class="sxs-lookup"><span data-stu-id="7fc74-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7fc74-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fc74-120">See also</span></span>

- [<span data-ttu-id="7fc74-121">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="7fc74-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="7fc74-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="7fc74-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

