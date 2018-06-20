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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06341f897a7865c09a565db67bb409fc9f49f8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792367"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="5ddf3-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="5ddf3-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="5ddf3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ddf3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ddf3-105">Zeigt eine Konfiguration Eigenschaftenblatt.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5ddf3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ddf3-106">Parameters</span></span>

 <span data-ttu-id="5ddf3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5ddf3-108">[in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="5ddf3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5ddf3-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5ddf3-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="5ddf3-112">[in] Ein Zeiger auf den Titel des Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="5ddf3-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="5ddf3-114">[in] Ein Zeiger auf den zeigt die Tabelle, die angezeigt werden, um die Steuerelemente auf der Eigenschaftenseite beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="5ddf3-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="5ddf3-116">[in] Ein Zeiger auf die Implementierung [IMAPIProp](imapipropiunknown.md) , für den Zugriff auf die Konfigurationseigenschaften verwendet werden, auf der Eigenschaftenseite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="5ddf3-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="5ddf3-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="5ddf3-118">[in] Ein nullbasierter Index der oberen Standardseite des Eigenschaftenblatts.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ddf3-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5ddf3-119">Return value</span></span>

<span data-ttu-id="5ddf3-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ddf3-120">S_OK</span></span> 
  
> <span data-ttu-id="5ddf3-121">Das Eigenschaftenblatt Konfiguration wurde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ddf3-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ddf3-122">Remarks</span></span>

<span data-ttu-id="5ddf3-123">Die **IMAPISupport::DoConfigPropsheet** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="5ddf3-124">**DoConfigPropSheet** stellt eine Standardbenutzeroberfläche zum Anzeigen der Eigenschaften der Dienstanbieter und Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="5ddf3-125">Sie sollten dieses Dialogfeld standard für alle Konfiguration-Eigenschaft zeigt verwenden, damit Benutzer eine konsistente Schnittstelle Windows nutzen.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="5ddf3-126">Dienstanbieter anrufen **DoConfigPropSheet** als Teil ihrer Implementierung [der SettingsDialog](imapistatus-settingsdialog.md) oder eine Schaltfläche zum Anzeigen von Details auf Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="5ddf3-127">Nachricht Services Aufrufen **DoConfigPropSheet** aus ihrer Nachricht Service Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ddf3-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5ddf3-128">Notes to callers</span></span>

<span data-ttu-id="5ddf3-129">Sie können die Anzeige-Tabelle der _LpDisplayTable_ -Parameter auf das durch Aufrufen der [BuildDisplayTable](builddisplaytable.md) -Funktion oder mit benutzerdefiniertem Code erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ddf3-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ddf3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ddf3-130">See also</span></span>



[<span data-ttu-id="5ddf3-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="5ddf3-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="5ddf3-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="5ddf3-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="5ddf3-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5ddf3-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="5ddf3-134">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ddf3-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="5ddf3-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="5ddf3-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="5ddf3-136">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ddf3-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="5ddf3-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5ddf3-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="5ddf3-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="5ddf3-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="5ddf3-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ddf3-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

