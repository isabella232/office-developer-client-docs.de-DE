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
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280054"
---
# <a name="nstserviceentry"></a><span data-ttu-id="7db4f-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="7db4f-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="7db4f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7db4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7db4f-105">Nachrichtendienst-Einstiegspunktfunktion für einen MAPI-Speicheranbieter zum Umschließen eines PST-basierten lokalen Speichers als NST-Speicher.</span><span class="sxs-lookup"><span data-stu-id="7db4f-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7db4f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7db4f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7db4f-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7db4f-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="7db4f-108">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7db4f-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="7db4f-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7db4f-109">Called by:</span></span>  <br/> |<span data-ttu-id="7db4f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7db4f-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7db4f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7db4f-111">Parameters</span></span>

 <span data-ttu-id="7db4f-112">**NSTServiceEntry** verwendet den Prototyp der **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7db4f-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="7db4f-113">Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="7db4f-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="7db4f-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7db4f-114">Return values</span></span>

<span data-ttu-id="7db4f-115">Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="7db4f-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7db4f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7db4f-116">Remarks</span></span>

<span data-ttu-id="7db4f-117">Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an.</span><span class="sxs-lookup"><span data-stu-id="7db4f-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="7db4f-118">Um die Replikations-API verwenden zu können, muss ein MAPI-Speicheranbieter zunächst einen PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)** öffnen und einbinden.</span><span class="sxs-lookup"><span data-stu-id="7db4f-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="7db4f-119">Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="7db4f-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="7db4f-120">Die folgenden Hinweise gelten für einen NST-Speicher:</span><span class="sxs-lookup"><span data-stu-id="7db4f-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="7db4f-121">Speichern Sie keine Informationen im Abschnitt globaler Profil beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry**verwendet.</span><span class="sxs-lookup"><span data-stu-id="7db4f-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="7db4f-122">Der Abschnitt globaler Profil wird von vielen Anbietern gemeinsam genutzt, und in diesem Profil gespeicherte Daten können überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7db4f-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="7db4f-123">Nur Elemente mit vorhandenen Änderungszeit Stempeln erhalten ihre Stempel beim Speichern aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7db4f-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="7db4f-124">Die Konfliktüberprüfung tritt nicht automatisch auf, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7db4f-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="7db4f-125">Doppelte Erkennung tritt nicht auf, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7db4f-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="7db4f-126">Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird angefügt. NST.</span><span class="sxs-lookup"><span data-stu-id="7db4f-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="7db4f-127">Wenn Sie einen Zeiger auf den Abschnitt globales Profil erhalten möchten, Ruft ein Nachrichtendienst **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** im Support-Objekt mithilfe von **pbNSTGlobalProfileSectionGuid** wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="7db4f-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="7db4f-128">In diesem Fall sollte das Unterstützungsobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport:: OpenProfileSection** den Profil Abschnitt zurückgibt, der durch die **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft im Standardprofil Abschnitt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7db4f-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="7db4f-129">Zum Abrufen dieses Profil Abschnitts kann das Support Objekt den Standardprofil Abschnitt öffnen, **PR_SERVICE_UID**abrufen und das Ergebnis an **IMAPISupport:: OpenProfileSection** zum Abrufen des richtigen globalen Profil Abschnitts weitergeben.</span><span class="sxs-lookup"><span data-stu-id="7db4f-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="7db4f-130">Das Support-Objekt gibt wiederum einen Zeiger auf diesen Abschnitt des globalen Profils an den Nachrichtendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="7db4f-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7db4f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7db4f-131">See also</span></span>



[<span data-ttu-id="7db4f-132">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="7db4f-132">About the Replication API</span></span>](about-the-replication-api.md)

