---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792758"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="0352b-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="0352b-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="0352b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0352b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0352b-105">Legt die Zugriffsebene f�r das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="0352b-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="0352b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0352b-106">Parameters</span></span>

 <span data-ttu-id="0352b-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="0352b-107">_ulAccess_</span></span>
  
> <span data-ttu-id="0352b-p101">[in] Eine Bitmaske aus Flags, die Zugriffsebene des Objekts angibt. Eine der folgenden Werte kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0352b-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="0352b-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="0352b-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="0352b-111">Das Objekt Zugriffsebene festgelegt auf schreibgesch�tzt.</span><span class="sxs-lookup"><span data-stu-id="0352b-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="0352b-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="0352b-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="0352b-113">Legt die Zugriffsebene f�r das Objekt den Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0352b-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0352b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0352b-114">Return value</span></span>

<span data-ttu-id="0352b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0352b-115">S_OK</span></span> 
  
> <span data-ttu-id="0352b-116">Zugriffsebene f�r das Objekt wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0352b-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0352b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0352b-117">Remarks</span></span>

<span data-ttu-id="0352b-p102">Die **IPropData::HrSetObjAccess** -Methode wird die Zugriffsebene f�r das gesamte Objekt, statt die Daten f�r die einzelnen Eigenschaften. So �ndern Sie die Zugriffsebene festgelegt, wenn das Objekt erstellt wurde, kann **HrSetObjAccess** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0352b-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0352b-120">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0352b-120">Notes to callers</span></span>

<span data-ttu-id="0352b-p103">Um eine Zugriffsebene f�r eine Eigenschaft festzulegen, rufen Sie zuerst **HrSetObjAccess** mit dem IPROP_READWRITE-Flag, das im Parameter  _ulAccess_ auf das Objekt ge�ndert werden kann, festgelegt. Rufen Sie dann die [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) -Methode, die die Target-Eigenschaft im Array auf die durch den  _lpPropTagArray_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0352b-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="0352b-123">Zum Erstellen eines Objekts mit Eigenschaften, die f�r Clients schreibgesch�tzt sein sollen, erstellen Sie ein Lese-Schreib-Objekt, f�gen Sie die erforderlichen Eigenschaften und rufen Sie dann **HrSetObjAccess**, um das Objekt Zugriff auf schreibgesch�tzte ge�ndert werden.</span><span class="sxs-lookup"><span data-stu-id="0352b-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="0352b-124">Sie k�nnen auch **HrSetObjAccess** verwenden, um zu verhindern, dass Clients Erstellung neuer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0352b-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0352b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0352b-125">See also</span></span>



[<span data-ttu-id="0352b-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="0352b-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="0352b-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="0352b-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="0352b-128">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0352b-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

