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
ms.openlocfilehash: 8d6eb011e65ad44f4183eb5821697dcf2508032c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566880"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Eigenschaft Datenobjekt, d. h., ein [IPropData](ipropdataimapiprop.md) -Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf eine Schnittstellenbezeichner (IID) für die Daten Property-Objekt. Der Bezeichner gültige Schnittstelle ist IID_IMAPIPropData. Übergeben NULL im _LpInterface_ -Parameter wird auch das Eigenschaftenobjekt-Daten, die in der _LppPropData_ -Parameter in der standard-Benutzeroberfläche für ein Property-Datenobjekt umgewandelt werden zurückgegeben. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpvReserved_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppPropData_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Daten Eigenschaftenobjekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Eingabeparametern _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ zeigen die [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) -Funktionen. Eine Clientanwendung Aufrufen **CreateIProp** übergibt Zeiger auf die MAPI-Funktionen, die nur mit dem Namen; Ein Dienstanbieter übergibt die Zeiger auf diese Funktionen, die es in seinem Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen. 
  

