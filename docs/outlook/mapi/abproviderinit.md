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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791236"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Betrifft**: Outlook 
  
Adressbuch-Dienstanbieter für Vorgang initialisiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Implementiert von:  <br/> |Von adressbuchanbietern implementierte  <br/> |
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
  
> [in] Die Instanz der Adressbuchanbieter Dynamic Link Library (DLL), die MAPI verwendet wird, wenn es verknüpft. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht. Der Adressbuchanbieter müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , gegebenenfalls MAPI Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die Funktion [MAPIAllocateMore](mapiallocatemore.md) , gegebenenfalls MAPI verwendet werden soll, zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, in denen MAPI erforderlich, um Arbeitsspeicher freizugeben. 
    
 _ulFlags_
  
> [in] Bitmaske der Kennzeichen. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows-Diensts, eine spezielle Art von Vorgang ohne Zugriff auf eine beliebige Benutzeroberfläche geladen. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), MAPI. DLL-Datei verwendet. Die aktuelle Versionsnummer finden Sie unter der MAPISPI. H-Headerdatei. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer der SPI, die diese Adressbuchanbieter verwendet. 
    
 _lppABProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierten Address Book Anbieter-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.
    
## <a name="remarks"></a>Hinweise

MAPI-aufrufen, die Eintrags-Funktion **ABProviderInit** nach einer Clientanmeldung Adressbuch-Dienstanbieter nicht initialisiert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuch-Dienstanbieter muss als Funktion Entry Point in die DLL des Anbieters **ABProviderInit** implementieren. Die Implementierung der **ABPROVIDERINIT** Funktionsprototyp auch im angegebenen MAPISPI basieren. H. MAPI definiert **ABPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **ABProviderInit** CDECL-Aufrufkonvention folgen. 
  
Ein Anbieter kann mehrere Male, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden initialisiert werden. Da das Anbieterobjekt Kontext enthält, muss **ABProviderInit** in _LppABProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben. 
  
Der Adressbuchanbieter sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden. Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden. Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen. 
  
Weitere Informationen zum Schreiben von **ABProviderInit**finden Sie unter [Implementieren einer Adresse Adressbuch Anbieter Eintrag Point-Funktion](implementing-an-address-book-provider-entry-point-function.md). Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch

- [IABProvider: IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

