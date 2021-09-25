---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 510230c63eef41816fef29634365d11d2ab2cc42
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584661"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Eigenschaftsdatenobjekt, d. h. ein [IPropData-Objekt.](ipropdataimapiprop.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Zeiger auf einen Schnittstellenbezeichner (INTERFACE Identifier, IID) für das Eigenschaftsdatenobjekt. Der gültige Schnittstellenbezeichner ist IID_IMAPIPropData. Wenn NULL im  _lpInterface-Parameter_ übergeben wird, wird auch das im  _Parameter "lppPropData"_ zurückgegebene Eigenschaftsdatenobjekt in die Standardschnittstelle für ein Eigenschaftsdatenobjekt umgewandelt. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppPropData_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Eigenschaftsdatenobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Eingabeparameter _lpAllocateBuffer,_ _lpAllocateMore_ und _lpFreeBuffer_ verweisen jeweils auf die Funktionen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md) Eine Clientanwendung, die **CreateIProp** aufruft, übergibt Zeiger an die mapi-Funktionen, die gerade benannt wurden. Ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er in seinem Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) abgerufen hat. 
  

