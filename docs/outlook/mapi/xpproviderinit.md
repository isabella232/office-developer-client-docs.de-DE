---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325655"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Transportanbieter für den Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Implementiert von:  <br/> |Transport Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Parameter

 _hInstance_
  
> in Die Instanz der Dynamic Link Library (DLL) des Transportanbieters, die MAPI beim Laden der DLL verwendet hat.
    
 _lpMalloc_
  
> in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Transportanbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _ulFlags_
  
> in Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows-Diensts, einem speziellen Prozesstyp ohne Zugriff auf eine beliebige Benutzeroberfläche, geladen. 
    
 _ulMAPIVer_
  
> in Versionsnummer der Dienstanbieterschnittstelle (SPI), die von MAPI. dll verwendet wird. Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi. h. 
    
 _lpulProviderVer_
  
> Out Zeiger auf die Versionsnummer des SPI, die dieser Transportanbieter verwendet. 
    
 _lppXPProvider_
  
> Out Zeiger auf einen Zeiger auf das initialisierte Transportanbieter Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die Einstiegspunktfunktion **XPProviderInit** auf, um einen Transportanbieter nach einer Clientanmeldung zu initialisieren. **XPProviderInit** wird einmal für jeden Transportanbieter aufgerufen, der im Profil des Clients angegeben ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Transportanbieter muss **XPProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **XPPROVIDERINIT** -Funktionsprototyp basieren, der auch in Mapispi. h angegeben ist. MAPI definiert **XPPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **XPPROVIDERINIT** der Cdecl-Aufrufkonvention folgt. Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der Anruf Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das Provider-Objekt den Kontext enthält, muss **XPProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppXPProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Der Transportanbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen verwenden. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden. Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird. 
  
Weitere Informationen zum Schreiben von **XPProviderInit**finden Sie unter [Initialisieren des Transport Anbieters](initializing-the-transport-provider.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

