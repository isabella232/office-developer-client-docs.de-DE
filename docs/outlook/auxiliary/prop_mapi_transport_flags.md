---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt Transporteinstellungen dar, die Outlook zum Ermitteln der erforderlichen Synchronisierungsaufgaben verwendet, und zum Deaktivieren der Benutzeroberflächenelemente, die das Konto nicht unterstützt.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326481"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="4d773-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4d773-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="4d773-104">Stellt Transporteinstellungen dar, die Outlook zum Ermitteln der erforderlichen Synchronisierungsaufgaben verwendet, und zum Deaktivieren der Benutzeroberflächenelemente, die das Konto nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d773-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4d773-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4d773-105">Quick info</span></span>

<span data-ttu-id="4d773-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4d773-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d773-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4d773-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4d773-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="4d773-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="4d773-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="4d773-109">Property type:</span></span>  <br/> |<span data-ttu-id="4d773-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d773-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d773-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="4d773-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4d773-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="4d773-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="4d773-113">Access</span><span class="sxs-lookup"><span data-stu-id="4d773-113">Access:</span></span>  <br/> |<span data-ttu-id="4d773-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4d773-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d773-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d773-115">Remarks</span></span>

<span data-ttu-id="4d773-116">Abrufen oder Festlegen dieser Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md) oder [IOlkAccount:: setprop](iolkaccount-setprop.md), beziehungsweise.</span><span class="sxs-lookup"><span data-stu-id="4d773-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="4d773-117">Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden, aber keine Nachrichten empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="4d773-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="4d773-118">In diesem Fall deaktiviert Outlook die Benutzeroberfläche, die für diese Art von Konten nicht gilt (beispielsweise die Benutzeroberfläche für **senden/empfangen**).</span><span class="sxs-lookup"><span data-stu-id="4d773-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d773-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d773-119">See also</span></span>

- [<span data-ttu-id="4d773-120">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="4d773-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="4d773-121">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="4d773-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

