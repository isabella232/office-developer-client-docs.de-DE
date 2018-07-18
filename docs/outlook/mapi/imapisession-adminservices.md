---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792325"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="3c979-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="3c979-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="3c979-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c979-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c979-105">Gibt einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) für die Änderung Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="3c979-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="3c979-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c979-106">Parameters</span></span>

 <span data-ttu-id="3c979-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3c979-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3c979-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="3c979-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3c979-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="3c979-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="3c979-110">[out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Service-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="3c979-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c979-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3c979-111">Return value</span></span>

<span data-ttu-id="3c979-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c979-112">S_OK</span></span> 
  
> <span data-ttu-id="3c979-113">Ein Zeiger auf ein Objekt "Message" Service Administration wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c979-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="3c979-114">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3c979-114">Notes to callers</span></span>

<span data-ttu-id="3c979-115">Die **IMAPISession::AdminServices** -Methode erstellt ein Service Administration Meldungsobjekt, ein Objekt, das die **IMsgServiceAdmin** -Schnittstelle unterstützt und gibt einen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="3c979-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="3c979-116">Rufen Sie mithilfe dieser Zeiger **IMsgServiceAdmin** -Methoden, um die Nachrichtendienste im Profil der Sitzung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3c979-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="3c979-117">Beachten Sie, dass diese Änderungen nicht übernommen, bis der nächste Sitzung werden; die aktuelle Sitzung ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="3c979-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3c979-118">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3c979-118">MFCMAPI reference</span></span>

<span data-ttu-id="3c979-119">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3c979-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3c979-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3c979-120">**File**</span></span>|<span data-ttu-id="3c979-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3c979-121">**Function**</span></span>|<span data-ttu-id="3c979-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3c979-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c979-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3c979-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3c979-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="3c979-124">GetServerName</span></span>  <br/> |<span data-ttu-id="3c979-125">MFCMAPI (engl.) wird die **IMAPISession::AdminServices** -Methode verwendet, Zugriff auf das Profil, um den Namen des Servers zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3c979-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c979-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c979-126">See also</span></span>



[<span data-ttu-id="3c979-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c979-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="3c979-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="3c979-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="3c979-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c979-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="3c979-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3c979-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

