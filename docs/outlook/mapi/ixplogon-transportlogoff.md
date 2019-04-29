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
  
Initiiert den ABMELDEPROZESS. 
  
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
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben. Wenn etwas anderes als S_OK zurückgegeben wird, wird der Anbieter abgemeldet.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPLogon:: TransportLogoff** -Methode auf, um eine Transportanbieter Sitzung für einen bestimmten Benutzer zu beenden. Vor dem Aufrufen von **TransportLogoff**verwirft der MAPI-Spooler alle Daten über unterstützte Messaging Adresstypen für diese Sitzung, die in der [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode übergeben werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Transportanbieter sollte jederzeit bereit sein, einen Anruf an **TransportLogoff** zu akzeptieren. Wenn eine Nachricht in Arbeit ist, sollte der Anbieter den sendenden Prozess beenden. 
  
Der Transportanbieter sollte alle Ressourcen freigeben, die für seine aktuelle Sitzung reserviert sind. Wenn der Speicherplatz für diese Sitzung mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion reserviert wurde, sollte er den Arbeitsspeicher mithilfe der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion freigeben. Jeder vom Transportanbieter zugewiesene Arbeitsspeicher, der Aufrufe der [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode erfüllt, kann zu diesem Zeitpunkt sicher freigegeben werden. 
  
In der Regel muss ein Anbieter beim Abschließen eines **TransportLogoff** -Aufrufs zuerst sein Logo-Objekt ungültig machen, indem er die [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) -Methode aufruft und dann sein Support-Objekt freigibt. Die Implementierung von **TransportLogoff** durch den Anbieter sollte das Support Objekt zuletzt freigeben, da der MAPI-Spooler, wenn das Support Objekt veröffentlicht wird, auch das Provider-Objekt selbst freigeben kann. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

