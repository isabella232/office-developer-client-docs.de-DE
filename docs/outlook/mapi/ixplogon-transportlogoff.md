---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417861"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert den Abmeldevorgang. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben. Wenn etwas anderes als S_OK zurückgegeben wird, wird der Anbieter abgemeldet.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::TransportLogoff-Methode auf,** um eine Transportanbietersitzung für einen bestimmten Benutzer zu beenden. Vor dem **Aufrufen von TransportLogoff** verwirft der MAPI-Spooler alle Daten zu unterstützten Messagingadressentypen für diese Sitzung, die in der [IXPLogon::AddressTypes-Methode übergeben](ixplogon-addresstypes.md) werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Transportanbieter sollte jederzeit bereit sein, einen Anruf bei **TransportLogoff** zu akzeptieren. Wenn eine Nachricht im Prozess ist, sollte der Anbieter den Sendevorgang beenden. 
  
Der Transportanbieter sollte alle ressourcen frei geben, die für die aktuelle Sitzung zugewiesen sind. Wenn der Speicher für diese Sitzung mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugewiesen wurde, sollte der Arbeitsspeicher mithilfe der [MAPIFreeBuffer-Funktion frei](mapifreebuffer.md) werden. Der vom Transportanbieter zur Erfüllung von Aufrufen der [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) zugewiesene Arbeitsspeicher kann derzeit sicher freigegeben werden. 
  
Normalerweise sollte ein Anbieter nach Abschluss eines **TransportLogoff-Aufrufs** zunächst sein Anmeldeobjekt ungültig machen, indem er die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufruft und dann sein Supportobjekt los gibt. Die Implementierung von **TransportLogoff** durch den Anbieter sollte das Supportobjekt zuletzt losgelassen werden, da der MAPI-Spooler bei der Freigabe des Supportobjekts auch das Anbieterobjekt selbst losgelassen werden kann. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

