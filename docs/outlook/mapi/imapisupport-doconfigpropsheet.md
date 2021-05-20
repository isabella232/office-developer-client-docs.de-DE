---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429015"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="d6711-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="d6711-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="d6711-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6711-105">Zeigt ein Konfigurationseigenschaftsblatt an.</span><span class="sxs-lookup"><span data-stu-id="d6711-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="d6711-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6711-106">Parameters</span></span>

 <span data-ttu-id="d6711-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d6711-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d6711-108">[in] Ein Handle zum übergeordneten Fenster des Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="d6711-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="d6711-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6711-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d6711-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d6711-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6711-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="d6711-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="d6711-112">[in] Ein Zeiger auf den Titel des Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="d6711-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="d6711-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="d6711-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="d6711-114">[in] Ein Zeiger auf die Anzeigetabelle, in der die Steuerelemente beschrieben werden, die auf dem Eigenschaftenblatt angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6711-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="d6711-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="d6711-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="d6711-116">[in] Ein Zeiger auf die [IMAPIProp-Implementierung,](imapipropiunknown.md) die für den Zugriff auf die Konfigurationseigenschaften verwendet werden soll, die auf dem Eigenschaftenblatt angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6711-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="d6711-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="d6711-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="d6711-118">[in] Ein nullbasierter Index zur Standardmäßigen oberen Seite des Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="d6711-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6711-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6711-119">Return value</span></span>

<span data-ttu-id="d6711-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6711-120">S_OK</span></span> 
  
> <span data-ttu-id="d6711-121">Das Konfigurationseigenschaftsblatt wurde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6711-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6711-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6711-122">Remarks</span></span>

<span data-ttu-id="d6711-123">Die **IMAPISupport::D oConfigPropsheet-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="d6711-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="d6711-124">**DoConfigPropSheet** bietet eine Standardbenutzerschnittstelle zum Anzeigen der Eigenschaften von Dienstanbietern und Nachrichtendiensten.</span><span class="sxs-lookup"><span data-stu-id="d6711-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="d6711-125">Verwenden Sie dieses Standarddialogfeld für alle Konfigurationseigenschaftsanzeigen, damit Benutzer von einer konsistenten Windows profitieren.</span><span class="sxs-lookup"><span data-stu-id="d6711-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="d6711-126">Dienstanbieter rufen **DoConfigPropSheet** im Rahmen der Implementierung der [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) oder über eine Schaltfläche auf, die zum Anzeigen von Details zu Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6711-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="d6711-127">Nachrichtendienste rufen **DoConfigPropSheet über** die Einstiegspunktfunktion des Nachrichtendiensts auf.</span><span class="sxs-lookup"><span data-stu-id="d6711-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6711-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d6711-128">Notes to callers</span></span>

<span data-ttu-id="d6711-129">Sie können die Anzeigetabelle erstellen, auf die der  _lpDisplayTable-Parameter_ verweist, indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) oder benutzerdefinierten Code aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d6711-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6711-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6711-130">See also</span></span>



[<span data-ttu-id="d6711-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d6711-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="d6711-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="d6711-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="d6711-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d6711-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d6711-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6711-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d6711-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="d6711-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="d6711-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6711-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="d6711-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d6711-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="d6711-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="d6711-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="d6711-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6711-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

