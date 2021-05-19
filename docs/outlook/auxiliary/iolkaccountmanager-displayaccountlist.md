---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Zeigt entweder das Dialogfeld Konto Einstellungen oder Das Dialogfeld Neues Konto hinzufügen an.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415033"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="7ea9a-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="7ea9a-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="7ea9a-104">Zeigt entweder **das** Einstellungen **oder das Dialogfeld Neues Konto** hinzufügen an.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7ea9a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7ea9a-105">Quick info</span></span>

<span data-ttu-id="7ea9a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7ea9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ea9a-107">Parameters</span></span>

<span data-ttu-id="7ea9a-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-108">_hwnd_</span></span>
  
> <span data-ttu-id="7ea9a-109">[in] Das Handle zu dem Fenster, zu dem das angezeigte Dialogfeld modal ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="7ea9a-110">Kann null sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-110">May be zero.</span></span>
    
<span data-ttu-id="7ea9a-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-111">_dwFlags_</span></span>
  
> <span data-ttu-id="7ea9a-112">[in] Flags zum Ändern des Anzeigeverhaltens.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="7ea9a-113">**ACCTUI_NO_WARNING**– Zeigen Sie die Warnung nicht an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="7ea9a-114">Gilt nur, wenn die Anwendung mit einem Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="7ea9a-115">**ACCTUI_SHOW_DATA_TAB**– Zeigt das Dialogfeld **Konto Einstellungen,** wenn die Registerkarte **Daten** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="7ea9a-116">Nur gültig, **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="7ea9a-117">**ACCTUI_SHOW_ACCTWIZARD**– Zeigt das **Dialogfeld Neues Konto** hinzufügen an.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="7ea9a-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-118">_wszTitle_</span></span>
  
> <span data-ttu-id="7ea9a-119">[in] Dieser Parameter wird nicht verwendet und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="7ea9a-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-120">_cCategories_</span></span>
  
> <span data-ttu-id="7ea9a-121">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="7ea9a-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="7ea9a-123">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="7ea9a-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="7ea9a-124">_pclsidType_</span></span>
  
> <span data-ttu-id="7ea9a-125">[in] Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7ea9a-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7ea9a-126">Return values</span></span>

|<span data-ttu-id="7ea9a-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7ea9a-127">**HRESULT**</span></span>|<span data-ttu-id="7ea9a-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ea9a-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ea9a-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ea9a-129">S_OK</span></span>  <br/> |<span data-ttu-id="7ea9a-130">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="7ea9a-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="7ea9a-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="7ea9a-132">Das Dialogfeld konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="7ea9a-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7ea9a-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7ea9a-134">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="7ea9a-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7ea9a-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="7ea9a-136">Im **Dialogfeld Neues Konto** hinzufügen wurde ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="7ea9a-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ea9a-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="7ea9a-138">Der  _Parameter cCategories_,  _rgclsidCategories_ oder  _pclsidType_ ist nicht NULL.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="7ea9a-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7ea9a-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="7ea9a-140">Im **Einstellungen** Dialogfeld Konto wurde ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ea9a-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ea9a-141">Remarks</span></span>

<span data-ttu-id="7ea9a-142">Die  _Parameter cCategories,_  _rgclsidCategories_ und  _pclsidType_ werden derzeit nicht verwendet und müssen NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="7ea9a-143">_wszTitle_ wird nicht verwendet und sollte auch NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

