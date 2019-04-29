---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Zeigt das Dialogfeld Kontoeinstellungen oder neues Konto hinzufügen an.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415033"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="d18c6-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="d18c6-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="d18c6-104">Zeigt das Dialogfeld **Kontoeinstellungen** oder **Neues Konto hinzufügen** an.</span><span class="sxs-lookup"><span data-stu-id="d18c6-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d18c6-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d18c6-105">Quick info</span></span>

<span data-ttu-id="d18c6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="d18c6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d18c6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d18c6-107">Parameters</span></span>

<span data-ttu-id="d18c6-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="d18c6-108">_hwnd_</span></span>
  
> <span data-ttu-id="d18c6-109">in Das Handle für das Fenster, in dem das angezeigte Dialogfeld modal ist.</span><span class="sxs-lookup"><span data-stu-id="d18c6-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="d18c6-110">MöglicherWeise NULL.</span><span class="sxs-lookup"><span data-stu-id="d18c6-110">May be zero.</span></span>
    
<span data-ttu-id="d18c6-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d18c6-111">_dwFlags_</span></span>
  
> <span data-ttu-id="d18c6-112">in Flags zum Ändern des Anzeigeverhaltens.</span><span class="sxs-lookup"><span data-stu-id="d18c6-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="d18c6-113">**ACCTUI_NO_WARNING**– zeigen Sie nicht die Warnung an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d18c6-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="d18c6-114">Gilt nur, wenn die Anwendung in-Process mit Outlook. exe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d18c6-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="d18c6-115">**ACCTUI_SHOW_DATA_TAB**– zeigt das Dialogfeld **Kontoeinstellungen** an, wobei die Registerkarte **Daten** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d18c6-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="d18c6-116">Gilt nur, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d18c6-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="d18c6-117">**ACCTUI_SHOW_ACCTWIZARD**– zeigt das Dialogfeld **Neues Konto hinzufügen** an.</span><span class="sxs-lookup"><span data-stu-id="d18c6-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="d18c6-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="d18c6-118">_wszTitle_</span></span>
  
> <span data-ttu-id="d18c6-119">in Dieser Parameter wird nicht verwendet und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="d18c6-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="d18c6-120">_cCategories_</span></span>
  
> <span data-ttu-id="d18c6-121">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="d18c6-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="d18c6-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="d18c6-123">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="d18c6-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="d18c6-124">_pclsidType_</span></span>
  
> <span data-ttu-id="d18c6-125">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d18c6-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d18c6-126">Return values</span></span>

|<span data-ttu-id="d18c6-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d18c6-127">**HRESULT**</span></span>|<span data-ttu-id="d18c6-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="d18c6-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d18c6-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="d18c6-129">S_OK</span></span>  <br/> |<span data-ttu-id="d18c6-130">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d18c6-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="d18c6-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="d18c6-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="d18c6-132">Das Dialogfeld konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d18c6-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="d18c6-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d18c6-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="d18c6-134">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d18c6-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="d18c6-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d18c6-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="d18c6-136">Das Dialogfeld **Neues Konto hinzufügen** hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d18c6-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="d18c6-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d18c6-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="d18c6-138">Der _cCategories_-, _RgclsidCategories_-oder _pclsidType_ -Parameter ist ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="d18c6-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="d18c6-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d18c6-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="d18c6-140">Das Dialogfeld **Kontoeinstellungen** hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d18c6-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d18c6-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d18c6-141">Remarks</span></span>

<span data-ttu-id="d18c6-142">Die _cCategories_-, _RgclsidCategories_-und _pclsidType_ -Parameter werden zu diesem Zeitpunkt nicht verwendet und müssen NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="d18c6-143">_wszTitle_ wird nicht verwendet und sollte auch NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d18c6-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

