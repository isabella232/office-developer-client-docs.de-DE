---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Gibt die sekundäre Accountsendstamp für die Nachricht an.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791183"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="6bcd5-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="6bcd5-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="6bcd5-104">Gibt die sekundäre Konto "Senden" für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6bcd5-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6bcd5-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bcd5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6bcd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bcd5-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="6bcd5-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="6bcd5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6bcd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6bcd5-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="6bcd5-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="6bcd5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6bcd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="6bcd5-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6bcd5-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6bcd5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6bcd5-112">Area:</span></span>  <br/> |<span data-ttu-id="6bcd5-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="6bcd5-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bcd5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6bcd5-114">Remarks</span></span>

<span data-ttu-id="6bcd5-115">Diese Eigenschaft gilt für ein MAPI-Message-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="6bcd5-116">Bei einer empfangenen Nachricht gibt der sekundären Konto-Stempel "Senden" welches Konto mit, eine Forward- oder eine Antwort gesendet werden soll, wenn mit das primäre Konto der weiterleiten oder der Antwort gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="6bcd5-117">Für eine ausgehende Nachricht bestimmt sekundäre Konto "Stempel senden" mit welchem Konto zum Senden der Nachricht, wenn die Nachricht mit das primäre Konto gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="6bcd5-118">Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) -Wert aus der [IOlkAccount](iolkaccount.md) -Schnittstelle des Kontos ein, mit denen die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6bcd5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bcd5-119">See also</span></span>

- [<span data-ttu-id="6bcd5-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="6bcd5-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="6bcd5-121">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bcd5-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="6bcd5-122">Kanonische PidTagNextSendAcct-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6bcd5-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

