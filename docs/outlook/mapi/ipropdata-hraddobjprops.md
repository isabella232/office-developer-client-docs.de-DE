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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315533"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="d26df-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="d26df-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="d26df-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d26df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d26df-105">Fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu.</span><span class="sxs-lookup"><span data-stu-id="d26df-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="d26df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d26df-106">Parameters</span></span>

 <span data-ttu-id="d26df-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d26df-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d26df-108">in Ein Zeiger auf ein Array von Property-Tags, die die hinzuzufügenden Eigenschaften Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d26df-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="d26df-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="d26df-109">_lppProblems_</span></span>
  
> <span data-ttu-id="d26df-110">[in, out] Bei der Eingabe ein gültiger Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur oder NULL.</span><span class="sxs-lookup"><span data-stu-id="d26df-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="d26df-111">Bei der Ausgabe ein Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnten, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="d26df-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="d26df-112">Ein Zeiger auf eine Eigenschaften Problem-Array Struktur wird nur zurückgegeben, wenn ein gültiger Zeiger übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d26df-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d26df-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d26df-113">Return value</span></span>

<span data-ttu-id="d26df-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d26df-114">S_OK</span></span> 
  
> <span data-ttu-id="d26df-115">Die Eigenschaften wurden erfolgreich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d26df-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="d26df-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="d26df-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="d26df-117">Ein anderer Eigenschaftentyp als PT_OBJECT wurde in dem Array übergeben, auf das der _lpPropTagArray_ -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="d26df-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="d26df-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d26df-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d26df-119">Das Objekt wurde so festgelegt, dass die Berechtigung Lese-/Schreibzugriff nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d26df-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="d26df-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="d26df-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="d26df-121">Einige, aber nicht alle Eigenschaften wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d26df-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d26df-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d26df-122">Remarks</span></span>

<span data-ttu-id="d26df-123">Die **IPropData:: HrAddObjProps** -Methode fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu.</span><span class="sxs-lookup"><span data-stu-id="d26df-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="d26df-124">**HrAddObjProps** bietet eine Alternative zur [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode für Objekteigenschaften, da Objekteigenschaften nicht durch Aufrufen von \*\*\*\* SetProps erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="d26df-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="d26df-125">Wenn Sie eine Objekteigenschaft hinzufügen, wird das Property-Tag in die Liste der Eigenschaftstags aufgenommen, die von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d26df-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d26df-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d26df-126">Notes to callers</span></span>

<span data-ttu-id="d26df-127">Wenn **HRADDOBJPROPS** MAPI_W_PARTIAL_COMPLETION zurückgibt und Sie _lppProblems_ auf einen gültigen Zeiger festgelegt haben, überprüfen Sie die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur, um herauszufinden, welche Eigenschaften nicht hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="d26df-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="d26df-128">NormalerWeise ist das einzige Problem, das auftritt, mangelnder Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d26df-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="d26df-129">Geben Sie die **SPropProblemArray** -Struktur frei, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="d26df-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="d26df-130">Zum Hinzufügen einer Eigenschaft muss das Zielobjekt Lese-/Schreibzugriff besitzen.</span><span class="sxs-lookup"><span data-stu-id="d26df-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="d26df-131">Wenn **HRADDOBJPROPS** MAPI_E_NO_ACCESS zurückgibt, können Sie dem Objekt keine Eigenschaften hinzufügen, da es keine Änderung zulässt.</span><span class="sxs-lookup"><span data-stu-id="d26df-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="d26df-132">Wenn Sie vor dem Aufrufen von **HrAddObjProps**Lese-/Schreibzugriff auf ein Objekt erhalten möchten, rufen Sie [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, und legen Sie den Parameter _ulAccess_ auf IPROP_READWRITE fest.</span><span class="sxs-lookup"><span data-stu-id="d26df-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d26df-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d26df-133">See also</span></span>



[<span data-ttu-id="d26df-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d26df-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d26df-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d26df-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="d26df-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d26df-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d26df-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d26df-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

