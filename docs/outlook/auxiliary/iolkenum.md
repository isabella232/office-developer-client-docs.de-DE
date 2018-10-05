---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389736"
---
# <a name="iolkenum"></a><span data-ttu-id="adf43-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="adf43-102">IOlkEnum</span></span>

<span data-ttu-id="adf43-103">Aufzählen von Konten als [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adf43-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="adf43-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="adf43-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adf43-105">Erbt:</span><span class="sxs-lookup"><span data-stu-id="adf43-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="adf43-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="adf43-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="adf43-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="adf43-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="adf43-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="adf43-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="adf43-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="adf43-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="adf43-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="adf43-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="adf43-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="adf43-111">Called by:</span></span>  <br/> |<span data-ttu-id="adf43-112">Client</span><span class="sxs-lookup"><span data-stu-id="adf43-112">Client</span></span>  <br/> |
|<span data-ttu-id="adf43-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="adf43-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="adf43-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="adf43-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="adf43-115">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="adf43-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="adf43-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="adf43-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="adf43-117">Ruft die Anzahl von Konten in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="adf43-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="adf43-118">Reset</span><span class="sxs-lookup"><span data-stu-id="adf43-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="adf43-119">Setzt den Enumerator auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="adf43-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="adf43-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="adf43-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="adf43-121">Ruft das nächste Konto in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="adf43-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="adf43-122">Überspringen</span><span class="sxs-lookup"><span data-stu-id="adf43-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="adf43-123">Überspringt eine angegebene Anzahl von Konten in den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="adf43-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adf43-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="adf43-124">Remarks</span></span>

<span data-ttu-id="adf43-125">Diese Schnittstelle wird von **IOlkAccountManager::EnumerateAccounts** zurückgegeben, wenn einen Enumerator von Konten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adf43-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adf43-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adf43-126">See also</span></span>

- [<span data-ttu-id="adf43-127">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="adf43-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="adf43-128">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="adf43-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

