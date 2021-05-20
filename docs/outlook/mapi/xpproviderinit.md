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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428536"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Transportanbieter für den Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Implementiert von:  <br/> |Transportanbieter  <br/> |
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
  
> [in] Die Instanz der Dll (Dynamic Link Library) des Transportanbieters, die MAPI beim Laden der DLL verwendet hat.
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll. Der Transportanbieter muss diese Zuweisungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.** 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der Dienstanbieterschnittstelle (SPI), die Mapi.dll wird. Die aktuelle Versionsnummer finden Sie in der Mapispi.h-Headerdatei. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer des SPI, den dieser Transportanbieter verwendet. 
    
 _lppXPProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Transportanbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die Einstiegspunktfunktion **XPProviderInit** auf, um einen Transportanbieter nach einer Clientanmeldung zu initialisieren. **XPProviderInit** wird einmal für jeden Transportanbieter aufgerufen, der im Clientprofil angegeben ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Transportanbieter muss **XPProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **XPPROVIDERINIT-Funktionsprototyp** basieren, der auch in Mapispi.h angegeben ist. MAPI definiert **XPPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **XPProviderInit** der CDECL-Aufrufkonvention folgt. Ein Vorteil von CDECL ist, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufenden Parameter nicht mit der Anzahl der definierten Parameter übereinstimmen. 
  
Ein Anbieter kann mehrmals initialisiert werden, da er in mehreren Profilen gleichzeitig angezeigt wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das provider-Objekt Kontext enthält, muss **XPProviderInit** ein anderes Anbieterobjekt in  _lppXPProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im gleichen Prozess. 
  
Der Transportanbieter sollte die Funktionen verwenden, auf die  _lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Deallocation verwiesen. Insbesondere muss der Anbieter diese Funktionen verwenden, um Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows zu reservieren.](imapitable-queryrows.md) Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das der  _lpMalloc-Parameter_ verweist. 
  
Weitere Informationen zum Schreiben von **XPProviderInit** finden Sie unter [Initializing the Transport Provider](initializing-the-transport-provider.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

