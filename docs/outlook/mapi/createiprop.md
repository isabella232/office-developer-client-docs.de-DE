---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406808"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Property-Datenobjekt, also ein [IPropData](ipropdataimapiprop.md) -Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf einen Schnittstellenbezeichner (IID) für das Eigenschaftendaten Objekt. Der gültige Schnittstellenbezeichner ist IID_IMAPIPropData. Das übergeben von NULL im _lpInterface_ -Parameter bewirkt außerdem, dass das im _lppPropData_ -Parameter zurückgegebene Property-Datenobjekt in die Standardschnittstelle für ein Datenobjekt der Eigenschaft umgewandelt wird. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppPropData_
  
> Out Zeiger auf einen Zeiger auf das zurückgegebene Eigenschaftendaten Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Die _lpAllocateBuffer_-, _LpAllocateMore_-und _lpFreeBuffer_ -Eingabeparameter zeigen auf die [MAPIAllocateBuffer](mapiallocatebuffer.md)-, [MAPIAllocateMore](mapiallocatemore.md)-und [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktionen. Eine Clientanwendung, die **CreateIProp** aufruft, übergibt Zeiger auf die soeben benannten MAPI-Funktionen. ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er bei seinem Initialisierungsaufruf erhalten hat, oder wird mit einem Aufruf der [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen. 
  

