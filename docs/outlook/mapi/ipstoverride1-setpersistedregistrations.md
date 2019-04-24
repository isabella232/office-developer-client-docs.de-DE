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
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315477"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="1490a-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="1490a-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="1490a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1490a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1490a-105">Registriert persönliche Ordner-Dateien (PST) für die automatische Entriegelung und verhindert weitere Aufrufe des HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="1490a-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="1490a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1490a-106">Parameters</span></span>

<span data-ttu-id="1490a-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="1490a-107">_pmval_</span></span>
  
> <span data-ttu-id="1490a-108">in Eine [SPropValue](spropvalue.md) -Struktur, die einen Zeiger auf den Pfad der zu registrierende Dynamic Link Library (dll) enthält.</span><span class="sxs-lookup"><span data-stu-id="1490a-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="1490a-109">Die Struktur weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="1490a-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="1490a-110">Ein ulPropTag von [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="1490a-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="1490a-111">Eine MVszW-Werteigenschaft, die auf ein Array von Zeichenfolgen mit null-terminierten Unicode-Zeichensätzen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1490a-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="1490a-112">Weitere Informationen finden Sie im Thema [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1490a-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1490a-113">Das SPropValue wird in einer MAPI-Eigenschaft im internen Datenbereichen des PST-Speichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1490a-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="1490a-114">Auf diese Eigenschaft kann für normale MAPI-Anwendungen nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="1490a-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1490a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1490a-115">Return value</span></span>

<span data-ttu-id="1490a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1490a-116">S_OK</span></span> 
  
> <span data-ttu-id="1490a-117">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1490a-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1490a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1490a-118">Remarks</span></span>

<span data-ttu-id="1490a-119">Dauerhafte Registrierungen können sich negativ auf die Leistung von Anwendungen wie Outlook und Windows-Desktop Suche auswirken, die PST öffnen.</span><span class="sxs-lookup"><span data-stu-id="1490a-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="1490a-120">Berücksichtigen Sie die Leistungsauswirkung bei der Verwendung oder Erweiterung der Nutzung dauerhafter Registrierungen.</span><span class="sxs-lookup"><span data-stu-id="1490a-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1490a-121">Diese Methode ist nur für Unicode implementiert.</span><span class="sxs-lookup"><span data-stu-id="1490a-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="1490a-122">Außerdem kann es zu einem vorbeugenden Fehler führen, wenn einer der Pfade im Array keine Dateinamenerweiterung von dll aufweist.</span><span class="sxs-lookup"><span data-stu-id="1490a-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1490a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1490a-123">See also</span></span>

- [<span data-ttu-id="1490a-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1490a-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="1490a-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1490a-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

