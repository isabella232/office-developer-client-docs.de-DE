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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322064"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="7e25f-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="7e25f-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="7e25f-104">Zeigt das Dialogfeld **Kontoeinstellungen** oder **Neues Konto hinzufügen** an.</span><span class="sxs-lookup"><span data-stu-id="7e25f-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7e25f-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7e25f-105">Quick info</span></span>

<span data-ttu-id="7e25f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7e25f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7e25f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e25f-107">Parameters</span></span>

<span data-ttu-id="7e25f-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="7e25f-108">_hwnd_</span></span>
  
> <span data-ttu-id="7e25f-109">in Das Handle für das Fenster, in dem das angezeigte Dialogfeld modal ist.</span><span class="sxs-lookup"><span data-stu-id="7e25f-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="7e25f-110">MöglicherWeise NULL.</span><span class="sxs-lookup"><span data-stu-id="7e25f-110">May be zero.</span></span>
    
<span data-ttu-id="7e25f-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7e25f-111">_dwFlags_</span></span>
  
> <span data-ttu-id="7e25f-112">in Flags zum Ändern des Anzeigeverhaltens.</span><span class="sxs-lookup"><span data-stu-id="7e25f-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="7e25f-113">**ACCTUI_NO_WARNING**– zeigen Sie nicht die Warnung an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7e25f-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="7e25f-114">Gilt nur, wenn die Anwendung in-Process mit Outlook. exe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e25f-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="7e25f-115">**ACCTUI_SHOW_DATA_TAB**– zeigt das Dialogfeld **Kontoeinstellungen** an, wobei die Registerkarte **Daten** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="7e25f-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="7e25f-116">Gilt nur, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7e25f-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="7e25f-117">**ACCTUI_SHOW_ACCTWIZARD**– zeigt das Dialogfeld **Neues Konto hinzufügen** an.</span><span class="sxs-lookup"><span data-stu-id="7e25f-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="7e25f-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="7e25f-118">_wszTitle_</span></span>
  
> <span data-ttu-id="7e25f-119">in Dieser Parameter wird nicht verwendet und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="7e25f-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="7e25f-120">_cCategories_</span></span>
  
> <span data-ttu-id="7e25f-121">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="7e25f-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="7e25f-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="7e25f-123">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="7e25f-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="7e25f-124">_pclsidType_</span></span>
  
> <span data-ttu-id="7e25f-125">in Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7e25f-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7e25f-126">Return values</span></span>

|<span data-ttu-id="7e25f-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7e25f-127">**HRESULT**</span></span>|<span data-ttu-id="7e25f-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e25f-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e25f-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e25f-129">S_OK</span></span>  <br/> |<span data-ttu-id="7e25f-130">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e25f-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="7e25f-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="7e25f-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="7e25f-132">Das Dialogfeld konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e25f-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="7e25f-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7e25f-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7e25f-134">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7e25f-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="7e25f-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7e25f-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="7e25f-136">Das Dialogfeld **Neues Konto hinzufügen** hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e25f-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="7e25f-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e25f-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="7e25f-138">Der _cCategories_-, _RgclsidCategories_-oder _pclsidType_ -Parameter ist ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="7e25f-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="7e25f-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7e25f-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="7e25f-140">Das Dialogfeld **Kontoeinstellungen** hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e25f-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e25f-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e25f-141">Remarks</span></span>

<span data-ttu-id="7e25f-142">Die _cCategories_-, _RgclsidCategories_-und _pclsidType_ -Parameter werden zu diesem Zeitpunkt nicht verwendet und müssen NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="7e25f-143">_wszTitle_ wird nicht verwendet und sollte auch NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e25f-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

