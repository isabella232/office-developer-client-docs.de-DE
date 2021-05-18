---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408348"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="97d4e-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="97d4e-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="97d4e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97d4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97d4e-105">Registriert Dateien für persönliche Ordner (PST) für die automatische Entsperrung, um weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="97d4e-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="97d4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97d4e-106">Parameters</span></span>

<span data-ttu-id="97d4e-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="97d4e-107">_pmval_</span></span>
  
> <span data-ttu-id="97d4e-108">[in] Eine [SPropValue-Struktur,](spropvalue.md) die einen Zeiger auf den Pfad der dynamic-link library (DLL) enthält, die registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97d4e-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="97d4e-109">Die Struktur hat die folgenden Merkmale:</span><span class="sxs-lookup"><span data-stu-id="97d4e-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="97d4e-110">Ein ulPropTag von [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="97d4e-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="97d4e-111">Eine MVszW-Werteigenschaft, die auf ein Array mit mit Nullen beendeten Unicode-Zeichenzeichenfolgen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="97d4e-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="97d4e-112">Weitere Informationen finden Sie im [Thema SWStringArray.](swstringarray.md)</span><span class="sxs-lookup"><span data-stu-id="97d4e-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="97d4e-113">Der SPropValue wird in einer MAPI-Eigenschaft im internen Bereich des PST gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97d4e-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="97d4e-114">Auf diese Eigenschaft kann für normale MAPI-Anwendungen nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="97d4e-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="97d4e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97d4e-115">Return value</span></span>

<span data-ttu-id="97d4e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="97d4e-116">S_OK</span></span> 
  
> <span data-ttu-id="97d4e-117">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="97d4e-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97d4e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97d4e-118">Remarks</span></span>

<span data-ttu-id="97d4e-119">Beibehaltene Registrierungen können sich negativ auf die Leistung von Anwendungen auswirken, z. B. Outlook und Windows Desktopsuche, die PSTs öffnen.</span><span class="sxs-lookup"><span data-stu-id="97d4e-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="97d4e-120">Berücksichtigen Sie den Leistungseffekt, wenn Sie die Verwendung von dauerhaften Registrierungen verwenden oder erweitern.</span><span class="sxs-lookup"><span data-stu-id="97d4e-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="97d4e-121">Diese Methode ist nur für Unicode implementiert.</span><span class="sxs-lookup"><span data-stu-id="97d4e-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="97d4e-122">Darüber hinaus wird ein Präemptiv fehlschlagen, wenn einer der Pfade im Array keine Dateinamenerweiterung von .dll.</span><span class="sxs-lookup"><span data-stu-id="97d4e-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97d4e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97d4e-123">See also</span></span>

- [<span data-ttu-id="97d4e-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97d4e-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="97d4e-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97d4e-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

