---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Dialogfeld Kontoeinstellungen oder neues Konto hinzufügen angezeigt.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791098"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="f06c2-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="f06c2-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="f06c2-104">Dialogfeld für die **Kontoeinstellungen** oder **Hinzufügen eines neuen Kontos** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f06c2-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f06c2-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f06c2-105">Quick info</span></span>

<span data-ttu-id="f06c2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f06c2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a><span data-ttu-id="f06c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f06c2-107">Parameters</span></span>

<span data-ttu-id="f06c2-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="f06c2-108">_hwnd_</span></span>
  
> <span data-ttu-id="f06c2-109">[in] Das Handle für das Fenster, das angezeigte Dialogfeld gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f06c2-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="f06c2-110">Möglicherweise 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f06c2-110">May be zero.</span></span>
    
<span data-ttu-id="f06c2-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f06c2-111">_dwFlags_</span></span>
  
> <span data-ttu-id="f06c2-112">[in] Kennzeichen, die um das Verhalten der Anzeige zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f06c2-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="f06c2-113">**ACCTUI_NO_WARNING**– die Warnung, dass die Änderungen erst in Kraft, werden Outlook gestartet wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f06c2-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="f06c2-114">Gilt nur, wenn die Anwendung ausgeführt wird in-Process mit Outlook.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="f06c2-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="f06c2-115">**ACCTUI_SHOW_DATA_TAB**– zeigt das Dialogfeld **Kontoeinstellungen** mit der Registerkarte **Daten** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f06c2-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="f06c2-116">Nur gültig, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f06c2-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="f06c2-117">**ACCTUI_SHOW_ACCTWIZARD**– zeigt das Dialogfeld **Neues Konto hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="f06c2-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="f06c2-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="f06c2-118">_wszTitle_</span></span>
  
> <span data-ttu-id="f06c2-119">[in] Dieser Parameter wird nicht verwendet und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="f06c2-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="f06c2-120">_cCategories_</span></span>
  
> <span data-ttu-id="f06c2-121">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="f06c2-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="f06c2-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="f06c2-123">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="f06c2-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="f06c2-124">_pclsidType_</span></span>
  
> <span data-ttu-id="f06c2-125">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f06c2-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f06c2-126">Return values</span></span>

|<span data-ttu-id="f06c2-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="f06c2-127">**HRESULT**</span></span>|<span data-ttu-id="f06c2-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f06c2-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f06c2-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="f06c2-129">S_OK</span></span>  <br/> |<span data-ttu-id="f06c2-130">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f06c2-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="f06c2-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="f06c2-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="f06c2-132">Das Dialogfeld konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f06c2-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="f06c2-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f06c2-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f06c2-134">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f06c2-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="f06c2-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f06c2-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="f06c2-136">Das Dialogfeld **Neues Konto hinzufügen** zurückgegeben einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f06c2-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="f06c2-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f06c2-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="f06c2-138">Der Parameter _cCategories_, _RgclsidCategories_oder _PclsidType_ ist ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="f06c2-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="f06c2-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f06c2-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="f06c2-140">Das Dialogfeld **Kontoeinstellungen** hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f06c2-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f06c2-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f06c2-141">Remarks</span></span>

<span data-ttu-id="f06c2-142">Der Parameter _cCategories_, _RgclsidCategories_und _PclsidType_ zu diesem Zeitpunkt nicht verwendet werden und müssen NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="f06c2-143">_WszTitle_ wird nicht verwendet und sollte auch NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f06c2-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

