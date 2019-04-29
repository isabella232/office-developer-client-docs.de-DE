---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416237"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Nachrichtenspeicher Anbieter für den Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Parameter

 _hInstance_
  
> in Die Instanz der Dynamic Link Library (DLL) des Nachrichtenspeicher Anbieters, die MAPI bei der Verknüpfung verwendet hat. 
    
 _lpMalloc_
  
> in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Nachrichtenspeicher Anbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden. 
    
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
  
> in Die Versionsnummer der Dienstanbieterschnittstelle, die von MAPI verwendet wird. Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi. h. 
    
 _lpulProviderVer_
  
> Out Zeiger auf die Versionsnummer des SPI, den dieser Nachrichtenspeicher Anbieter verwendet. 
    
 _lppMSProvider_
  
> Out Zeiger auf einen Zeiger auf das initialisierte Nachrichtenspeicher-Anbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die Einstiegspunktfunktion **MSProviderInit** auf, um einen Nachrichtenspeicher Anbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Nachrichtenspeicher Anbieter muss **MSProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem Prototyp der **MSPROVIDERINIT** -Funktion basieren, der auch in MAPISPI angegeben ist. H. MAPI definiert **MSPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **MSPROVIDERINIT** der Cdecl-Aufrufkonvention folgt. Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der Anruf Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das Provider-Objekt den Kontext enthält, muss **MSProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppMSProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Die Anbieter-DLL sollte nicht mit mapix. dll verknüpft werden. Stattdessen sollten Sie diese Zeiger für die Speicherbelegung oder-dereservierung verwenden. 
  
Der Nachrichtenspeicher Anbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen verwenden. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden. Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird. 
  
Weitere Informationen zum Schreiben von **MSProviderInit**finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

