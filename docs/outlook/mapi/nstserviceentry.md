---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280054"
---
# <a name="nstserviceentry"></a><span data-ttu-id="953d5-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="953d5-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="953d5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="953d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="953d5-105">Message Service Entry Points-Funktion für einen MAPI-Speicheranbieter, um einen PST-basierten lokalen Speicher als NST-Speicher einzubinden.</span><span class="sxs-lookup"><span data-stu-id="953d5-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="953d5-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="953d5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="953d5-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="953d5-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="953d5-108">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="953d5-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="953d5-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="953d5-109">Called by:</span></span>  <br/> |<span data-ttu-id="953d5-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="953d5-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="953d5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="953d5-111">Parameters</span></span>

 <span data-ttu-id="953d5-112">**NSTServiceEntry** verwendet den Prototyp der **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="953d5-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="953d5-113">Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="953d5-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="953d5-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="953d5-114">Return values</span></span>

<span data-ttu-id="953d5-115">Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="953d5-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="953d5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="953d5-116">Remarks</span></span>

<span data-ttu-id="953d5-117">Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an.</span><span class="sxs-lookup"><span data-stu-id="953d5-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="953d5-118">Um die Replikations-API verwenden zu können, muss ein MAPI-Speicheranbieter zuerst einen PST-basierten lokalen Speicher öffnen und umbrechen, indem er **[NSTServiceEntry](nstserviceentry.md)** aufruft.</span><span class="sxs-lookup"><span data-stu-id="953d5-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="953d5-119">Der Anbieter kann dann die Hauptschnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="953d5-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="953d5-120">Die folgenden Hinweise gelten für einen NST-Speicher:</span><span class="sxs-lookup"><span data-stu-id="953d5-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="953d5-121">Speichern Sie beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry**verwendet, keine Informationen im Abschnitt globales Profil.</span><span class="sxs-lookup"><span data-stu-id="953d5-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="953d5-122">Der Abschnitt "globaler Profil" wird von vielen Anbietern freigegeben, und die in diesem Profil gespeicherten Daten können überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="953d5-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="953d5-123">Nur Elemente mit vorhandenen Änderungszeit Stempeln erhalten ihre Stempel aktualisiert, wenn Sie gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="953d5-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="953d5-124">Die Konfliktprüfung tritt nicht automatisch ein, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="953d5-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="953d5-125">Die doppelte Erkennung tritt nicht auf, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="953d5-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="953d5-126">Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird angehängt. NST.</span><span class="sxs-lookup"><span data-stu-id="953d5-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="953d5-127">Um einen Zeiger auf den Abschnitt "Global profile" zu erhalten, Ruft ein Nachrichtendienst **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** im Unterstützungsobjekt mit **pbNSTGlobalProfileSectionGuid** wie unten definiert auf:</span><span class="sxs-lookup"><span data-stu-id="953d5-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="953d5-128">In diesem Fall sollte das Unterstützungsobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport:: OpenProfileSection** den Profil Abschnitt zurückgibt, der von der **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft im Standardprofil Abschnitt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="953d5-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="953d5-129">Zum Abrufen dieses Profil Abschnitts kann das Support Objekt den Standardprofil Abschnitt öffnen, **PR_SERVICE_UID**abrufen und das Ergebnis an **IMAPISupport:: OpenProfileSection** übergeben, um den richtigen globalen Profil Abschnitt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="953d5-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="953d5-130">Das Unterstützungsobjekt wiederum gibt einen Zeiger auf diesen globalen Profil Abschnitt zum Nachrichtendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="953d5-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="953d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="953d5-131">See also</span></span>



[<span data-ttu-id="953d5-132">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="953d5-132">About the Replication API</span></span>](about-the-replication-api.md)

