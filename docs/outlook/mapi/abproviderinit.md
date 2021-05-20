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

 _hInstance_
  
> [in] Die Instanz der Dynamic-Link Library (DLL) des Adressbuchanbieters, die MAPI beim Verknüpfen verwendet hat. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll. Der Adressbuchanbieter muss diese Zuweisungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.** 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die bei Bedarf von MAPI zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die bei Bedarf von MAPI zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die verwendet werden soll, wenn mapi zum Freispeichern des Arbeitsspeichers erforderlich ist. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags. Das folgende Flag kann festgelegt werden:
    
MAPI_NT_SERVICE 
  
> Der Anbieter wird im Kontext eines Windows geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche. 
    
 _ulMAPIVer_
  
> [in] Versionsnummer der Dienstanbieterschnittstelle (SPI), die MAPI.DLL wird. Die aktuelle Versionsnummer finden Sie im MAPISPI. H-Headerdatei. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer des SPI, den dieser Adressbuchanbieter verwendet. 
    
 _lppABProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Adressbuchanbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die Einstiegspunktfunktion **ABProviderInit** auf, um einen Adressbuchanbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Adressbuchanbieter muss **ABProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **AbPROVIDERINIT-Funktionsprototyp** basieren, der auch in MAPISPI.H angegeben ist. MAPI definiert **ABPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **ABProviderInit** der CDECL-Aufrufkonvention folgt. 
  
Ein Anbieter kann mehrmals initialisiert werden, da er in mehreren Profilen gleichzeitig angezeigt wird oder mehr als einmal im gleichen Profil angezeigt wird. Da das provider-Objekt Kontext enthält, muss **ABProviderInit** ein anderes Anbieterobjekt in  _lppABProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im gleichen Prozess. 
  
Der Adressbuchanbieter sollte die Funktionen verwenden, auf die  _von lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation. Insbesondere muss der Anbieter diese Funktionen verwenden, um Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows zu reservieren.](imapitable-queryrows.md) Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das der  _lpMalloc-Parameter_ verweist. 
  
Weitere Informationen zum Schreiben von **ABProviderInit** finden Sie unter [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Siehe auch

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

