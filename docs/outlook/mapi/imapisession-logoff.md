---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338108"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="98a3a-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="98a3a-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="98a3a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98a3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98a3a-105">Beendet eine MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="98a3a-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="98a3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98a3a-106">Parameters</span></span>

 <span data-ttu-id="98a3a-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="98a3a-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="98a3a-108">in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98a3a-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="98a3a-109">Dieser Parameter wird ignoriert, wenn das MAPI_LOGOFF_UI-Flag nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="98a3a-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="98a3a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98a3a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="98a3a-111">in Eine Bitmaske mit Flags, die den Abmeldevorgang steuern.</span><span class="sxs-lookup"><span data-stu-id="98a3a-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="98a3a-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="98a3a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="98a3a-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="98a3a-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="98a3a-114">Wenn diese Sitzung freigegeben ist, sollten alle Clients, die sich mit der freigegebenen Sitzung angemeldet haben, über die Abmeldung in Bearbeitung benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="98a3a-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="98a3a-115">Die Clients sollten sich abmelden.</span><span class="sxs-lookup"><span data-stu-id="98a3a-115">The clients should log off.</span></span> <span data-ttu-id="98a3a-116">Jeder Client, der die freigegebene Sitzung verwendet, kann dieses Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="98a3a-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="98a3a-117">MAPI_LOGOFF_SHARED wird ignoriert, wenn die aktuelle Sitzung nicht freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="98a3a-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="98a3a-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="98a3a-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="98a3a-119">\*\*\*\* Bei der Abmeldung kann während des Vorgangs ein Dialogfeld angezeigt werden, sodass der Benutzer möglicherweise zur Bestätigung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="98a3a-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="98a3a-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="98a3a-120">_ulReserved_</span></span>
  
> <span data-ttu-id="98a3a-121">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="98a3a-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98a3a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98a3a-122">Return value</span></span>

<span data-ttu-id="98a3a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="98a3a-123">S_OK</span></span> 
  
> <span data-ttu-id="98a3a-124">Der Abmeldevorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98a3a-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98a3a-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98a3a-125">Remarks</span></span>

<span data-ttu-id="98a3a-126">Die **IMAPISession:: Logoff** -Methode beendet eine MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="98a3a-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="98a3a-127">Wenn **Logoff** zurückgegeben wird, kann keine der Methoden außer [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="98a3a-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98a3a-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="98a3a-128">Notes to callers</span></span>

<span data-ttu-id="98a3a-129">Wenn \*\*\*\* die Abmeldung zurückgegeben wird, geben Sie das Sitzungsobjekt durch Aufrufen seiner **IUnknown:: Release** -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="98a3a-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="98a3a-130">Weitere Informationen zum Beenden einer Sitzung finden Sie unter [Beenden einer MAPI-Sitzung](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="98a3a-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="98a3a-131">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="98a3a-131">MFCMAPI reference</span></span>

<span data-ttu-id="98a3a-132">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="98a3a-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="98a3a-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="98a3a-133">**File**</span></span>|<span data-ttu-id="98a3a-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="98a3a-134">**Function**</span></span>|<span data-ttu-id="98a3a-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="98a3a-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="98a3a-136">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="98a3a-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="98a3a-137">CMapiObjects:: abmelden</span><span class="sxs-lookup"><span data-stu-id="98a3a-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="98a3a-138">MfcMapi verwendet die **IMAPISession:: Logout** -Methode, um sich von der Sitzung abzumelden, bevor Sie Sie freigibt.</span><span class="sxs-lookup"><span data-stu-id="98a3a-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="98a3a-139">Aufgrund des fast-shutdown-Verhaltens, das in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 und Microsoft Outlook 2013 eingeführt wurde, sollten Clients den **MAPI_LOGOFF_SHARED** -Parameter nie an [IMAPISession:: Logoff](imapisession-logoff.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="98a3a-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="98a3a-140">Durch das Übergeben von **MAPI_LOGOFF_SHARED** werden alle MAPI-Clients zum Herunterfahren gestartet, und es wird ein unerwartetes Verhalten auftreten.</span><span class="sxs-lookup"><span data-stu-id="98a3a-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98a3a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98a3a-141">See also</span></span>



[<span data-ttu-id="98a3a-142">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98a3a-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="98a3a-143">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="98a3a-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="98a3a-144">Beenden einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="98a3a-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

