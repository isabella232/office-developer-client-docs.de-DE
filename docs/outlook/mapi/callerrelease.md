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
# <a name="callerrelease"></a><span data-ttu-id="e3080-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="e3080-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="e3080-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3080-105">Definiert eine Rückruffunktion, mit der ein Tabellendatenobjekt freigegeben werden kann, wenn eine Tabellenansicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3080-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3080-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e3080-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3080-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e3080-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e3080-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e3080-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e3080-109">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e3080-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="e3080-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="e3080-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e3080-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e3080-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="e3080-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3080-112">Parameters</span></span>

 <span data-ttu-id="e3080-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e3080-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="e3080-114">[in] Anruferdaten, die von MAPI mit der Tabellenansicht gespeichert und an die **CALLERRELEASE-basierte** Rückruffunktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3080-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="e3080-115">Die Daten bieten Kontext zur freigegebenen Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="e3080-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="e3080-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="e3080-116">_lpTblData_</span></span>
  
> <span data-ttu-id="e3080-117">[in] Zeiger auf die [ITableData : IUnknown-Schnittstelle](itabledataiunknown.md) für das Tabellendatenobjekt, das der freigegebenen Tabellenansicht zugrunde liegt.</span><span class="sxs-lookup"><span data-stu-id="e3080-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="e3080-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="e3080-118">_lpVue_</span></span>
  
> <span data-ttu-id="e3080-119">[in] Zeiger auf die [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) für die tabellenansicht, die freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3080-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="e3080-120">Dies ist eine Schnittstelle für das Tabellenobjekt, das im  _lppMAPITable-Parameter_ der [ITableData::HrGetView-Methode](itabledata-hrgetview.md) zurückgegeben wird, die das zu veröffentlichende Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="e3080-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e3080-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3080-121">Return value</span></span>

<span data-ttu-id="e3080-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e3080-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3080-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3080-123">Remarks</span></span>

<span data-ttu-id="e3080-124">Eine Clientanwendung oder ein Dienstanbieter, der ein Tabellendatenobjekt aufgefüllt hat, kann [ITableData::HrGetView](itabledata-hrgetview.md) aufrufen, um eine schreibgeschützte, sortierte Ansicht der Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e3080-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="e3080-125">Der Aufruf von **HrGetView** übergibt einen Zeiger an eine **CALLERRELEASE-basierte** Rückruffunktion und auch einen Kontext, der mit der Tabellenansicht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3080-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="e3080-126">Wenn die Referenzanzahl der Tabellenansicht auf Null zurückkehrt und die Ansicht freigegeben wird, ruft die **IMAPITable-Implementierung** die Rückruffunktion auf und übergibt den Kontext im _ulCallerData-Parameter._</span><span class="sxs-lookup"><span data-stu-id="e3080-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="e3080-127">Eine häufige Verwendung einer **CALLERRELEASE-basierten** Rückruffunktion besteht in der Freigabe des zugrunde liegenden Tabellendatenobjekts und muss während der nachfolgenden Verarbeitung nicht nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="e3080-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

