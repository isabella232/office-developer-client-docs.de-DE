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
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793128"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="8e91c-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="8e91c-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="8e91c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e91c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e91c-105">Öffnet eine [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle in einem Formular Bibliothek Anbieter-Objekt im Zusammenhang mit einer vorhandenen Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="8e91c-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e91c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8e91c-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e91c-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="8e91c-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8e91c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8e91c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e91c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8e91c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8e91c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8e91c-110">Called by:</span></span>  <br/> |<span data-ttu-id="8e91c-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="8e91c-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="8e91c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e91c-112">Parameters</span></span>

 <span data-ttu-id="8e91c-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="8e91c-113">_pSession_</span></span>
  
> <span data-ttu-id="8e91c-114">[in] Zeiger auf die Sitzung von der Clientanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e91c-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="8e91c-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="8e91c-115">_ppmgr_</span></span>
  
> <span data-ttu-id="8e91c-116">[out] Zeiger auf die zurückgegebene Schnittstelle **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="8e91c-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e91c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e91c-117">Return value</span></span>

<span data-ttu-id="8e91c-118">None.</span><span class="sxs-lookup"><span data-stu-id="8e91c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e91c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e91c-119">Remarks</span></span>

<span data-ttu-id="8e91c-120">Nach eine Clientanwendung an die **MAPIOpenFormMgr** -Funktion aufruft, erfolgen die meisten nachfolgende Forms-bezogene Interaktionen über den Formular-Bibliothek-Anbieter oder eine Schnittstelle, die vom Formular Bibliotheksanbieter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e91c-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="8e91c-121">Die **IMAPIFormMgr** -Schnittstelle ermöglicht dem Client zum Arbeiten mit Message Handler und Ausführen von Lösungen zwischen Nachrichtenklassen und Formularbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="8e91c-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e91c-122">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="8e91c-122">MFCMAPI reference</span></span>

<span data-ttu-id="8e91c-123">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8e91c-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e91c-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8e91c-124">**File**</span></span>|<span data-ttu-id="8e91c-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8e91c-125">**Function**</span></span>|<span data-ttu-id="8e91c-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8e91c-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e91c-127">MainDlg.cpp öffnet den Formular-Manager aus, damit ein Formular ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e91c-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="8e91c-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="8e91c-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="8e91c-129">MFCMAPI (engl.) verwendet die **MAPIOpenFormMgr** -Methode, um den Formular-Manager zu öffnen, damit ein Formular ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e91c-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e91c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e91c-130">See also</span></span>



[<span data-ttu-id="8e91c-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8e91c-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

