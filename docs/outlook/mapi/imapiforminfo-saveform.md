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
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593473"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="da8d8-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="da8d8-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="da8d8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da8d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da8d8-105">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="da8d8-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="da8d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da8d8-106">Parameters</span></span>

 <span data-ttu-id="da8d8-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="da8d8-107">_szFileName_</span></span>
  
> <span data-ttu-id="da8d8-108">[in] Eine Zeichenfolge, die das Formular Nachricht Beschreibungsdatei benennt, in dem die Beschreibung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="da8d8-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="da8d8-109">Gibt den Dateinamen muss die .fdm-Erweiterung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="da8d8-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da8d8-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="da8d8-110">Return value</span></span>

<span data-ttu-id="da8d8-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="da8d8-111">S_OK</span></span> 
  
> <span data-ttu-id="da8d8-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="da8d8-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="da8d8-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="da8d8-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="da8d8-114">Die Konfigurationsdatei konnte nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="da8d8-114">The configuration file could not be written.</span></span> <span data-ttu-id="da8d8-115">Um die Struktur [MAPIERROR](mapierror.md) abzurufen, die dem Fehler zugeordnet ist, rufen Sie die [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="da8d8-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="da8d8-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="da8d8-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="da8d8-117">**SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im Container lokale Formular zu speichern.</span><span class="sxs-lookup"><span data-stu-id="da8d8-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="da8d8-118">**SaveForm** wird für den Container lokale Formular nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da8d8-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="da8d8-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="da8d8-119">Remarks</span></span>

<span data-ttu-id="da8d8-120">Clientanwendungen rufen Sie die **IMAPIFormInfo::SaveForm** -Methode, um eine Beschreibung des aktuellen Formulars in der Datei zu speichern, die den angegebenen Dateinamen hat.</span><span class="sxs-lookup"><span data-stu-id="da8d8-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="da8d8-121">**SaveForm** erstellt eine Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="da8d8-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="da8d8-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="da8d8-122">Notes to callers</span></span>

<span data-ttu-id="da8d8-123">Sie können Formulare, indem Sie sie aus einer Liste von Formular Deskriptor Nachrichten in einem Dialogfeld, die Bibliothek Anbieter Anzeige bilden auswählen installieren.</span><span class="sxs-lookup"><span data-stu-id="da8d8-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="da8d8-124">Die empfohlene Erweiterung für das Formular Deskriptor Nachrichten ist .fdm.</span><span class="sxs-lookup"><span data-stu-id="da8d8-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="da8d8-125">Rufen Sie die Methode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) **SaveForm** MAPI_E_EXTENDED_ERROR zurück, und überprüfen Sie die zurückgegebene **MAPIERROR** -Struktur, um die Bedingung zu ermitteln, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="da8d8-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da8d8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da8d8-126">See also</span></span>



[<span data-ttu-id="da8d8-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="da8d8-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="da8d8-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="da8d8-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="da8d8-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="da8d8-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

