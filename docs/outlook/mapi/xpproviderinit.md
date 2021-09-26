---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6935eb7aebf718065486e686184e98b84b156acc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583226"
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

 _Hinstance_
  
> [in] Die Instanz der DLL (Dynamic Link Library) des Transportanbieters, die die MAPI beim Laden der DLL verwendet hat.
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle** verfügbar machen kann. Der Transportanbieter muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream** arbeitet. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows Diensts geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der Dienstanbieterschnittstelle (SERVICE Provider Interface, SPI), die Mapi.dll verwendet. Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer der SPI, die von diesem Transportanbieter verwendet wird. 
    
 _lppXPProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Transportanbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von der MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die Einstiegspunktfunktion **XPProviderInit** auf, um einen Transportanbieter nach einer Clientanmeldung zu initialisieren. **XPProviderInit** wird einmal für jeden Transportanbieter aufgerufen, der im Clientprofil angegeben ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Transportanbieter muss **XPProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **XPPROVIDERINIT-Funktionsprototyp** basieren, der auch in Mapispi.h angegeben ist. MAPI definiert **XPPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **XPProviderInit** der CDECL-Aufrufkonvention folgt. Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufbaren Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig oder mehrmals im selben Profil angezeigt wird. Da das Anbieterobjekt Kontext enthält, muss **XPProviderInit** ein anderes Anbieterobjekt in  _lppXPProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Der Transportanbieter sollte die Funktionen verwenden, auf die  _lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Zuordnungen verweisen. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)zuzuweisen. Wenn der Anbieter auch erwartet, dass die OLE-Speicherzuweisung verwendet wird, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das durch den  _lpMalloc-Parameter_ verwiesen wird. 
  
Weitere Informationen zum Schreiben von **XPProviderInit** finden Sie unter [Initialisieren des Transportanbieters.](initializing-the-transport-provider.md) Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion.](implementing-a-service-provider-entry-point-function.md) 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

