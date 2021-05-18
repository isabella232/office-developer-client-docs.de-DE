---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Gibt den primären Accountsendstamp für eine Nachricht an.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327706"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="ecca3-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="ecca3-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="ecca3-104">Gibt den primären Kontostempel "Senden" für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="ecca3-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ecca3-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ecca3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ecca3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ecca3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecca3-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ecca3-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="ecca3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ecca3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecca3-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="ecca3-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="ecca3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ecca3-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecca3-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecca3-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecca3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ecca3-112">Area:</span></span>  <br/> |<span data-ttu-id="ecca3-113">Konto</span><span class="sxs-lookup"><span data-stu-id="ecca3-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecca3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecca3-114">Remarks</span></span>

<span data-ttu-id="ecca3-115">Diese Eigenschaft gilt für ein MAPI-Nachrichtenobjekt.</span><span class="sxs-lookup"><span data-stu-id="ecca3-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="ecca3-116">Für eine empfangene Nachricht gibt der primäre Kontostempel "Senden" an, mit welchem Konto eine Weiterleitung oder eine Antwort gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecca3-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="ecca3-117">Für eine ausgehende Nachricht bestimmt sie, mit welchem Konto die Nachricht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecca3-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="ecca3-118">Der Wert ist der [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) von der [IOlkAccount-Schnittstelle](iolkaccount.md) des Kontos, mit dem die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecca3-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecca3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecca3-119">See also</span></span>

- [<span data-ttu-id="ecca3-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="ecca3-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="ecca3-121">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecca3-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="ecca3-122">PidTagPrimarySendAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ecca3-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

