---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439289"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="b9276-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="b9276-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="b9276-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9276-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9276-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b9276-105">Deprecated.</span></span> <span data-ttu-id="b9276-106">Gibt die Adresstypen zurück, die von allen Transportanbietern in der Sitzung verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b9276-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="b9276-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9276-107">Parameters</span></span>

 <span data-ttu-id="b9276-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9276-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b9276-109">[in] Eine Bitmaske mit Flags, die das Format für die zurückgegebenen Adresstypen angibt.</span><span class="sxs-lookup"><span data-stu-id="b9276-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="b9276-110">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b9276-110">The following flag can be set:</span></span>
    
<span data-ttu-id="b9276-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9276-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b9276-112">Die Adresstypen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b9276-112">The address types are in Unicode format.</span></span> <span data-ttu-id="b9276-113">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Adresstypen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b9276-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="b9276-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="b9276-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="b9276-115">[out] Ein Zeiger auf eine Anzahl von Adresstypen, auf die der _lpppszAdrTypes-Parameter verweist._</span><span class="sxs-lookup"><span data-stu-id="b9276-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="b9276-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="b9276-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="b9276-117">[out] Ein Zeiger auf ein Array von Zeigern auf Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="b9276-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9276-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9276-118">Return value</span></span>

<span data-ttu-id="b9276-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9276-119">S_OK</span></span> 
  
> <span data-ttu-id="b9276-120">Die Adresstypen wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b9276-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9276-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9276-121">Remarks</span></span>

<span data-ttu-id="b9276-122">Die **IMAPISession::EnumAdrTypes-Methode** gibt eine Liste der Adresstypen zurück, die von allen aktiven Transportanbietern in der Sitzung verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b9276-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="b9276-123">Die Adresstypen für Transportanbieter, die derzeit nicht geladen sind, sind nicht in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9276-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="b9276-124">Transportanbieter registrieren sich, um einen oder mehrere Adresstypen zu behandeln, wenn MAPI ihre [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="b9276-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b9276-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b9276-125">Notes to callers</span></span>

<span data-ttu-id="b9276-126">Rufen [Sie MAPIFreeBuffer auf,](mapifreebuffer.md) um das Zeichenfolgenarray frei zu lassen, auf das der  _lpppszAdrTypes-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="b9276-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9276-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9276-127">See also</span></span>



[<span data-ttu-id="b9276-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="b9276-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="b9276-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b9276-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b9276-130">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9276-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

