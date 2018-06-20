---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Erstellt ein Objekt, das ein Client zugreifen kann in einem bevorzugten Zeichenformat.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790942"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="c32e3-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="c32e3-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="c32e3-104">Erstellt ein Objekt, das ein Client zugreifen kann in einem bevorzugten Zeichenformat.</span><span class="sxs-lookup"><span data-stu-id="c32e3-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c32e3-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c32e3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c32e3-106">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="c32e3-106">Exported by:</span></span>  <br/> |<span data-ttu-id="c32e3-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c32e3-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c32e3-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c32e3-108">Called by:</span></span>  <br/> |<span data-ttu-id="c32e3-109">Client</span><span class="sxs-lookup"><span data-stu-id="c32e3-109">Client</span></span>  <br/> |
|<span data-ttu-id="c32e3-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c32e3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c32e3-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="c32e3-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="c32e3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c32e3-112">Parameters</span></span>

<span data-ttu-id="c32e3-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="c32e3-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="c32e3-114">[in] Das ursprüngliche allein stehenden Outlook-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c32e3-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="c32e3-115">Muss eine der folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="c32e3-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="c32e3-116">[IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), oder [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c32e3-116">[IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="c32e3-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="c32e3-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="c32e3-118">[in] Kennzeichen, die das ursprüngliche allein stehenden Objekt charakterisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c32e3-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="c32e3-119">Eine oder mehrere der folgenden Werte muss sein:</span><span class="sxs-lookup"><span data-stu-id="c32e3-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="c32e3-120">DDLWRAP_FLAG_ANSI – Unwrapped-Objekt ist ANSI.</span><span class="sxs-lookup"><span data-stu-id="c32e3-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="c32e3-121">DDLWRAP_FLAG_UNICODE – Unwrapped-Objekt ist UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c32e3-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="c32e3-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="c32e3-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="c32e3-123">[in] Flags für die bevorzugten Zeichenformat.</span><span class="sxs-lookup"><span data-stu-id="c32e3-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="c32e3-124">Eine oder mehrere der folgenden Werte muss sein:</span><span class="sxs-lookup"><span data-stu-id="c32e3-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="c32e3-125">DDLWRAP_FLAG_ANSI – Wrapped-Objekt wird als ANSI verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="c32e3-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="c32e3-126">DDLWRAP_FLAG_UNICODE – Wrapped-Objekt wird als UNICODE verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="c32e3-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="c32e3-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="c32e3-127">_pIID_</span></span>
  
>  <span data-ttu-id="c32e3-128">[in] Der Bezeichner der Schnittstelle, durch die allein stehenden-Objekt unterstützt; Legen Sie es auf NULL, wenn dies nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c32e3-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="c32e3-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="c32e3-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="c32e3-130">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c32e3-130">[in] This parameter is not used.</span></span> <span data-ttu-id="c32e3-131">Es muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c32e3-131">It must be NULL.</span></span> 
    
<span data-ttu-id="c32e3-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="c32e3-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="c32e3-133">[in] Legen Sie diesen Parameter auf **true fest,** Wenn _PvUnwrapped_ auf seinem Format vor Umbruch überprüft werden soll; Legen Sie ihn auf **false fest** , wenn das Objekt ohne Überprüfung umbrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c32e3-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="c32e3-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="c32e3-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="c32e3-135">[out] Ein Zeiger auf das angeforderte Objekt, in das angeforderte Zeichenformat eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c32e3-136">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c32e3-136">Return values</span></span>

<span data-ttu-id="c32e3-137">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c32e3-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c32e3-138">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="c32e3-138">Remarks</span></span>

<span data-ttu-id="c32e3-139">Ein Objekt allein stehenden führt übergeben in einem gepackten-Objekt mit _fCheckWrap_ auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c32e3-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="c32e3-140">Unabhängig davon, ob das zurückgegebene Objekt umgebrochen wird muss der Client für den Verweis auf das zurückgegebene Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="c32e3-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="c32e3-141">Wenn **GetProcAddress** für die Adresse des dieser Funktion in msmapi32.dll suchen, geben Sie **HrCreateNewWrappedObject@28** als den Namen der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c32e3-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c32e3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c32e3-142">See also</span></span>

- [<span data-ttu-id="c32e3-143">Über der Datenschicht Abbau API</span><span class="sxs-lookup"><span data-stu-id="c32e3-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="c32e3-144">Konstanten (Beeinträchtigung Datenebene API)</span><span class="sxs-lookup"><span data-stu-id="c32e3-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

