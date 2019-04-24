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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322414"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="3b014-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="3b014-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="3b014-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b014-105">Gibt einen [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Zeiger zurück, um Änderungen an den Nachrichtendiensten vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3b014-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="3b014-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b014-106">Parameters</span></span>

 <span data-ttu-id="3b014-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b014-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3b014-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="3b014-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3b014-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="3b014-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="3b014-110">Out Ein Zeiger auf einen Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3b014-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b014-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b014-111">Return value</span></span>

<span data-ttu-id="3b014-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b014-112">S_OK</span></span> 
  
> <span data-ttu-id="3b014-113">Ein Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b014-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="3b014-114">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3b014-114">Notes to callers</span></span>

<span data-ttu-id="3b014-115">Die **IMAPISession:: AdminServices** -Methode erstellt ein Nachrichtendienst-Verwaltungsobjekt, ein Objekt, das die **IMsgServiceAdmin** -Schnittstelle unterstützt und einen Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3b014-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="3b014-116">Mithilfe dieses Zeigers können Sie **IMsgServiceAdmin** -Methoden aufrufen, um einen beliebigen Nachrichtendienst im Sitzungsprofil zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3b014-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="3b014-117">Beachten Sie, dass diese Änderungen erst in der nächsten Sitzung wirksam werden. die aktuelle Sitzung ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="3b014-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b014-118">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="3b014-118">MFCMAPI reference</span></span>

<span data-ttu-id="3b014-119">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3b014-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b014-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3b014-120">**File**</span></span>|<span data-ttu-id="3b014-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3b014-121">**Function**</span></span>|<span data-ttu-id="3b014-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3b014-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b014-123">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="3b014-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3b014-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="3b014-124">GetServerName</span></span>  <br/> |<span data-ttu-id="3b014-125">MFCMAPI verwendet die **IMAPISession:: AdminServices** -Methode, um auf das Profil zuzugreifen, um den Servernamen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3b014-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b014-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b014-126">See also</span></span>



[<span data-ttu-id="3b014-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b014-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="3b014-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="3b014-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="3b014-129">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b014-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="3b014-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3b014-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

