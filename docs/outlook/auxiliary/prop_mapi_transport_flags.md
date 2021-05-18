---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt Transporteinstellungen dar Outlook die verwendet werden, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die benutzeroberflächenelemente zu deaktivieren, die vom Konto nicht unterstützt werden.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404526"
---
# <a name="prop_mapi_transport_flags"></a><span data-ttu-id="32a7e-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="32a7e-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="32a7e-104">Stellt Transporteinstellungen dar Outlook die verwendet werden, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die benutzeroberflächenelemente zu deaktivieren, die vom Konto nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="32a7e-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="32a7e-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="32a7e-105">Quick info</span></span>

<span data-ttu-id="32a7e-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="32a7e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32a7e-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="32a7e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="32a7e-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="32a7e-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="32a7e-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="32a7e-109">Property type:</span></span>  <br/> |<span data-ttu-id="32a7e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="32a7e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="32a7e-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="32a7e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="32a7e-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="32a7e-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="32a7e-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="32a7e-113">Access:</span></span>  <br/> |<span data-ttu-id="32a7e-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="32a7e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32a7e-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32a7e-115">Remarks</span></span>

<span data-ttu-id="32a7e-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) bzw. [IOlkAccount::SetProp](iolkaccount-setprop.md)erhalten oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="32a7e-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="32a7e-117">Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden, aber keine Nachrichten empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="32a7e-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="32a7e-118">In diesem Fall deaktiviert Outlook benutzeroberfläche, die nicht für diesen Typ von Konten gilt (z. B. die Benutzeroberfläche für **Senden/Empfangen**).</span><span class="sxs-lookup"><span data-stu-id="32a7e-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32a7e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32a7e-119">See also</span></span>

- [<span data-ttu-id="32a7e-120">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="32a7e-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="32a7e-121">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="32a7e-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

