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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425155"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="3dcb4-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="3dcb4-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="3dcb4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dcb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dcb4-105">Legt die Zugriffsebene f�r das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="3dcb4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dcb4-106">Parameters</span></span>

 <span data-ttu-id="3dcb4-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="3dcb4-107">_ulAccess_</span></span>
  
> <span data-ttu-id="3dcb4-p101">[in] Eine Bitmaske aus Flags, die Zugriffsebene des Objekts angibt. Eine der folgenden Werte kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3dcb4-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="3dcb4-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="3dcb4-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="3dcb4-111">Das Objekt Zugriffsebene festgelegt auf schreibgesch�tzt.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="3dcb4-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="3dcb4-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="3dcb4-113">Legt die Zugriffsebene f�r das Objekt den Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3dcb4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dcb4-114">Return value</span></span>

<span data-ttu-id="3dcb4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dcb4-115">S_OK</span></span> 
  
> <span data-ttu-id="3dcb4-116">Zugriffsebene f�r das Objekt wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dcb4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dcb4-117">Remarks</span></span>

<span data-ttu-id="3dcb4-p102">Die **IPropData::HrSetObjAccess** -Methode wird die Zugriffsebene f�r das gesamte Objekt, statt die Daten f�r die einzelnen Eigenschaften. So �ndern Sie die Zugriffsebene festgelegt, wenn das Objekt erstellt wurde, kann **HrSetObjAccess** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3dcb4-120">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3dcb4-120">Notes to callers</span></span>

<span data-ttu-id="3dcb4-p103">Um eine Zugriffsebene f�r eine Eigenschaft festzulegen, rufen Sie zuerst **HrSetObjAccess** mit dem IPROP_READWRITE-Flag, das im Parameter  _ulAccess_ auf das Objekt ge�ndert werden kann, festgelegt. Rufen Sie dann die [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) -Methode, die die Target-Eigenschaft im Array auf die durch den  _lpPropTagArray_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="3dcb4-123">Zum Erstellen eines Objekts mit Eigenschaften, die f�r Clients schreibgesch�tzt sein sollen, erstellen Sie ein Lese-Schreib-Objekt, f�gen Sie die erforderlichen Eigenschaften und rufen Sie dann **HrSetObjAccess**, um das Objekt Zugriff auf schreibgesch�tzte ge�ndert werden.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="3dcb4-124">Sie k�nnen auch **HrSetObjAccess** verwenden, um zu verhindern, dass Clients Erstellung neuer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3dcb4-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dcb4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dcb4-125">See also</span></span>



[<span data-ttu-id="3dcb4-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="3dcb4-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="3dcb4-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="3dcb4-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="3dcb4-128">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3dcb4-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

