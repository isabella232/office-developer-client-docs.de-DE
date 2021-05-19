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
  
Initialisiert einen Nachrichtenspeicheranbieter für den Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
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
  
> [in] Die Instanz der DYNAMIC-Link Library (DLL) des Nachrichtenspeicheranbieters, die MAPI beim Verknüpfen verwendet hat. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll. Der Nachrichtenspeicheranbieter muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.** 
    
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
  
> [in] Versionsnummer der von MAPI verwendeten Dienstanbieterschnittstelle (Service Provider Interface, SPI). Die aktuelle Versionsnummer finden Sie in der Mapispi.h-Headerdatei. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer des SPI, den dieser Nachrichtenspeicheranbieter verwendet. 
    
 _lppMSProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Objekt des Nachrichtenspeicheranbieters.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die Einstiegspunktfunktion **MSProviderInit** auf, um einen Nachrichtenspeicheranbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Nachrichtenspeicheranbieter muss **MSProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **MSPROVIDERINIT-Funktionsprototyp** basieren, der auch in MAPISPI.H angegeben ist. MAPI definiert **MSPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **MSProviderInit** der CDECL-Aufrufkonvention folgt. Ein Vorteil von CDECL ist, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufenden Parameter nicht mit der Anzahl der definierten Parameter übereinstimmen. 
  
Ein Anbieter kann mehrmals initialisiert werden, da er in mehreren Profilen gleichzeitig angezeigt wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das provider-Objekt Kontext enthält, muss **MSProviderInit** ein anderes Anbieterobjekt in  _lppMSProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im gleichen Prozess. 
  
Die Anbieter-DLL sollte nicht mit dem Mapix.dll. Stattdessen sollten diese Zeiger für die Speicherzuweisung oder -verteilung verwendet werden. 
  
Der Nachrichtenspeicheranbieter sollte die Funktionen verwenden, auf die  _von lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Deallocation verwiesen wird. Insbesondere muss der Anbieter diese Funktionen verwenden, um Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows zu reservieren.](imapitable-queryrows.md) Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das der  _lpMalloc-Parameter_ verweist. 
  
Weitere Informationen zum Schreiben von **MSProviderInit** finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

