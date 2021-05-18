---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Stellt eine ACCT_BIN, die die UID eines Exchange-Kontos enthält.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326551"
---
# <a name="prop_mapi_emsmdb_uid"></a><span data-ttu-id="65e00-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="65e00-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="65e00-104">Stellt eine [ACCT_BIN,](acct_bin.md) die die UID eines Exchange-Kontos enthält.</span><span class="sxs-lookup"><span data-stu-id="65e00-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="65e00-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="65e00-105">Quick info</span></span>

<span data-ttu-id="65e00-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="65e00-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65e00-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="65e00-107">Identifier:</span></span>  <br/> |<span data-ttu-id="65e00-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="65e00-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="65e00-109">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="65e00-109">Property type:</span></span>  <br/> |<span data-ttu-id="65e00-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="65e00-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="65e00-111">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="65e00-111">Property tag:</span></span>  <br/> |<span data-ttu-id="65e00-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="65e00-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="65e00-113">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="65e00-113">Access:</span></span>  <br/> |<span data-ttu-id="65e00-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65e00-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65e00-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65e00-115">Remarks</span></span>

<span data-ttu-id="65e00-116">Diese Eigenschaft mithilfe von [IOlkAccount::GetProp erhalten.](iolkaccount-getprop.md)</span><span class="sxs-lookup"><span data-stu-id="65e00-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="65e00-117">Verwenden [PROP_ACCT_IS_EXCH,](prop_acct_is_exch.md) um zu überprüfen, ob es sich bei dem Konto um ein Exchange-Konto handelt.</span><span class="sxs-lookup"><span data-stu-id="65e00-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="65e00-118">Wenn dies **\_ der** MAPI_EMSMDB_UID ist,  ist prop ACCT_BIN, das **die emsmdbUID** enthält, die die eindeutige ID für das Exchange-Konto ist.</span><span class="sxs-lookup"><span data-stu-id="65e00-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="65e00-119">Wenn es sich bei dem Konto nicht um ein Exchange-Konto handelt, ist diese Eigenschaft nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="65e00-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65e00-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65e00-120">See also</span></span>

- [<span data-ttu-id="65e00-121">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="65e00-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="65e00-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="65e00-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="65e00-123">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="65e00-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="65e00-124">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="65e00-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

