---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Stellt die Eintrags-ID der standardmäßiger übermittlungsspeicher für das Konto an.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791179"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="40e7b-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="40e7b-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="40e7b-104">Stellt die Eintrags-ID der standardmäßiger übermittlungsspeicher für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="40e7b-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="40e7b-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="40e7b-105">Quick info</span></span>

<span data-ttu-id="40e7b-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="40e7b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40e7b-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="40e7b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="40e7b-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="40e7b-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="40e7b-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="40e7b-109">Property type:</span></span>  <br/> |<span data-ttu-id="40e7b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="40e7b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="40e7b-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="40e7b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="40e7b-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="40e7b-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="40e7b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="40e7b-113">Access:</span></span>  <br/> |<span data-ttu-id="40e7b-114">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="40e7b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40e7b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40e7b-115">Remarks</span></span>

<span data-ttu-id="40e7b-116">Abrufen Sie oder festlegen Sie dieser Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md) oder [IOlkAccount::SetProp](iolkaccount-setprop.md), jeweils.</span><span class="sxs-lookup"><span data-stu-id="40e7b-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="40e7b-117">Einer der Nebeneffekte einen Speicher festlegen, wie die standardmäßiger übermittlungsspeicher für ein Konto besteht darin, dass beim Start von Outlook Outlook Suchordner für diesen Speicher, erstellt sofern diese noch nicht vorhanden, und den Informationsspeicher, in der Aufgabenleiste auflisten.</span><span class="sxs-lookup"><span data-stu-id="40e7b-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40e7b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40e7b-118">See also</span></span>

- [<span data-ttu-id="40e7b-119">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="40e7b-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="40e7b-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="40e7b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

