---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06832b3ae760983474fd3553324fee304bd9ac37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595931"
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::TransportLogoff-Methode** auf, um eine Transportanbietersitzung für einen bestimmten Benutzer zu beenden. Vor dem Aufrufen von **TransportLogoff** verwirft der MAPI-Spooler alle Daten zu unterstützten Messaging-Adresstypen für diese Sitzung, die an die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) übergeben werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Transportanbieter sollte jederzeit bereit sein, einen Aufruf von **TransportLogoff** zu akzeptieren. Wenn eine Nachricht bearbeitet wird, sollte der Anbieter den Sendevorgang beenden. 
  
Der Transportanbieter sollte alle Ressourcen freigeben, die für die aktuelle Sitzung zugeordnet sind. Wenn sie mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) Speicher für diese Sitzung zugewiesen hat, sollte der Speicher mithilfe der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) freigegeben werden. Jeder vom Transportanbieter zur Erfüllung von Aufrufen der [IXPLogon::AddressTypes-Methode zugewiesene](ixplogon-addresstypes.md) Speicher kann zu diesem Zeitpunkt sicher freigegeben werden. 
  
In der Regel sollte ein Anbieter nach Abschluss eines **TransportLogoff-Aufrufs** zunächst sein Anmeldeobjekt ungültig machen, indem er die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufruft und dann sein Supportobjekt freigibt. Die **TransportLogoff-Implementierung** des Anbieters sollte das Supportobjekt zuletzt freigeben, da beim Freigeben des Supportobjekts der MAPI-Spooler auch das Anbieterobjekt selbst freigeben kann. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

