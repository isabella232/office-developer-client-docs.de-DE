---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418050"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="bff78-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="bff78-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="bff78-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bff78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bff78-105">Öffnet eine [IMAPIFormMgr-Schnittstelle](imapiformmgriunknown.md) für ein Formularbibliotheksanbieterobjekt im Kontext einer vorhandenen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bff78-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bff78-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bff78-106">Header file:</span></span>  <br/> |<span data-ttu-id="bff78-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bff78-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bff78-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bff78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bff78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bff78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bff78-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bff78-110">Called by:</span></span>  <br/> |<span data-ttu-id="bff78-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="bff78-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="bff78-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bff78-112">Parameters</span></span>

 <span data-ttu-id="bff78-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="bff78-113">_pSession_</span></span>
  
> <span data-ttu-id="bff78-114">[in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bff78-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="bff78-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="bff78-115">_ppmgr_</span></span>
  
> <span data-ttu-id="bff78-116">[out] Zeiger auf die zurückgegebene **IMAPIFormMgr-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="bff78-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bff78-117">Return value</span><span class="sxs-lookup"><span data-stu-id="bff78-117">Return value</span></span>

<span data-ttu-id="bff78-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="bff78-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bff78-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bff78-119">Remarks</span></span>

<span data-ttu-id="bff78-120">Nachdem eine Clientanwendung einen Aufruf der **MAPIOpenFormMgr-Funktion** ausgeführt hat, finden die meisten nachfolgenden formularbezogenen Interaktionen über den Formularbibliotheksanbieter oder eine vom Formularbibliotheksanbieter zurückgegebene Schnittstelle statt.</span><span class="sxs-lookup"><span data-stu-id="bff78-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="bff78-121">Die **IMAPIFormMgr-Schnittstelle** ermöglicht es dem Client, mit Nachrichtenhandlern zu arbeiten und Auflösungen zwischen Nachrichtenklassen und Formularbibliotheken durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="bff78-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bff78-122">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="bff78-122">MFCMAPI reference</span></span>

<span data-ttu-id="bff78-123">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bff78-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bff78-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="bff78-124">**File**</span></span>|<span data-ttu-id="bff78-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bff78-125">**Function**</span></span>|<span data-ttu-id="bff78-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="bff78-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bff78-127">MainDlg.cpp öffnet den Formular-Manager, damit ein Formular ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bff78-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="bff78-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="bff78-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="bff78-129">MFCMAPI verwendet die **MAPIOpenFormMgr-Methode,** um den Formular-Manager zu öffnen, damit ein Formular ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bff78-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bff78-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff78-130">See also</span></span>



[<span data-ttu-id="bff78-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="bff78-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

