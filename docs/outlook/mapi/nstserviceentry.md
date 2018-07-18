---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793289"
---
# <a name="nstserviceentry"></a><span data-ttu-id="316cb-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="316cb-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="316cb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="316cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="316cb-105">Nachricht Service Entry Point-Funktion für MAPI-Speicheranbieter umfließt einen PST-basierten lokalen Speicher als NST Speicher.</span><span class="sxs-lookup"><span data-stu-id="316cb-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="316cb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="316cb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="316cb-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="316cb-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="316cb-108">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="316cb-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="316cb-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="316cb-109">Called by:</span></span>  <br/> |<span data-ttu-id="316cb-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="316cb-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="316cb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="316cb-111">Parameters</span></span>

 <span data-ttu-id="316cb-112">**NSTServiceEntry** verwendet den **[MSGSERVICEENTRY](msgserviceentry.md)** Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="316cb-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="316cb-113">Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="316cb-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="316cb-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="316cb-114">Return values</span></span>

<span data-ttu-id="316cb-115">Informationen zu Rückgabewerte finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="316cb-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="316cb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="316cb-116">Remarks</span></span>

<span data-ttu-id="316cb-117">Wenn **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** für die Adresse des dieser Funktion in msmapi32.dll suchen, geben Sie "NSTServiceEntry" als den Namen der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="316cb-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="316cb-118">Um die Replikation-API verwenden, muss ein MAPI-Anbieter zuerst öffnen und in eine PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)** umgebrochen.</span><span class="sxs-lookup"><span data-stu-id="316cb-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="316cb-119">Der Anbieter können Sie die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)**, um die Replikation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="316cb-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="316cb-120">Die folgenden Anmerkungen gelten für einen Speicher NST:</span><span class="sxs-lookup"><span data-stu-id="316cb-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="316cb-121">Speichern Sie alle Informationen nicht im Abschnitt globale Profile beim Implementieren von eines MAPI-Anbieters, der die **NSTServiceEntry**verwendet.</span><span class="sxs-lookup"><span data-stu-id="316cb-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="316cb-122">Abschnitt globale Profile von vielen Anbietern freigegeben und können in diesem Profil gespeicherte Daten überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="316cb-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="316cb-123">Nur Elemente mit vorhandenen Änderung Zeitstempel erhalten ihre Stempel aktualisiert, wenn sie gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="316cb-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="316cb-124">Überprüfung von Konflikt tritt nicht automatisch auf Wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="316cb-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="316cb-125">Erkennung von Duplikaten tritt nicht auf, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="316cb-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="316cb-126">Die Datei, die die zwischengespeicherte Version des Servers darstellt angehängt ist. NST.</span><span class="sxs-lookup"><span data-stu-id="316cb-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="316cb-127">Um einen Zeiger auf den Profilabschnitt globale zu ermitteln, ruft eine Message Service **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** im Support-Objekt mit **PbNSTGlobalProfileSectionGuid** wie unten definiert:</span><span class="sxs-lookup"><span data-stu-id="316cb-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="316cb-128">In diesem Fall sollten das Support-Objekt des Diensts Nachricht sicherstellen, dass **IMAPISupport::OpenProfileSection** Profilabschnitt zurückgegeben, der von der **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft in den Abschnitt für das Standardprofil identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="316cb-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="316cb-129">Wenn in diesem Profilabschnitt erhalten möchten, kann das Support-Objekt öffnen Sie den Abschnitt für das Standardprofil, **PR_SERVICE_UID**abrufen und übergeben Sie das Ergebnis an **IMAPISupport::OpenProfileSection** den richtige globale Profilabschnitt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="316cb-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="316cb-130">Die Support-Objekts gibt einen Zeiger wiederum für diesen Profilabschnitt globale mit dem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="316cb-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="316cb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="316cb-131">See also</span></span>



[<span data-ttu-id="316cb-132">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="316cb-132">About the Replication API</span></span>](about-the-replication-api.md)

