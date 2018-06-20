---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Stellt transporteinstellungen, die Outlook verwendet, um die erforderlichen Aufgaben zu ermitteln und die Elemente der Benutzeroberfläche (UI) zu deaktivieren, die das Konto nicht unterstützt.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791192"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="44c30-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="44c30-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="44c30-104">Stellt transporteinstellungen, die Outlook verwendet, um die erforderlichen Aufgaben zu ermitteln und die Elemente der Benutzeroberfläche (UI) zu deaktivieren, die das Konto nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44c30-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="44c30-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="44c30-105">Quick info</span></span>

<span data-ttu-id="44c30-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="44c30-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44c30-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="44c30-107">Identifier:</span></span>  <br/> |<span data-ttu-id="44c30-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="44c30-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="44c30-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="44c30-109">Property type:</span></span>  <br/> |<span data-ttu-id="44c30-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="44c30-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="44c30-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="44c30-111">Property tag:</span></span>  <br/> |<span data-ttu-id="44c30-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="44c30-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="44c30-113">Access:</span><span class="sxs-lookup"><span data-stu-id="44c30-113">Access:</span></span>  <br/> |<span data-ttu-id="44c30-114">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="44c30-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44c30-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44c30-115">Remarks</span></span>

<span data-ttu-id="44c30-116">Abrufen Sie oder festlegen Sie dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp](iolkaccount-setprop.md), jeweils.</span><span class="sxs-lookup"><span data-stu-id="44c30-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="44c30-117">Gibt **MAPIACCT_SEND_ONLY** zurück, wenn das Konto nur Nachrichten senden kann, jedoch keine Nachrichten empfangen.</span><span class="sxs-lookup"><span data-stu-id="44c30-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="44c30-118">In diesem Fall wird Outlook Benutzeroberfläche, die auf diese Art von Konten (beispielsweise die Benutzeroberfläche für **Senden/Empfangen**) nicht anwendbar ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="44c30-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44c30-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44c30-119">See also</span></span>

- [<span data-ttu-id="44c30-120">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="44c30-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="44c30-121">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="44c30-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

