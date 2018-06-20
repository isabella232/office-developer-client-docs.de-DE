---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Stellt eine ACCT_BIN-Struktur, die UID des ein Exchange-Konto enthält.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791211"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="b8f83-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="b8f83-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="b8f83-104">Stellt eine [ACCT_BIN](acct_bin.md) -Struktur, die UID des ein Exchange-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="b8f83-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b8f83-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b8f83-105">Quick info</span></span>

<span data-ttu-id="b8f83-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b8f83-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8f83-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b8f83-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b8f83-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="b8f83-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="b8f83-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="b8f83-109">Property type:</span></span>  <br/> |<span data-ttu-id="b8f83-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b8f83-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b8f83-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="b8f83-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b8f83-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="b8f83-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="b8f83-113">Access:</span><span class="sxs-lookup"><span data-stu-id="b8f83-113">Access:</span></span>  <br/> |<span data-ttu-id="b8f83-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b8f83-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8f83-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8f83-115">Remarks</span></span>

<span data-ttu-id="b8f83-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="b8f83-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="b8f83-117">Verwenden Sie [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) , um sicherzustellen, wenn das Konto ein Exchange-Konto ist.</span><span class="sxs-lookup"><span data-stu-id="b8f83-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="b8f83-118">Wenn dies der Fall, **Eigenschaft\_MAPI_EMSMDB_UID** ist eine **ACCT_BIN** , die die **EmsmdbUID**enthält, die die eindeutige ID, für die Exchange-Konto ist.</span><span class="sxs-lookup"><span data-stu-id="b8f83-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="b8f83-119">Wenn das Konto nicht um ein Exchange-Konto handelt, ist diese Eigenschaft nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b8f83-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8f83-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8f83-120">See also</span></span>

- [<span data-ttu-id="b8f83-121">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="b8f83-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="b8f83-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b8f83-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="b8f83-123">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="b8f83-123">Using Multiple Exchange Accounts</span></span>](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="b8f83-124">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b8f83-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)
