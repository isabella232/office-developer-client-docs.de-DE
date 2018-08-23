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
ms.openlocfilehash: 33adef7a8248e137869912afc2026583828b087e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570170"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Initialisiert eine Nachricht Speicheranbieter Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
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
  
> [in] Die Instanz der Nachricht Speichern des Anbieters Dynamic Link Library (DLL), die MAPI verwendet wird, wenn es verknüpft. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Nachricht Speicheranbieter müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _ulFlags_
  
> [in] Bitmaske der Kennzeichen. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows-Diensts, eine spezielle Art von Vorgang ohne Zugriff auf eine beliebige Benutzeroberfläche geladen. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), die MAPI verwendet. Die aktuelle Versionsnummer finden Sie unter der Headerdatei Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer der SPI, die diese Nachricht Speicher-Anbieter verwendet wird. 
    
 _lppMSProvider_
  
> [out] Zeiger auf einen Zeiger auf den initialisierten Message Store Provider-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-aufrufen, die Eintrags-Funktion **MSProviderInit** einen Anbieter für anmelden nach einer Clientanmeldung nicht initialisiert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine Nachricht Speicheranbieter muss als Funktion Entry Point in die DLL des Anbieters **MSProviderInit** implementieren. Die Implementierung der **MSPROVIDERINIT** Funktionsprototyp auch im angegebenen MAPISPI basieren. H. MAPI definiert **MSPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **MSProviderInit** CDECL-Aufrufkonvention folgen. Ein Vorteil CDECL ist, dass Anrufe versucht werden können, selbst wenn die Anzahl der aufrufenden Parameter nicht die Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrere Male, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden initialisiert werden. Da das Anbieterobjekt Kontext enthält, muss **MSProviderInit** in _LppMSProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben. 
  
Der Provider-DLL sollte nicht mit Mapix.dll verknüpft werden. In diesem Fall sollte diese Zeiger für oder Aufheben der arbeitsspeicherreservierung verwendet werden. 
  
Der Nachricht Speicheranbieter sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden. Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden. Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen. 
  
Weitere Informationen über das Schreiben von **MSProviderInit**finden Sie unter [Message-Anbieter laden](loading-message-store-providers.md). Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

