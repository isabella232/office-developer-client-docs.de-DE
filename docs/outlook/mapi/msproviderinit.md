---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d9a31a768ca588971fa0e22c1ab8c4d659753d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595651"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert einen Nachrichtenspeicheranbieter für den Vorgang.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
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

 _Hinstance_
  
> [in] Die Instanz der DLL (Dynamic Link Library) des Nachrichtenspeicheranbieters, die die MAPI beim Verknüpfen verwendet hat. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle** verfügbar machen kann. Der Nachrichtenspeicheranbieter muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream** arbeitet. 
    
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
  
> [in] Versionsnummer der VON MAPI verwendeten Dienstanbieterschnittstelle (Service Provider Interface, SPI). Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Zeiger auf die Versionsnummer der SPI, die von diesem Nachrichtenspeicheranbieter verwendet wird. 
    
 _lppMSProvider_
  
> [out] Zeiger auf einen Zeiger auf das initialisierte Nachrichtenspeicheranbieterobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_VERSION 
  
> Die von der MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die Einstiegspunktfunktion **MSProviderInit** auf, um einen Nachrichtenspeicheranbieter nach einer Clientanmeldung zu initialisieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Nachrichtenspeicheranbieter muss **MSProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren. Die Implementierung muss auf dem **MSPROVIDERINIT-Funktionsprototyp** basieren, der auch in MAPISPI.H angegeben ist. MAPI definiert **MSPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **MSProviderInit** der CDECL-Aufrufkonvention folgt. Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufbaren Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt. 
  
Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig oder mehrmals im selben Profil angezeigt wird. Da das Anbieterobjekt Kontext enthält, muss **MSProviderInit** ein anderes Anbieterobjekt in  _lppMSProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im selben Prozess. 
  
Die Anbieter-DLL sollte nicht mit Mapix.dll verknüpft werden. Stattdessen sollten diese Zeiger für die Speicherzuweisung oder -zuordnung verwendet werden. 
  
Der Nachrichtenspeicheranbieter sollte die Funktionen verwenden, auf die  _lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und -zuordnungen verweisen. Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)zuzuweisen. Wenn der Anbieter auch erwartet, dass die OLE-Speicherzuweisung verwendet wird, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das durch den  _lpMalloc-Parameter_ verwiesen wird. 
  
Weitere Informationen zum Schreiben von **MSProviderInit** finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md). Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion.](implementing-a-service-provider-entry-point-function.md) 
  
## <a name="see-also"></a>Siehe auch



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

