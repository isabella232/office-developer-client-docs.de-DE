---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428746"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="08253-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="08253-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="08253-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08253-105">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="08253-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="08253-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08253-106">Parameters</span></span>

 <span data-ttu-id="08253-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="08253-107">_szFileName_</span></span>
  
> <span data-ttu-id="08253-108">[in] Eine Zeichenfolge, die die Beschreibungsnachrichtendatei des Formulars benennt, in der die Beschreibung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="08253-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="08253-109">Dieser Dateiname muss die .fdm-Erweiterung haben.</span><span class="sxs-lookup"><span data-stu-id="08253-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08253-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08253-110">Return value</span></span>

<span data-ttu-id="08253-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="08253-111">S_OK</span></span> 
  
> <span data-ttu-id="08253-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="08253-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08253-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="08253-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="08253-114">Die Konfigurationsdatei konnte nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08253-114">The configuration file could not be written.</span></span> <span data-ttu-id="08253-115">Rufen Sie die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, um die [MAPIERROR-Struktur](mapierror.md) zu erhalten, die dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08253-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="08253-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="08253-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="08253-117">**SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im lokalen Formularcontainer zu speichern.</span><span class="sxs-lookup"><span data-stu-id="08253-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="08253-118">**SaveForm** wird im lokalen Formularcontainer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08253-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08253-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08253-119">Remarks</span></span>

<span data-ttu-id="08253-120">Clientanwendungen rufen die **IMAPIFormInfo::SaveForm-Methode** auf, um eine Beschreibung des aktuellen Formulars in der Datei mit dem angegebenen Dateinamen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="08253-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="08253-121">**SaveForm** erstellt eine Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="08253-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="08253-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="08253-122">Notes to callers</span></span>

<span data-ttu-id="08253-123">Sie können Formulare erneut installieren, indem Sie sie aus einer Liste von Formularbeschreibungsmeldungen in einem Dialogfeld auswählen, das von Formularbibliotheksanbietern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08253-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="08253-124">Die empfohlene Erweiterung für Formulardeskriptormeldungen ist .fdm.</span><span class="sxs-lookup"><span data-stu-id="08253-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="08253-125">Rufen Sie [die IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, wenn **SaveForm** MAPI_E_EXTENDED_ERROR zurückgibt, und überprüfen Sie die zurückgegebene **MAPIERROR-Struktur,** um die Bedingung zu ermitteln, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="08253-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08253-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08253-126">See also</span></span>



[<span data-ttu-id="08253-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="08253-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="08253-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="08253-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="08253-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="08253-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

