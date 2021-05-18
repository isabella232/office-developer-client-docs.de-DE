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
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405086"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="b6a5a-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="b6a5a-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="b6a5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6a5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6a5a-105">Installiert ein Formular in einer Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="b6a5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6a5a-106">Parameters</span></span>

 <span data-ttu-id="b6a5a-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b6a5a-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b6a5a-108">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="b6a5a-109">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, die Clientanwendung legt das MAPI_DIALOG im  _ulFlags-Parameter_ fest.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b6a5a-110">Der  _ulUIParam-Parameter_ kann NULL sein, MAPI_DIALOG nicht auch übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="b6a5a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6a5a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b6a5a-112">[in] Eine Bitmaske mit Flags, die die Installation des Formulars steuert.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="b6a5a-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b6a5a-113">The following flags can be set:</span></span>
    
<span data-ttu-id="b6a5a-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b6a5a-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b6a5a-115">Zeigt ein Dialogfeld an, um Statusinformationen zur Verfügung zu stellen oder den Benutzer zu weiteren Informationen aufforderen.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="b6a5a-116">Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="b6a5a-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6a5a-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b6a5a-118">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b6a5a-119">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="b6a5a-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="b6a5a-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="b6a5a-121">Wenn bereits ein anderes Formular vorhanden ist, das die von diesem Formular behandelte Nachrichtenklasse behandelt, ersetzen Sie das vorhandene Formular durch dieses Formular.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="b6a5a-122">Dieses Flag wird ignoriert, wenn MAPI_DIALOG auch vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="b6a5a-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="b6a5a-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="b6a5a-124">[in] Der Pfad zur Konfigurationsdatei des Formulars.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6a5a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6a5a-125">Return value</span></span>

<span data-ttu-id="b6a5a-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6a5a-126">S_OK</span></span> 
  
> <span data-ttu-id="b6a5a-127">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b6a5a-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="b6a5a-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="b6a5a-129">Ein Implementierungsfehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-129">An implementation error occurred.</span></span> <span data-ttu-id="b6a5a-130">Rufen Sie die [IMAPIFormContainer::GetLastError-Methode](imapiformcontainer-getlasterror.md) auf, um die [MAPIERROR-Struktur](mapierror.md) zu erhalten, die dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="b6a5a-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b6a5a-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b6a5a-132">Der Benutzer hat die Installation des Formulars abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b6a5a-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b6a5a-133">Notes to implementers</span></span>

<span data-ttu-id="b6a5a-134">Formularbibliotheksanbieter sollten eine **MAPIERROR-Struktur** ausfüllen und MAPI_E_EXTENDED_ERROR, wenn eine der folgenden Bedingungen auftritt:</span><span class="sxs-lookup"><span data-stu-id="b6a5a-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="b6a5a-135">Die Konfigurationsdatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="b6a5a-136">Die Konfigurationsdatei ist nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="b6a5a-137">Die Konfigurationsdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="b6a5a-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b6a5a-138">Notes to callers</span></span>

<span data-ttu-id="b6a5a-139">Clientanwendungen rufen die **IMAPIFormContainer::InstallForm-Methode** auf, um ein Formular in einem bestimmten Formularcontainer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="b6a5a-140">Der  _Parameter szCfgPathName_ muss den Pfad einer Formularkonfigurationsdatei enthalten (d. h. eine Datei mit der Erweiterung .cfg, die das Formular und dessen Implementierung beschreibt).</span><span class="sxs-lookup"><span data-stu-id="b6a5a-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="b6a5a-141">Die Flags im  _ulFlags-Parameter_ geben Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="b6a5a-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="b6a5a-142">Wenn das MAPI_DIALOG festgelegt ist, wird eine Benutzeroberfläche angezeigt, mit der der Benutzer, der das Formular installiert, Installationsdetails angeben kann.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="b6a5a-143">Wenn das MAPIFORM_INSTALL_OVERWRITEONCONFLICT festgelegt ist, wird jedes vorherige Formular für dieselbe Nachrichtenklasse durch das zu installierende Formular ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="b6a5a-144">Andernfalls wird die Formularinstallation mit der aktuellen Formularbeschreibung zusammengeführt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="b6a5a-145">Wenn MAPI_DIALOG festgelegt ist, wird MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="b6a5a-146">Das Fehlen MAPIFORM_INSTALL_OVERWRITEONCONFLICT im Flagsatz bedeutet, dass eine Zusammenführung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="b6a5a-147">Alle neuen Plattformen in der CFG-Datei, die derzeit nicht in der Formularbeschreibung vorhanden sind, werden installiert, und es werden keine weiteren Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="b6a5a-148">Wenn das MAPI_UNICODE festgelegt ist, ist der Pfad der Formularkonfigurationsdatei eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="b6a5a-149">Clients sollten [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) aufrufen, wenn **InstallForm** MAPI_E_EXTENDED_ERROR zurückgibt, und sie sollten die zurückgegebene [MAPIERROR-Struktur](mapierror.md) überprüfen, um die Bedingung zu ermitteln, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6a5a-150">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b6a5a-150">MFCMAPI reference</span></span>

<span data-ttu-id="b6a5a-151">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6a5a-152">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b6a5a-152">**File**</span></span>|<span data-ttu-id="b6a5a-153">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b6a5a-153">**Function**</span></span>|<span data-ttu-id="b6a5a-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b6a5a-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6a5a-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b6a5a-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="b6a5a-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="b6a5a-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="b6a5a-157">MFCMAPI verwendet die **IMAPIFormContainer::InstallForm-Methode,** um ein Formular in einem Formularcontainer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b6a5a-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6a5a-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6a5a-158">See also</span></span>



[<span data-ttu-id="b6a5a-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b6a5a-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b6a5a-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6a5a-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="b6a5a-161">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b6a5a-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

