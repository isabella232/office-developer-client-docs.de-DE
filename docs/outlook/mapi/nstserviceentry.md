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
# <a name="nstserviceentry"></a><span data-ttu-id="a8c37-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="a8c37-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="a8c37-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c37-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span><span class="sxs-lookup"><span data-stu-id="a8c37-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a8c37-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a8c37-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8c37-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a8c37-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8c37-108">MAPI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="a8c37-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="a8c37-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a8c37-109">Called by:</span></span>  <br/> |<span data-ttu-id="a8c37-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c37-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a8c37-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8c37-111">Parameters</span></span>

 <span data-ttu-id="a8c37-112">**NSTServiceEntry verwendet** den **[MSGSERVICEENTRY-Funktionsprototyp.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a8c37-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="a8c37-113">Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="a8c37-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="a8c37-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a8c37-114">Return values</span></span>

<span data-ttu-id="a8c37-115">Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="a8c37-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8c37-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8c37-116">Remarks</span></span>

<span data-ttu-id="a8c37-117">Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um in msmapi32.dll nach der Adresse dieser Funktion zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an.</span><span class="sxs-lookup"><span data-stu-id="a8c37-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="a8c37-118">Um die Replikations-API zu verwenden, muss ein MAPI-Speicheranbieter zunächst einen lokalen PST-basierten Speicher öffnen und umschließen, indem **[er NSTServiceEntry aufruft.](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a8c37-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="a8c37-119">Der Anbieter kann dann die Hauptschnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation zu durchführen.</span><span class="sxs-lookup"><span data-stu-id="a8c37-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="a8c37-120">Die folgenden Hinweise gelten für einen NST-Speicher:</span><span class="sxs-lookup"><span data-stu-id="a8c37-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="a8c37-121">Speichern Sie beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry** verwendet, keine Informationen im Abschnitt globales Profil.</span><span class="sxs-lookup"><span data-stu-id="a8c37-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="a8c37-122">Der Abschnitt "Globales Profil" wird von vielen Anbietern freigegeben, und in diesem Profil gespeicherte Daten können überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a8c37-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="a8c37-123">Nur Elemente mit vorhandenen Änderungszeitstempeln erhalten ihre Stempel aktualisiert, wenn sie gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a8c37-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="a8c37-124">Die Konfliktüberprüfung erfolgt nicht automatisch, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a8c37-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="a8c37-125">Die Duplikaterkennung erfolgt nicht, wenn Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a8c37-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="a8c37-126">Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird mit angefügt. NST.</span><span class="sxs-lookup"><span data-stu-id="a8c37-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="a8c37-127">Um einen Zeiger auf den globalen Profilabschnitt zu erhalten, ruft ein Nachrichtendienst **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** im Supportobjekt mithilfe von **pbNSTGlobalProfileSectionGuid** auf, wie unten definiert:</span><span class="sxs-lookup"><span data-stu-id="a8c37-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="a8c37-128">In diesem Fall sollte das Supportobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport::OpenProfileSection** den Profilabschnitt zurückgibt, der durch die **[PR_SERVICE_UID-Eigenschaft](pidtagserviceuid-canonical-property.md)** im Standardprofilabschnitt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a8c37-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="a8c37-129">Zum Abrufen dieses Profilabschnitts kann das Supportobjekt den Standardprofilabschnitt öffnen, **PR_SERVICE_UID** abrufen und das Ergebnis an **IMAPISupport::OpenProfileSection** übergeben, um den richtigen globalen Profilabschnitt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8c37-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="a8c37-130">Das Supportobjekt gibt wiederum einen Zeiger auf diesen globalen Profilabschnitt auf den Nachrichtendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="a8c37-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8c37-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8c37-131">See also</span></span>



[<span data-ttu-id="a8c37-132">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="a8c37-132">About the Replication API</span></span>](about-the-replication-api.md)

