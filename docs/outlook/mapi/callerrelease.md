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
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568128"
---
# <a name="callerrelease"></a><span data-ttu-id="5f610-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="5f610-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="5f610-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f610-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f610-105">Definiert eine Rückruffunktion, die ein Table-Datenobjekt freigeben kann, wenn eine Tabellenansicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f610-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f610-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5f610-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f610-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5f610-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5f610-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="5f610-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5f610-109">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5f610-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5f610-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="5f610-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5f610-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5f610-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="5f610-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f610-112">Parameters</span></span>

 <span data-ttu-id="5f610-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="5f610-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="5f610-114">[in] Anrufer-Daten mit der Tabellenansicht MAPI gespeichert und an die **CALLERRELEASE** übergebenen basieren Callback-Funktion.</span><span class="sxs-lookup"><span data-stu-id="5f610-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="5f610-115">Die Daten enthält Kontext über die Tabellenansicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f610-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="5f610-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="5f610-116">_lpTblData_</span></span>
  
> <span data-ttu-id="5f610-117">[in] Zeiger auf die [ITableData: IUnknown](itabledataiunknown.md) Schnittstelle für die Tabelle Datenobjekt zugrunde liegenden der Tabellenansicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f610-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="5f610-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="5f610-118">_lpVue_</span></span>
  
> <span data-ttu-id="5f610-119">[in] Zeiger auf die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle für die Tabellenansicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f610-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="5f610-120">Dies ist eine Schnittstelle für das Table-Objekt zurückgegeben, die im Parameter _LppMAPITable_ der [ITableData::HrGetView](itabledata-hrgetview.md) -Methode, die das freizugebende-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f610-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f610-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5f610-121">Return value</span></span>

<span data-ttu-id="5f610-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5f610-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5f610-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f610-123">Remarks</span></span>

<span data-ttu-id="5f610-124">Eine Clientanwendung oder Dienstanbieter, die ein Table-Datenobjekt gefüllt wurde kann [ITableData::HrGetView](itabledata-hrgetview.md) zum Erstellen einer Ansicht, sortierten der Tabelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5f610-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="5f610-125">Der Anruf an **HrGetView** übergibt einen Zeiger auf eine Rückruffunktion **CALLERRELEASE** basiert und auch einen Kontext mit der Tabellenansicht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f610-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="5f610-126">Wenn der Tabellenansicht der Referenzzähler gibt 0 (null) zurück, und die Ansicht wird veröffentlicht, ruft die **IMAPITable** -Implementierung die Callback-Funktion, die im Kontext der _UlCallerData_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f610-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="5f610-127">Eine häufige Verwendung von einer Rückruffunktion **CALLERRELEASE** basierend ist zum Freigeben des zugrunde liegenden Daten Tabellenobjekts und keinen verfolgen sie bei der nachfolgenden Verarbeitung an.</span><span class="sxs-lookup"><span data-stu-id="5f610-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

