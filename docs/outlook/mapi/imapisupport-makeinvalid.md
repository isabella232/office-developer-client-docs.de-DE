---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427493"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Markiert ein Objekt als unbrauchbar.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _lpObject_
  
> in Ein Zeiger auf das Objekt, das ungültig werden soll. Die Schnittstelle des Objekts muss von **IUnknown**abgeleitet werden.
    
 _ulRefCount_
  
> in Der aktuelle Verweiszähler des Objekts.
    
 _cMethods_
  
> in Die Anzahl der Methoden in der Vtable des Objekts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich als unbrauchbar gekennzeichnet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: MakeInvalid** -Methode wird für alle Support-Objekte implementiert. Das Objekt, das ungültig werden soll, muss von der **IUnknown** -Schnittstelle oder von einer von **IUnknown**abgeleiteten Schnittstelle abgeleitet werden.
  
 **MakeInvalid** markiert ein Objekt als unbrauchbar, indem die Vtable des Objekts durch eine Stub-Vtable mit ähnlicher Größe ersetzt wird, in der die Methoden **IUnknown:: AddRef** und **IUnknown:: Release** wie erwartet ausgeführt werden. Allerdings schlagen alle anderen Methoden fehl, wobei der Wert MAPI_E_INVALID_OBJECT zurückgegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Dienstanbieter und Nachrichtendienste rufen **MakeInvalid** in der Regel beim Herunterfahren auf. **MakeInvalid** kann jedoch jederzeit aufgerufen werden. Wenn ein Client beispielsweise ein Objekt freigibt, ohne einige seiner unter Objekte freizugeben, können Sie **MakeInvalid** sofort aufrufen, um diese unter Objekte freizugeben. 
  
Sie müssen das Objekt besitzen, das Sie ungültig machen möchten. Sie muss mindestens 16 Bytes lang sein und mindestens drei Methoden in ihrer vtable aufweisen. 
  
Sie können **MakeInvalid** aufrufen und dann alle Aufgaben zum Herunterfahren ausführen, wie das Verwerfen zugeordneter Datenstrukturen, die in der Regel während der Freigabe eines Objekts ausgeführt werden. Code zur Unterstützung des Objekts muss nicht im Arbeitsspeicher aufbewahrt werden, da MAPI den Arbeitsspeicher durch Aufrufen von [mapifreebufferfreigegeben](mapifreebuffer.md) freigibt und das Objekt dann frei gibt. Sie können Ressourcen freigeben, **MakeInvalid**aufrufen und dann das Invalidated-Objekt ignorieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

