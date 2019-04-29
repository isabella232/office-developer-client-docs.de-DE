---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408726"
---
# <a name="callerrelease"></a><span data-ttu-id="13238-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="13238-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="13238-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13238-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13238-105">Definiert eine Rückruffunktion, die ein Tabellendaten Objekt freigeben kann, wenn eine Tabellenansicht veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="13238-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13238-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13238-106">Header file:</span></span>  <br/> |<span data-ttu-id="13238-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="13238-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="13238-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="13238-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="13238-109">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="13238-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="13238-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="13238-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="13238-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="13238-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="13238-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13238-112">Parameters</span></span>

 <span data-ttu-id="13238-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="13238-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="13238-114">in Von MAPI gespeicherte Anrufer-Daten in der Tabellenansicht und an die **CALLERRELEASE** -basierte Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="13238-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="13238-115">Die Daten liefern Kontext über die Tabellenansicht, die freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13238-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="13238-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="13238-116">_lpTblData_</span></span>
  
> <span data-ttu-id="13238-117">in Zeiger auf die [ITableData: IUnknown](itabledataiunknown.md) -Schnittstelle für das Tabellendaten Objekt, das der Tabellenansicht zugrunde liegt, die freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13238-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="13238-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="13238-118">_lpVue_</span></span>
  
> <span data-ttu-id="13238-119">in Zeiger auf die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle für die Tabellenansicht, die freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13238-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="13238-120">Hierbei handelt es sich um eine Schnittstelle für das Table-Objekt, das im _lppMAPITable_ -Parameter der [ITableData:: HrGetView](itabledata-hrgetview.md) -Methode zurückgegeben wird, die das Release-Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="13238-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13238-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13238-121">Return value</span></span>

<span data-ttu-id="13238-122">Keine</span><span class="sxs-lookup"><span data-stu-id="13238-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13238-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13238-123">Remarks</span></span>

<span data-ttu-id="13238-124">Eine Clientanwendung oder ein Dienstanbieter, der ein Tabellendaten Objekt aufgefüllt hat, kann [ITableData:: HrGetView](itabledata-hrgetview.md) aufrufen, um eine schreibgeschützte, sortierte Ansicht der Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13238-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="13238-125">Der Aufruf von **HrGetView** übergibt einen Zeiger auf eine **CALLERRELEASE** -basierte Rückruffunktion und auch einen Kontext, der mit der Tabellenansicht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="13238-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="13238-126">Wenn der Verweiszähler der Tabellenansicht auf Null zurückgesetzt wird und die Ansicht veröffentlicht wird, ruft die **IMAPITable** -Implementierung die Rückruffunktion auf und übergibt den Kontext im _ulCallerData_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="13238-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="13238-127">Eine häufige Verwendung einer **CALLERRELEASE** -basierten Rückruffunktion besteht darin, das zugrunde liegende Tabellendaten Objekt freizusetzen und es während der nachfolgenden Verarbeitung nicht nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="13238-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

