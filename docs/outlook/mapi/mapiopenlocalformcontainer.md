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
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582560"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="84850-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="84850-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="84850-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84850-105">Gibt einen Schnittstellenzeiger auf den lokalen Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="84850-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84850-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="84850-106">Header file:</span></span>  <br/> |<span data-ttu-id="84850-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="84850-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="84850-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="84850-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="84850-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="84850-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="84850-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="84850-110">Called by:</span></span>  <br/> |<span data-ttu-id="84850-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="84850-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="84850-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="84850-112">Parameters</span></span>

 <span data-ttu-id="84850-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="84850-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="84850-114">[out] Zeiger auf einen Zeiger auf die lokale Formular Library-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="84850-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84850-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84850-115">Return value</span></span>

<span data-ttu-id="84850-116">None.</span><span class="sxs-lookup"><span data-stu-id="84850-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84850-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="84850-117">Remarks</span></span>

<span data-ttu-id="84850-118">Die Schnittstelle, an die ein Zeiger zurückgegeben wird, kann anwendungsspezifische-Formularen in die Bibliothek installieren, ohne das Programm zuvor zur Anmeldung bei MAPI von Programmen von Drittanbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84850-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="84850-119">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="84850-119">MFCMAPI reference</span></span>

<span data-ttu-id="84850-120">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84850-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84850-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="84850-121">**File**</span></span>|<span data-ttu-id="84850-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="84850-122">**Function**</span></span>|<span data-ttu-id="84850-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="84850-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84850-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="84850-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="84850-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="84850-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="84850-126">MFCMAPI (engl.) verwendet die **MAPIOpenLocalFormContainer** -Methode, um den lokalen Formular Container zum Rendern in einem neuen Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="84850-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84850-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84850-127">See also</span></span>



[<span data-ttu-id="84850-128">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="84850-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

