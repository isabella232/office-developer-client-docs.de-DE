---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Stellt die Eintrags-ID des Standard Zustellungs Speichers für das Konto dar.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327671"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="89d74-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="89d74-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="89d74-104">Stellt die Eintrags-ID des Standard Zustellungs Speichers für das Konto dar.</span><span class="sxs-lookup"><span data-stu-id="89d74-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89d74-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="89d74-105">Quick info</span></span>

<span data-ttu-id="89d74-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="89d74-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89d74-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="89d74-107">Identifier:</span></span>  <br/> |<span data-ttu-id="89d74-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="89d74-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="89d74-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="89d74-109">Property type:</span></span>  <br/> |<span data-ttu-id="89d74-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="89d74-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="89d74-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="89d74-111">Property tag:</span></span>  <br/> |<span data-ttu-id="89d74-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="89d74-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="89d74-113">Access</span><span class="sxs-lookup"><span data-stu-id="89d74-113">Access:</span></span>  <br/> |<span data-ttu-id="89d74-114">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89d74-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89d74-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d74-115">Remarks</span></span>

<span data-ttu-id="89d74-116">Abrufen oder Festlegen dieser Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md) oder [IOlkAccount:: setprop](iolkaccount-setprop.md), beziehungsweise.</span><span class="sxs-lookup"><span data-stu-id="89d74-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="89d74-117">Einer der Nebeneffekte beim Festlegen eines Speichers als standardmäßiger Zustellungs Speicher für ein Konto besteht darin, dass Outlook beim Start von Outlook Suchordner für diesen Speicher erstellt, sofern Sie noch nicht vorhanden sind, und den Informationsspeicher in der Aufgabenleiste auflisten.</span><span class="sxs-lookup"><span data-stu-id="89d74-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89d74-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89d74-118">See also</span></span>

- [<span data-ttu-id="89d74-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="89d74-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="89d74-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="89d74-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

