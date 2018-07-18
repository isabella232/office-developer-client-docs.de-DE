---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791126"
---
# <a name="iolkenum"></a><span data-ttu-id="dd1a8-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="dd1a8-102">IOlkEnum</span></span>

<span data-ttu-id="dd1a8-103">Aufzählen von Konten als [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) -Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="dd1a8-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dd1a8-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd1a8-105">Erbt:</span><span class="sxs-lookup"><span data-stu-id="dd1a8-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="dd1a8-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd1a8-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="dd1a8-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dd1a8-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd1a8-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="dd1a8-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="dd1a8-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="dd1a8-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="dd1a8-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="dd1a8-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="dd1a8-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dd1a8-111">Called by:</span></span>  <br/> |<span data-ttu-id="dd1a8-112">Client</span><span class="sxs-lookup"><span data-stu-id="dd1a8-112">Client</span></span>  <br/> |
|<span data-ttu-id="dd1a8-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="dd1a8-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dd1a8-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="dd1a8-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dd1a8-115">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="dd1a8-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dd1a8-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="dd1a8-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="dd1a8-117">Ruft die Anzahl von Konten in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="dd1a8-118">Reset</span><span class="sxs-lookup"><span data-stu-id="dd1a8-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="dd1a8-119">Setzt den Enumerator auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="dd1a8-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="dd1a8-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="dd1a8-121">Ruft das nächste Konto in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="dd1a8-122">Überspringen</span><span class="sxs-lookup"><span data-stu-id="dd1a8-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="dd1a8-123">Überspringt eine angegebene Anzahl von Konten in den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd1a8-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd1a8-124">Remarks</span></span>

<span data-ttu-id="dd1a8-125">Diese Schnittstelle wird von **IOlkAccountManager::EnumerateAccounts** zurückgegeben, wenn einen Enumerator von Konten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd1a8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd1a8-126">See also</span></span>

- [<span data-ttu-id="dd1a8-127">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="dd1a8-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="dd1a8-128">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="dd1a8-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

