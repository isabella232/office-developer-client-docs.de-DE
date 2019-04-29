---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427738"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="a8738-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="a8738-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="a8738-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8738-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8738-105">Gibt einen Schnittstellenzeiger auf die lokale Formularbibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="a8738-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8738-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a8738-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8738-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="a8738-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a8738-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a8738-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8738-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8738-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8738-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a8738-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8738-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a8738-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="a8738-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8738-112">Parameters</span></span>

 <span data-ttu-id="a8738-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="a8738-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="a8738-114">Out Zeiger auf einen Zeiger auf die Schnittstelle der lokalen Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="a8738-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8738-115">Return value</span><span class="sxs-lookup"><span data-stu-id="a8738-115">Return value</span></span>

<span data-ttu-id="a8738-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8738-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8738-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8738-117">Remarks</span></span>

<span data-ttu-id="a8738-118">Die Schnittstelle, an die ein Zeiger zurückgegeben wird, kann von Drittanbieter-Installationsprogrammen verwendet werden, um anwendungsspezifische Formulare in der Bibliothek zu installieren, ohne dass sich das Programm zuerst bei MAPI anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="a8738-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8738-119">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a8738-119">MFCMAPI reference</span></span>

<span data-ttu-id="a8738-120">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8738-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8738-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a8738-121">**File**</span></span>|<span data-ttu-id="a8738-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a8738-122">**Function**</span></span>|<span data-ttu-id="a8738-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a8738-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8738-124">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a8738-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a8738-125">CMainDlg:: OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="a8738-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="a8738-126">MFCMAPI verwendet die **MAPIOpenLocalFormContainer** -Methode, um den lokalen Formular Container zu öffnen, der in einem neuen Fenster gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8738-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8738-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8738-127">See also</span></span>



[<span data-ttu-id="a8738-128">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a8738-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

