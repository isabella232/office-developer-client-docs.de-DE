---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Gibt die primäre Accountsendstamp für eine Nachricht an.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791177"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="ab9c3-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="ab9c3-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="ab9c3-104">Gibt die primäre Konto "Senden" Zeitstempel für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="ab9c3-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ab9c3-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ab9c3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab9c3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab9c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab9c3-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ab9c3-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="ab9c3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ab9c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab9c3-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="ab9c3-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="ab9c3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab9c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab9c3-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab9c3-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab9c3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab9c3-112">Area:</span></span>  <br/> |<span data-ttu-id="ab9c3-113">Konto</span><span class="sxs-lookup"><span data-stu-id="ab9c3-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab9c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab9c3-114">Remarks</span></span>

<span data-ttu-id="ab9c3-115">Diese Eigenschaft gilt für ein MAPI-Message-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab9c3-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="ab9c3-116">Bei einer empfangenen Nachricht gibt der primäre Konto Stempel "Senden" welches Konto eine Forward- oder eine Antwort mit gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab9c3-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="ab9c3-117">Für eine ausgehende Nachricht an bestimmt, welches Konto zum Senden der Nachricht mit.</span><span class="sxs-lookup"><span data-stu-id="ab9c3-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="ab9c3-118">Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos ein, mit denen die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab9c3-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab9c3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab9c3-119">See also</span></span>

- [<span data-ttu-id="ab9c3-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="ab9c3-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="ab9c3-121">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab9c3-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="ab9c3-122">PidTagPrimarySendAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab9c3-122">PidTagPrimarySendAccount Canonical Property</span></span>](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

