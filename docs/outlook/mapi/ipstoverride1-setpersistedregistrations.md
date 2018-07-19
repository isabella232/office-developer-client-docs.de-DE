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
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792810"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="77763-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="77763-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="77763-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77763-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77763-105">Registriert persönlichen Ordner (PST)-Dateien für die automatische Entsperren Weitere Anrufe an die HrTrustedPSTOverrideHandlerCallback zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="77763-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="77763-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77763-106">Parameters</span></span>

<span data-ttu-id="77763-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="77763-107">_pmval_</span></span>
  
> <span data-ttu-id="77763-108">[in] Eine [SPropValue](spropvalue.md) -Struktur, die einen Zeiger auf den Pfad zu der Dynamic Link Library (DLL enthält) registriert.</span><span class="sxs-lookup"><span data-stu-id="77763-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="77763-109">Die Struktur weist folgende Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="77763-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="77763-110">Ein UlPropTag des [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="77763-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="77763-111">Eine MVszW Value-Eigenschaft, die auf ein Array von Zeichenfolgen mit Null terminierte Unicode-Zeichen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="77763-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="77763-112">Weitere Informationen finden Sie unter dem Thema [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="77763-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="77763-113">Die SPropValue wird in einem MAPI-Eigenschaft im internen Bereich der PST-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="77763-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="77763-114">Diese Eigenschaft ist nicht möglich, für normale MAPI-Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="77763-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="77763-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77763-115">Return value</span></span>

<span data-ttu-id="77763-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="77763-116">S_OK</span></span> 
  
> <span data-ttu-id="77763-117">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="77763-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77763-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77763-118">Remarks</span></span>

<span data-ttu-id="77763-119">Beibehaltene Registrierungen können die Leistung der Anwendung, wie Outlook und Windows-Desktopsuche beeinträchtigen, die PST-Dateien öffnen.</span><span class="sxs-lookup"><span data-stu-id="77763-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="77763-120">Berücksichtigen Sie die Auswirkung auf die Leistung bei der Verwendung oder die Verwendung der permanenten Registrierungen erweitern.</span><span class="sxs-lookup"><span data-stu-id="77763-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="77763-121">Diese Methode ist nur für Unicode implementiert.</span><span class="sxs-lookup"><span data-stu-id="77763-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="77763-122">Darüber hinaus wird es präventiv fehl, wenn Pfade, die im Array Erweiterung DLL nicht verfügen.</span><span class="sxs-lookup"><span data-stu-id="77763-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77763-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77763-123">See also</span></span>

- [<span data-ttu-id="77763-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77763-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="77763-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77763-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

