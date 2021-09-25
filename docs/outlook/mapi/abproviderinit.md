---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea53639308f96c0b13641119e0e59dcc0a0359c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592725"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Adressbuchanbieter für den Vorgang. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
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

 _Hinstance_
  
> [in] Die Instanz der DLL (Dynamic Link Library) des Adressbuchanbieters, die die MAPI beim Verknüpfen verwendet hat. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle** verfügbar machen kann. Der Adressbuchanbieter muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream** arbeitet. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die verwendet werden soll, wenn die MAPI Arbeitsspeicher zuweist. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, wenn die MAPI zusätzlichen Speicher zuweist. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die verwendet werden soll, wenn die MAPI zum Freigeben von Arbeitsspeicher erforderlich ist. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows Diensts geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der Dienstanbieterschnittstelle (SERVICE Provider Interface, SPI), die MAPI.DLL verwendet. Die aktuelle Versionsnummer finden Sie unter MAPISPI. H-Headerdatei. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer des SPI, die von diesem Adressbuchanbieter verwendet wird. 
    
 _lppABProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Adressbuchanbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von der MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die Einstiegspunktfunktion **ABProviderInit** auf, um einen Adressbuchanbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Adressbuchanbieter muss **ABProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **ABPROVIDERINIT-Funktionsprototyp** basieren, der auch in MAPISPI.H angegeben ist. MAPI definiert **ABPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **ABProviderInit** der CDECL-Aufrufkonvention folgt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig oder mehrmals im selben Profil angezeigt wird. Da das Anbieterobjekt Kontext enthält, muss **ABProviderInit** ein anderes Anbieterobjekt in  _lppABProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Der Adressbuchanbieter sollte die Funktionen verwenden, auf die  _lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Zuordnungen verweisen. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)zuzuweisen. Wenn der Anbieter auch erwartet, dass die OLE-Speicherzuweisung verwendet wird, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das durch den  _lpMalloc-Parameter_ verwiesen wird. 
  
Weitere Informationen zum Schreiben von **ABProviderInit** finden Sie unter [Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion.](implementing-an-address-book-provider-entry-point-function.md) Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion.](implementing-a-service-provider-entry-point-function.md) 
  
## <a name="see-also"></a>Siehe auch

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

