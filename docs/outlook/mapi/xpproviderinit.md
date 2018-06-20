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
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795868"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Betrifft**: Outlook 
  
Initialisiert eine Adressbuchhierarchie für Vorgang.
  
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
  
> [in] Die Instanz der Adressbuchhierarchie Dynamic Link Library (DLL), MAPI verwendet, wenn sie die DLL-Datei geladen.
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Transportdienst müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden. 
    
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
  
> [in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), die die Datei MAPI verwendet. Die aktuelle Versionsnummer finden Sie unter der Headerdatei Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer der SPI, die dieser Transportdienst verwendet. 
    
 _lppXPProvider_
  
> [out] Zeiger auf einen Zeiger auf den initialisierten Transportobjekt Anbieter.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>Hinweise

MAPI-aufrufen, die Eintrags-Funktion **XPProviderInit** ein Transportdienstes nach einer Clientanmeldung nicht initialisiert werden. **XPProviderInit** wird einmal für jede Adressbuchhierarchie im Profil des Clients angegebene aufgerufen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Transportdienstes muss als Funktion Entry Point in die DLL des Anbieters **XPProviderInit** implementieren. Die Implementierung der **XPPROVIDERINIT** Funktionsprototyp auch im angegebenen Mapispi.h basieren. MAPI definiert **XPPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **XPProviderInit** CDECL-Aufrufkonvention folgen. Ein Vorteil CDECL ist, dass Anrufe versucht werden können, selbst wenn die Anzahl der aufrufenden Parameter nicht die Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrmals initialisiert werden, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden. Da das Anbieterobjekt Kontext enthält, muss **XPProviderInit** in _LppXPProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben. 
  
Der Transportdienst sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden. Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden. Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen. 
  
Weitere Informationen über das Schreiben von **XPProviderInit**finden Sie unter [der Adressbuchhierarchie initialisieren](initializing-the-transport-provider.md). Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IXPProvider: IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

