---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792771"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="eaff3-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="eaff3-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="eaff3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eaff3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eaff3-105">Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="eaff3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaff3-106">Parameters</span></span>

 <span data-ttu-id="eaff3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="eaff3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="eaff3-108">[in] Ein Zeiger auf ein Array von Eigenschaftentags, die angeben, die Eigenschaften hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eaff3-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="eaff3-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="eaff3-109">_lppProblems_</span></span>
  
> <span data-ttu-id="eaff3-110">[in, out] Klicken Sie auf Eingaben, einen gültigen Zeiger auf eine Struktur [SPropProblemArray](spropproblemarray.md) oder NULL.</span><span class="sxs-lookup"><span data-stu-id="eaff3-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="eaff3-111">Klicken Sie auf Ausgabe, einen Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnte, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="eaff3-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="eaff3-112">Nur, wenn ein gültiger Zeiger übergeben wird, wird ein Zeiger auf eine Eigenschaft Problem Array-Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eaff3-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eaff3-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="eaff3-113">Return value</span></span>

<span data-ttu-id="eaff3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="eaff3-114">S_OK</span></span> 
  
> <span data-ttu-id="eaff3-115">Die Eigenschaften wurden erfolgreich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="eaff3-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="eaff3-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="eaff3-117">Geben Sie eine Eigenschaft außer PT_OBJECT im Array übergeben wurde, die auf der _LpPropTagArray_ -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="eaff3-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="eaff3-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="eaff3-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="eaff3-119">Das Objekt wurde nicht für Lese-/Schreibberechtigung zulassen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="eaff3-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="eaff3-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="eaff3-121">Einige, jedoch nicht alle Eigenschaften wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaff3-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eaff3-122">Remarks</span></span>

<span data-ttu-id="eaff3-123">Die **IPropData::HrAddObjProps** -Methode fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="eaff3-124">**HrAddObjProps** stellt eine Alternative zur die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode für Objekteigenschaften, da Objekteigenschaften durch Aufrufen von **SetProps**nicht erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="eaff3-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="eaff3-125">Hinzufügen einer Object-Eigenschaft führt das Eigenschafts-Tag eingeschlossen werden, in der Liste der Eigenschaftentags, die die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eaff3-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eaff3-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eaff3-126">Notes to callers</span></span>

<span data-ttu-id="eaff3-127">Wenn **HrAddObjProps** MAPI_W_PARTIAL_COMPLETION zurückgegeben, und Sie _LppProblems_ auf einen gültigen Zeiger festgelegt haben, überprüfen Sie die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur, um zu ermitteln, welche Eigenschaften nicht hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="eaff3-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="eaff3-128">In der Regel ist das einzige Problem, dass nicht genügend Speicherplatz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eaff3-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="eaff3-129">Freigeben der Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, wenn Sie mit ihm fertig sind.</span><span class="sxs-lookup"><span data-stu-id="eaff3-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="eaff3-130">Zum Hinzufügen einer Eigenschaft muss das Zielobjekt Lese-/Schreibberechtigung haben.</span><span class="sxs-lookup"><span data-stu-id="eaff3-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="eaff3-131">Wenn **HrAddObjProps** MAPI_E_NO_ACCESS zurückgibt, können nicht Sie Eigenschaften für das Objekt hinzufügen, da diese Änderung nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="eaff3-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="eaff3-132">Lese-/Schreibberechtigung für ein Objekt vor dem Aufrufen von **HrAddObjProps**zu erhalten, rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , und legen Sie den Parameter _UlAccess_ auf IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="eaff3-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eaff3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaff3-133">See also</span></span>



[<span data-ttu-id="eaff3-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eaff3-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eaff3-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="eaff3-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="eaff3-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="eaff3-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="eaff3-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eaff3-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
