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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dcde242f5f2e956d1926d6914431008383f5aa55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792309"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="b7ac7-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="b7ac7-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="b7ac7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7ac7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7ac7-105">Öffnet das MAPI-integrierte Adressbuch, einen [IAddrBook](iaddrbookimapiprop.md) Zeiger für den weiteren Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="b7ac7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7ac7-106">Parameters</span></span>

 <span data-ttu-id="b7ac7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b7ac7-108">[in] Ein Handle für das übergeordnete Fenster der Adresse Standarddialogfeld und anderer weiterführende zeigt.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="b7ac7-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-109">_lpInterface_</span></span>
  
> <span data-ttu-id="b7ac7-110">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für das Adressbuch zugreifen zu verwendende darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="b7ac7-111">Übergeben von **null** gibt einen Zeiger auf das Adressbuch Standardschnittstelle, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b7ac7-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="b7ac7-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-112">_ulFlags_</span></span>
  
> <span data-ttu-id="b7ac7-113">[in] Eine Bitmaske aus Flags, die das Öffnen des Adressbuchs steuert.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="b7ac7-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b7ac7-114">The following flag can be set:</span></span>
    
<span data-ttu-id="b7ac7-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b7ac7-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="b7ac7-116">Unterdrückt die Anzeige von Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="b7ac7-117">Wenn das Flag AB_NO_DIALOG nicht festgelegt ist, können die adressbuchanbietern implementierte, die auf die integrierte Adressbuch beitragen der Benutzer für alle erforderlichen Informationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="b7ac7-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="b7ac7-119">[out] Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7ac7-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b7ac7-120">Return value</span></span>

<span data-ttu-id="b7ac7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7ac7-121">S_OK</span></span> 
  
> <span data-ttu-id="b7ac7-122">Das Adressbuch wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="b7ac7-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="b7ac7-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="b7ac7-124">Der Aufruf war erfolgreich, aber die Container für eine oder mehrere adressbuchanbietern implementierte konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="b7ac7-125">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b7ac7-126">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b7ac7-127">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b7ac7-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7ac7-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7ac7-128">Remarks</span></span>

<span data-ttu-id="b7ac7-129">Die **IMAPISession::OpenAddressBook** -Methode öffnet das integrierte Adressbuch MAPI, eine Auflistung von Container der obersten Ebene aller von der adressbuchanbietern implementierte im Profil.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="b7ac7-130">Der Zeiger, der im Parameter _LppAdrBook_ zurückgegeben wird, bietet weitere Zugriff auf den Inhalt des Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="b7ac7-131">Dadurch wird den Anrufer für Aufgaben wie öffnen einzelne Container, messaging Benutzer suchen und Anzeigen von Dialogfeldern für allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7ac7-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b7ac7-132">Notes to callers</span></span>

 <span data-ttu-id="b7ac7-133">**OpenAddressBook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn mindestens eines der adressbuchanbietern implementierte im Profil geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="b7ac7-134">Dieser Wert ist eine Warnung, keinen Fehlerwert. Behandeln Sie es wie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="b7ac7-135">**OpenAddressBook** gibt immer einen gültigen Zeiger in der _LppAdrBook_ -Parameter, unabhängig davon, wie viele der Address Book Anbieter konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="b7ac7-136">Aus diesem Grund müssen Sie zu einem bestimmten Zeitpunkt auch immer im Adressbuch [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, vor der Abmeldung.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="b7ac7-137">Wenn **OpenAddressBook** MAPI_W_ERRORS_RETURNED zurückgegeben wird, rufen Sie [IMAPISession::GetLastError](imapisession-getlasterror.md) um eine [MAPIERROR](mapierror.md) -Struktur zu erhalten, die Informationen zu den fehlerhaften Anbietern enthält.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="b7ac7-138">Eine einzelne **MAPIERROR** -Struktur zurückgegeben, die Informationen von alle Anbieter bereitgestellt wird, enthält.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b7ac7-139">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="b7ac7-139">MFCMAPI reference</span></span>

<span data-ttu-id="b7ac7-140">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b7ac7-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b7ac7-141">**File**</span></span>|<span data-ttu-id="b7ac7-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b7ac7-142">**Function**</span></span>|<span data-ttu-id="b7ac7-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b7ac7-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7ac7-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="b7ac7-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="b7ac7-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="b7ac7-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="b7ac7-146">MFCMAPI (engl.) verwendet die **IMAPISession::OpenAddressBook** -Methode, um die integrierten Adressbuch abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7ac7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7ac7-147">See also</span></span>



[<span data-ttu-id="b7ac7-148">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7ac7-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="b7ac7-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b7ac7-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="b7ac7-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b7ac7-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b7ac7-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7ac7-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b7ac7-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b7ac7-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

