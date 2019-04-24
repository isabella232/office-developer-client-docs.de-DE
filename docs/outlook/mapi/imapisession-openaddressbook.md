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
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329421"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="7a0cc-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="7a0cc-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="7a0cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a0cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a0cc-105">Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook](iaddrbookimapiprop.md) -Zeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="7a0cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a0cc-106">Parameters</span></span>

 <span data-ttu-id="7a0cc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7a0cc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7a0cc-108">in Ein Handle für das übergeordnete Fenster des Dialogfelds "allgemeine Adresse" und andere zugehörige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="7a0cc-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7a0cc-109">_lpInterface_</span></span>
  
> <span data-ttu-id="7a0cc-110">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Adressbuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="7a0cc-111">Beim Übergeben von **null** wird ein Zeiger auf die Standardschnittstelle des Adressbuchs [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="7a0cc-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a0cc-112">_ulFlags_</span></span>
  
> <span data-ttu-id="7a0cc-113">in Eine Bitmaske von Flags, die das Öffnen des Adressbuchs steuert.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="7a0cc-114">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7a0cc-114">The following flag can be set:</span></span>
    
<span data-ttu-id="7a0cc-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7a0cc-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="7a0cc-116">Unterdrückt die Anzeige von Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="7a0cc-117">Wenn das AB_NO_DIALOG-Flag nicht festgelegt ist, können die Adressbuchanbieter, die zum integrierten Adressbuch beitragen, den Benutzer um erforderliche Informationen auffordern.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="7a0cc-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="7a0cc-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="7a0cc-119">Out Ein Zeiger auf einen Zeiger auf das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a0cc-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a0cc-120">Return value</span></span>

<span data-ttu-id="7a0cc-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a0cc-121">S_OK</span></span> 
  
> <span data-ttu-id="7a0cc-122">Das Adressbuch wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="7a0cc-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="7a0cc-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="7a0cc-124">Der Aufruf war erfolgreich, aber die Container eines oder mehrerer Adressbuchanbieter konnten nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="7a0cc-125">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7a0cc-126">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7a0cc-127">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7a0cc-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a0cc-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a0cc-128">Remarks</span></span>

<span data-ttu-id="7a0cc-129">Die **IMAPISession:: openaddressbook** -Methode öffnet das integrierte MAPI-Adressbuch, eine Sammlung der Container der obersten Ebene aller Adressbuchanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="7a0cc-130">Der im Parameter _lppAdrBook_ zurückgegebene Zeiger bietet weiteren Zugriff auf den Inhalt des Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="7a0cc-131">Dadurch kann der Anrufer Aufgaben wie das Öffnen einzelner Container, das Auffinden von Messaging Benutzern und das Anzeigen allgemeiner Adress Dialogfelder ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a0cc-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7a0cc-132">Notes to callers</span></span>

 <span data-ttu-id="7a0cc-133">**Openaddressbook** gibt MAPI_W_ERRORS_RETURNED zurück, wenn ein oder mehrere Adressbuchanbieter im Profil nicht geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="7a0cc-134">Dieser Wert ist eine Warnung, kein Fehlerwert; behandeln Sie Sie wie S_OK.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="7a0cc-135">**Openaddressbook** gibt immer einen gültigen Zeiger im _lppAdrBook_ -Parameter zurück, unabhängig davon, wie viele Adressbuchanbieter nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="7a0cc-136">Daher müssen Sie vor dem Abmelden immer die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode des Adressbuchs aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="7a0cc-137">Wenn **Openaddressbook** MAPI_W_ERRORS_RETURNED zurückgibt, rufen Sie [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) auf, um eine [MAPIERROR](mapierror.md) -Struktur abzurufen, die Informationen zu den fehlerhaften Anbietern enthält.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="7a0cc-138">Es wird eine einzelne **MAPIERROR** -Struktur zurückgegeben, die von allen Anbietern bereitgestellte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7a0cc-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7a0cc-139">MFCMAPI reference</span></span>

<span data-ttu-id="7a0cc-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7a0cc-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7a0cc-141">**File**</span></span>|<span data-ttu-id="7a0cc-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7a0cc-142">**Function**</span></span>|<span data-ttu-id="7a0cc-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7a0cc-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a0cc-144">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="7a0cc-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="7a0cc-145">CMapiObjects:: GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="7a0cc-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="7a0cc-146">MFCMAPI verwendet die **IMAPISession:: openaddressbook** -Methode, um das integrierte Adressbuch abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a0cc-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a0cc-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a0cc-147">See also</span></span>



[<span data-ttu-id="7a0cc-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7a0cc-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="7a0cc-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7a0cc-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="7a0cc-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="7a0cc-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="7a0cc-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a0cc-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="7a0cc-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7a0cc-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

