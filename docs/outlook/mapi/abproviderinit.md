---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428284"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Adressbuchanbieter für den Vorgang. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Parameter

 _hInstance_
  
> in Die Instanz der Dynamic Link Library (DLL) des Adressbuch Anbieters, die MAPI bei der Verknüpfung verwendet hat. 
    
 _lpMalloc_
  
> in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Adressbuchanbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die verwendet werden soll, wenn MAPI zum Reservieren von Arbeitsspeicher erforderlich ist. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die bei Bedarf von MAPI verwendet werden kann, um zusätzlichen Arbeitsspeicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden soll, wenn MAPI zum Freigeben des Arbeitsspeichers erforderlich ist. 
    
 _ulFlags_
  
> in Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows-Diensts, einem speziellen Prozesstyp ohne Zugriff auf eine beliebige Benutzeroberfläche, geladen. 
    
 _ulMAPIVer_
  
> in Versionsnummer der Dienstanbieterschnittstelle (SPI), die MAPI. DLL verwendet. Die aktuelle Versionsnummer finden Sie unter MAPISPI. H-Headerdatei. 
    
 _lpulProviderVer_
  
> Out Zeiger auf die Versionsnummer des SPI, den dieser Adressbuchanbieter verwendet. 
    
 _lppABProvider_
  
> Out Zeiger auf einen Zeiger auf das Objekt des initialisierten Adressbuch Anbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die Einstiegspunktfunktion **ABProviderInit** auf, um einen Adressbuchanbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Adressbuchanbieter muss **ABProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem Prototyp der **ABPROVIDERINIT** -Funktion basieren, der auch in MAPISPI angegeben ist. H. MAPI definiert **ABPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **ABPROVIDERINIT** der Cdecl-Aufrufkonvention folgt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das Provider-Objekt den Kontext enthält, muss **ABProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppABProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Der Adressbuchanbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Zuordnungen verwenden. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden. Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird. 
  
Weitere Informationen zum Schreiben von **ABProviderInit**finden Sie unter [Implementieren der Einstiegspunktfunktion eines Adressbuch Anbieters](implementing-an-address-book-provider-entry-point-function.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

