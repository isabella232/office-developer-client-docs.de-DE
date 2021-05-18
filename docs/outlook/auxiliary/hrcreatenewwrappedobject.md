---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317605"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="9bc98-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="9bc98-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="9bc98-104">Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="9bc98-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9bc98-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9bc98-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bc98-106">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="9bc98-106">Exported by:</span></span>  <br/> |<span data-ttu-id="9bc98-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="9bc98-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="9bc98-108">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9bc98-108">Called by:</span></span>  <br/> |<span data-ttu-id="9bc98-109">Client</span><span class="sxs-lookup"><span data-stu-id="9bc98-109">Client</span></span>  <br/> |
|<span data-ttu-id="9bc98-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9bc98-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9bc98-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="9bc98-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9bc98-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bc98-112">Parameters</span></span>

<span data-ttu-id="9bc98-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="9bc98-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="9bc98-114">[in] Das anfängliche unverpackte Outlook Objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc98-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="9bc98-115">Muss eine der folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="9bc98-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="9bc98-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)oder [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9bc98-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="9bc98-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="9bc98-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="9bc98-118">[in] Kennzeichen, die das entpackte anfängliche Objekt kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="9bc98-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="9bc98-119">Muss mindestens einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="9bc98-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="9bc98-120">DDLWRAP_FLAG_ANSI– Unwrapped-Objekt ist ANSI.</span><span class="sxs-lookup"><span data-stu-id="9bc98-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="9bc98-121">DDLWRAP_FLAG_UNICODE– Unwrapped-Objekt ist UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9bc98-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="9bc98-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="9bc98-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="9bc98-123">[in] Flags für das bevorzugte Zeichenformat.</span><span class="sxs-lookup"><span data-stu-id="9bc98-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="9bc98-124">Muss mindestens einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="9bc98-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="9bc98-125">DDLWRAP_FLAG_ANSI– Das umschlossene Objekt wird als ANSI verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="9bc98-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="9bc98-126">DDLWRAP_FLAG_UNICODE– Das umschlossene Objekt wird als UNICODE verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="9bc98-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="9bc98-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="9bc98-127">_pIID_</span></span>
  
>  <span data-ttu-id="9bc98-128">[in] Der Bezeichner der Schnittstelle, die vom entpackten Objekt unterstützt wird. Legen Sie ihn auf NULL fest, wenn dies nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9bc98-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="9bc98-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="9bc98-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="9bc98-130">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bc98-130">[in] This parameter is not used.</span></span> <span data-ttu-id="9bc98-131">Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9bc98-131">It must be NULL.</span></span> 
    
<span data-ttu-id="9bc98-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="9bc98-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="9bc98-133">[in] Legen Sie diesen Parameter auf **true,**  _wenn pvUnwrapped_ vor dem Umbruch auf sein Format überprüft werden soll. legen Sie den Wert **auf false,** wenn das Objekt ohne Überprüfung umschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bc98-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="9bc98-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="9bc98-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="9bc98-135">[out] Ein Zeiger auf das angeforderte Objekt, umschlossen in das angeforderte Zeichenformat.</span><span class="sxs-lookup"><span data-stu-id="9bc98-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9bc98-136">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9bc98-136">Return values</span></span>

<span data-ttu-id="9bc98-137">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9bc98-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9bc98-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9bc98-138">Remarks</span></span>

<span data-ttu-id="9bc98-139">Das Übergeben eines umschlossenen Objekts, bei dem  _fCheckWrap_ auf **true** festgelegt ist, führt zu einem entpackten Objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc98-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="9bc98-140">Unabhängig davon, ob das zurückgegebene Objekt umschlossen ist, ist der Client für die Freigabe des Verweises auf das zurückgegebene Objekt verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="9bc98-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="9bc98-141">Wenn Sie **GetProcAddress** verwenden, um nach der Adresse dieser Funktion in msmapi32.dll zu suchen, geben Sie HrCreateNewWrappedObject@28 **Prozedurnamen** an.</span><span class="sxs-lookup"><span data-stu-id="9bc98-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bc98-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bc98-142">See also</span></span>

- [<span data-ttu-id="9bc98-143">Über der Datenschicht Abbau API</span><span class="sxs-lookup"><span data-stu-id="9bc98-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="9bc98-144">Konstanten (Datendegradierungsschicht-API)</span><span class="sxs-lookup"><span data-stu-id="9bc98-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

