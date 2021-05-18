---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329421"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="f4dc3-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="f4dc3-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="f4dc3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4dc3-105">Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger für](iaddrbookimapiprop.md) weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="f4dc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4dc3-106">Parameters</span></span>

 <span data-ttu-id="f4dc3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f4dc3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f4dc3-108">[in] Ein Handle zum übergeordneten Fenster des Dialogfelds allgemeine Adresse und andere zugehörige Displays.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="f4dc3-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f4dc3-109">_lpInterface_</span></span>
  
> <span data-ttu-id="f4dc3-110">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="f4dc3-111">Wenn **Null** übergeben wird, wird ein Zeiger auf die Standardschnittstelle des Adressbuchs, [IAddrBook : IMAPIProp , zurückgegeben.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f4dc3-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="f4dc3-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4dc3-112">_ulFlags_</span></span>
  
> <span data-ttu-id="f4dc3-113">[in] Eine Bitmaske mit Flags, die das Öffnen des Adressbuchs steuert.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="f4dc3-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f4dc3-114">The following flag can be set:</span></span>
    
<span data-ttu-id="f4dc3-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f4dc3-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="f4dc3-116">Unterdrückt die Anzeige von Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="f4dc3-117">Wenn das AB_NO_DIALOG nicht festgelegt ist, können die Adressbuchanbieter, die zum integrierten Adressbuch beitragen, den Benutzer zur Eingabe der erforderlichen Informationen aufforderen.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="f4dc3-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="f4dc3-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="f4dc3-119">[out] Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4dc3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4dc3-120">Return value</span></span>

<span data-ttu-id="f4dc3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4dc3-121">S_OK</span></span> 
  
> <span data-ttu-id="f4dc3-122">Das Adressbuch wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="f4dc3-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="f4dc3-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="f4dc3-124">Der Anruf ist erfolgreich, aber die Container eines oder mehreren Adressbuchanbietern konnten nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="f4dc3-125">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f4dc3-126">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f4dc3-127">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f4dc3-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4dc3-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4dc3-128">Remarks</span></span>

<span data-ttu-id="f4dc3-129">Die **IMAPISession::OpenAddressBook-Methode** öffnet das integrierte MAPI-Adressbuch, eine Auflistung der Container auf oberster Ebene aller Adressbuchanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="f4dc3-130">Der zeiger, der im  _lppAdrBook-Parameter_ zurückgegeben wird, bietet weiteren Zugriff auf den Inhalt des Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="f4dc3-131">Dadurch kann der Anrufer Aufgaben ausführen, z. B. das Öffnen einzelner Container, das Suchen von Messagingbenutzern und das Anzeigen von Allgemeinen Adressdialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4dc3-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f4dc3-132">Notes to callers</span></span>

 <span data-ttu-id="f4dc3-133">**OpenAddressBook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn es einen oder mehrere Adressbuchanbieter nicht in das Profil laden kann.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="f4dc3-134">Dieser Wert ist eine Warnung und kein Fehlerwert. behandeln, wie Sie es S_OK.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="f4dc3-135">**OpenAddressBook** gibt immer einen gültigen Zeiger im  _lppAdrBook-Parameter_ zurück, unabhängig davon, wie viele Adressbuchanbieter nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="f4dc3-136">Daher müssen Sie immer die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Adressbuchs an einem bestimmten Punkt aufrufen, bevor Sie sich abmelden.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="f4dc3-137">Wenn **OpenAddressBook** MAPI_W_ERRORS_RETURNED, rufen Sie [IMAPISession::GetLastError](imapisession-getlasterror.md) auf, um eine [MAPIERROR-Struktur](mapierror.md) zu erhalten, die Informationen zu den fehlerhaften Anbietern enthält.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="f4dc3-138">Es wird **eine einzelne MAPIERROR-Struktur** zurückgegeben, die Informationen enthält, die von allen Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4dc3-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f4dc3-139">MFCMAPI reference</span></span>

<span data-ttu-id="f4dc3-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4dc3-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f4dc3-141">**File**</span></span>|<span data-ttu-id="f4dc3-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f4dc3-142">**Function**</span></span>|<span data-ttu-id="f4dc3-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f4dc3-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4dc3-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="f4dc3-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="f4dc3-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="f4dc3-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="f4dc3-146">MFCMAPI verwendet die **IMAPISession::OpenAddressBook-Methode,** um das integrierte Adressbuch zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4dc3-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4dc3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4dc3-147">See also</span></span>



[<span data-ttu-id="f4dc3-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4dc3-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="f4dc3-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f4dc3-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="f4dc3-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f4dc3-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f4dc3-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4dc3-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f4dc3-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f4dc3-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

