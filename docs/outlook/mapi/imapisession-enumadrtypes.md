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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792302"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="17ae0-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="17ae0-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="17ae0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17ae0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17ae0-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="17ae0-105">Deprecated.</span></span> <span data-ttu-id="17ae0-106">Gibt die behandelt werden können Adresstypen aller Anbieter für den Transport in der Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="17ae0-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="17ae0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="17ae0-107">Parameters</span></span>

 <span data-ttu-id="17ae0-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17ae0-108">_ulFlags_</span></span>
  
> <span data-ttu-id="17ae0-109">[in] Eine Bitmaske aus Flags, die das Format für die zurückgegebene Adresstypen angibt.</span><span class="sxs-lookup"><span data-stu-id="17ae0-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="17ae0-110">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="17ae0-110">The following flag can be set:</span></span>
    
<span data-ttu-id="17ae0-111">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="17ae0-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="17ae0-112">Die Adresstypen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="17ae0-112">The address types are in Unicode format.</span></span> <span data-ttu-id="17ae0-113">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Adresstypen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="17ae0-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="17ae0-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="17ae0-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="17ae0-115">[out] Ein Zeiger auf eine Anzahl von-Adresstypen auf den durch den Parameter _LpppszAdrTypes_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="17ae0-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="17ae0-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="17ae0-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="17ae0-117">[out] Ein Zeiger auf ein Array von Zeigern für Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="17ae0-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17ae0-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="17ae0-118">Return value</span></span>

<span data-ttu-id="17ae0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="17ae0-119">S_OK</span></span> 
  
> <span data-ttu-id="17ae0-120">Die Adresstypen wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="17ae0-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17ae0-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17ae0-121">Remarks</span></span>

<span data-ttu-id="17ae0-122">Die **IMAPISession::EnumAdrTypes** -Methode gibt eine Liste der durch alle aktiven Transportanbieter behandelt werden kann Adresstypen in der Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="17ae0-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="17ae0-123">Die Adresstypen für Transportanbieter, die derzeit nicht geladen werden, sind nicht in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="17ae0-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="17ae0-124">Transportanbieter registrieren, um eine oder mehrere Adresstypen behandeln, wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="17ae0-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="17ae0-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="17ae0-125">Notes to callers</span></span>

<span data-ttu-id="17ae0-126">Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) , um auf das durch den Parameter _LpppszAdrTypes_ Zeichenfolgenarrays freizugeben.</span><span class="sxs-lookup"><span data-stu-id="17ae0-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17ae0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ae0-127">See also</span></span>



[<span data-ttu-id="17ae0-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="17ae0-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="17ae0-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="17ae0-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="17ae0-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="17ae0-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

