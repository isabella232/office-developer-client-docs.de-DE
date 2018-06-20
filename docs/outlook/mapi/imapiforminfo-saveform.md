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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e2d757fe329f9a57447723d72a859c7d82fc2b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792168"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="b4094-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="b4094-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="b4094-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4094-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4094-105">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="b4094-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="b4094-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4094-106">Parameters</span></span>

 <span data-ttu-id="b4094-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="b4094-107">_szFileName_</span></span>
  
> <span data-ttu-id="b4094-108">[in] Eine Zeichenfolge, die das Formular Nachricht Beschreibungsdatei benennt, in dem die Beschreibung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b4094-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="b4094-109">Gibt den Dateinamen muss die .fdm-Erweiterung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b4094-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4094-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b4094-110">Return value</span></span>

<span data-ttu-id="b4094-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4094-111">S_OK</span></span> 
  
> <span data-ttu-id="b4094-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b4094-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b4094-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="b4094-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="b4094-114">Die Konfigurationsdatei konnte nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b4094-114">The configuration file could not be written.</span></span> <span data-ttu-id="b4094-115">Um die Struktur [MAPIERROR](mapierror.md) abzurufen, die dem Fehler zugeordnet ist, rufen Sie die [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b4094-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="b4094-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b4094-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b4094-117">**SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im Container lokale Formular zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b4094-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="b4094-118">**SaveForm** wird für den Container lokale Formular nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4094-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b4094-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4094-119">Remarks</span></span>

<span data-ttu-id="b4094-120">Clientanwendungen rufen Sie die **IMAPIFormInfo::SaveForm** -Methode, um eine Beschreibung des aktuellen Formulars in der Datei zu speichern, die den angegebenen Dateinamen hat.</span><span class="sxs-lookup"><span data-stu-id="b4094-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="b4094-121">**SaveForm** erstellt eine Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="b4094-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b4094-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b4094-122">Notes to callers</span></span>

<span data-ttu-id="b4094-123">Sie können Formulare, indem Sie sie aus einer Liste von Formular Deskriptor Nachrichten in einem Dialogfeld, die Bibliothek Anbieter Anzeige bilden auswählen installieren.</span><span class="sxs-lookup"><span data-stu-id="b4094-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="b4094-124">Die empfohlene Erweiterung für das Formular Deskriptor Nachrichten ist .fdm.</span><span class="sxs-lookup"><span data-stu-id="b4094-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="b4094-125">Rufen Sie die Methode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) **SaveForm** MAPI_E_EXTENDED_ERROR zurück, und überprüfen Sie die zurückgegebene **MAPIERROR** -Struktur, um die Bedingung zu ermitteln, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="b4094-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4094-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4094-126">See also</span></span>



[<span data-ttu-id="b4094-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b4094-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b4094-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b4094-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b4094-129">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b4094-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

