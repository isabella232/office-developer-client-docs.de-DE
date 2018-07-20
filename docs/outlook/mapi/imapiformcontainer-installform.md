---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d329d3a14b6026d0bd62df9feba6ccff251e4151
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792147"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="418d3-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="418d3-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="418d3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="418d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="418d3-105">Wird ein Formular in einer Formularbibliothek installiert.</span><span class="sxs-lookup"><span data-stu-id="418d3-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="418d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="418d3-106">Parameters</span></span>

 <span data-ttu-id="418d3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="418d3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="418d3-108">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="418d3-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="418d3-109">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, die Clientanwendung das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="418d3-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="418d3-110">Der Parameter _UlUIParam_ kann NULL sein, wenn MAPI_DIALOG nicht auch übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="418d3-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="418d3-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="418d3-111">_ulFlags_</span></span>
  
> <span data-ttu-id="418d3-112">[in] Eine Bitmaske aus Flags, die die Installation des Formulars steuert.</span><span class="sxs-lookup"><span data-stu-id="418d3-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="418d3-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="418d3-113">The following flags can be set:</span></span>
    
<span data-ttu-id="418d3-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="418d3-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="418d3-115">Zeigt ein Dialogfeld zum Bereitstellen von Fortschrittsinformationen oder auffordern, Weitere Informationen an.</span><span class="sxs-lookup"><span data-stu-id="418d3-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="418d3-116">Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="418d3-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="418d3-117">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="418d3-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="418d3-118">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="418d3-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="418d3-119">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="418d3-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="418d3-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="418d3-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="418d3-121">Wenn ein anderes Formular bereits vorhanden, behandelt dieses Formular die Nachrichtenklasse behandelt ist, ersetzen Sie das bestehende Formular mit diesem.</span><span class="sxs-lookup"><span data-stu-id="418d3-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="418d3-122">Dieses Kennzeichen werden ignoriert, wenn das Flag MAPI_DIALOG auch vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="418d3-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="418d3-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="418d3-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="418d3-124">[in] Der Pfad zur Konfigurationsdatei für das Formular.</span><span class="sxs-lookup"><span data-stu-id="418d3-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="418d3-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="418d3-125">Return value</span></span>

<span data-ttu-id="418d3-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="418d3-126">S_OK</span></span> 
  
> <span data-ttu-id="418d3-127">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="418d3-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="418d3-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="418d3-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="418d3-129">Ein Implementierung Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="418d3-129">An implementation error occurred.</span></span> <span data-ttu-id="418d3-130">Um die Struktur [MAPIERROR](mapierror.md) abzurufen, die dem Fehler zugeordnet ist, rufen Sie die [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="418d3-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="418d3-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="418d3-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="418d3-132">Der Benutzer hat die Installation des Formulars, in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="418d3-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="418d3-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="418d3-133">Notes to implementers</span></span>

<span data-ttu-id="418d3-134">Formular Bibliothek Anbieter sollte eine **MAPIERROR** Struktur füllen und MAPI_E_EXTENDED_ERROR zurück, wenn Sie eine der folgenden Situationen auftreten:</span><span class="sxs-lookup"><span data-stu-id="418d3-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="418d3-135">Die Konfigurationsdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="418d3-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="418d3-136">Die Konfigurationsdatei kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="418d3-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="418d3-137">Die Konfigurationsdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="418d3-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="418d3-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="418d3-138">Notes to callers</span></span>

<span data-ttu-id="418d3-139">Clientanwendungen rufen Sie die **IMAPIFormContainer::InstallForm** -Methode, um ein Formular in ein bestimmtes Formular Container zu installieren.</span><span class="sxs-lookup"><span data-stu-id="418d3-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="418d3-140">Der Parameter _SzCfgPathName_ muss den Pfad einer Konfigurationsdatei Formular (d. h., eine Datei mit der cfg-Erweiterung, die das Formular und deren Implementierung beschreibt) enthalten.</span><span class="sxs-lookup"><span data-stu-id="418d3-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="418d3-141">Die Kennzeichen im Parameter _UlFlags_ geben Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="418d3-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="418d3-142">Wenn das Flag MAPI_DIALOG festgelegt ist, wird eine Benutzeroberfläche angezeigt, durch den Benutzer, der das Formular, um die Installationsdetails angeben installiert.</span><span class="sxs-lookup"><span data-stu-id="418d3-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="418d3-143">Wenn das Flag MAPIFORM_INSTALL_OVERWRITEONCONFLICT festgelegt ist, wird mit dem Formular installiert alle vorherigen Formular für dieselbe Nachrichtenklasse ersetzt.</span><span class="sxs-lookup"><span data-stu-id="418d3-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="418d3-144">Andernfalls wird die Installation des Formulars mit der aktuellen formularbeschreibung zusammengeführt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="418d3-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="418d3-145">Wenn MAPI_DIALOG festgelegt ist, wird die MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.</span><span class="sxs-lookup"><span data-stu-id="418d3-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="418d3-146">Das fehlen MAPIFORM_INSTALL_OVERWRITEONCONFLICT in das Flag festlegen bedeutet, die eine Zusammenführung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="418d3-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="418d3-147">Neuen Plattformen in die cfg-Datei, die nicht in der formularbeschreibung derzeit vorhanden sind installiert werden und keine anderen Änderungen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="418d3-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="418d3-148">Wenn die Option MAPI_UNICODE festgelegt ist, ist der Pfad der Konfigurationsdatei Formular eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="418d3-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="418d3-149">Clients sollte [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) aufrufen, wenn **InstallForm** MAPI_E_EXTENDED_ERROR zurückgegeben, und sie, dass die zurückgegebene [MAPIERROR](mapierror.md) -Struktur überprüfen sollten, um die Bedingung zu ermitteln, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="418d3-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="418d3-150">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="418d3-150">MFCMAPI reference</span></span>

<span data-ttu-id="418d3-151">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="418d3-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="418d3-152">**Datei**</span><span class="sxs-lookup"><span data-stu-id="418d3-152">**File**</span></span>|<span data-ttu-id="418d3-153">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="418d3-153">**Function**</span></span>|<span data-ttu-id="418d3-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="418d3-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="418d3-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="418d3-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="418d3-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="418d3-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="418d3-157">MFCMAPI (engl.) verwendet die **IMAPIFormContainer::InstallForm** -Methode, um ein Formular in einem Formular Container installieren.</span><span class="sxs-lookup"><span data-stu-id="418d3-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="418d3-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="418d3-158">See also</span></span>



[<span data-ttu-id="418d3-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="418d3-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="418d3-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="418d3-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="418d3-161">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="418d3-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

