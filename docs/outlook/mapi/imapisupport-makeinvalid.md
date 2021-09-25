---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0830efe7ef5b76f2f25aca86a7d737bdc0810a03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567431"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Markiert ein Objekt als nicht verwendbar.
  
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
  
> Reserviert; muss Null sein.
    
 _lpObject_
  
> [in] Ein Zeiger auf das Objekt, das ungültig werden soll. Die Schnittstelle des Objekts muss von **IUnknown** abgeleitet werden.
    
 _ulRefCount_
  
> [in] Die aktuelle Referenzanzahl des Objekts.
    
 _cMethods_
  
> [in] Die Anzahl der Methoden in der vtable des Objekts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich als nicht verwendbar markiert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::MakeInvalid-Methode** ist für alle Unterstützungsobjekte implementiert. Das ungültige Objekt muss von der **IUnknown-Schnittstelle** oder von einer von **IUnknown** abgeleiteten Schnittstelle abgeleitet werden.
  
 **MakeInvalid** markiert ein Objekt als unbrauchbar, indem die vtable des Objekts durch eine Stub-VTable ähnlicher Größe ersetzt wird, in der die Methoden **IUnknown::AddRef** und **IUnknown::Release** erwartungsgemäß funktionieren. Bei allen anderen Methoden tritt jedoch ein Fehler auf, und der Wert wird MAPI_E_INVALID_OBJECT zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Dienstanbieter und Nachrichtendienste rufen **MakeInvalid** in der Regel zum Zeitpunkt des Herunterfahrens auf. **MakeInvalid** kann jedoch jederzeit aufgerufen werden. Wenn ein Client beispielsweise ein Objekt loslässt, ohne einige seiner Unterobjekte freizugeben, können Sie **MakeInvalid** sofort aufrufen, um diese Unterobjekte freizugeben. 
  
Sie müssen das Objekt besitzen, das Sie ungültig machen möchten. Sie muss mindestens 16 Bytes lang sein und mindestens drei Methoden in der vtable aufweisen. 
  
Sie können **MakeInvalid** aufrufen und dann alle Vorgänge zum Herunterfahren ausführen, z. B. das Verwerfen zugeordneter Datenstrukturen, die normalerweise während der Freigabe eines Objekts durchgeführt werden. Code zur Unterstützung des Objekts muss nicht im Arbeitsspeicher gespeichert werden, da MAPI den Speicher durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) freigibt und dann das Objekt freigibt. Sie können Ressourcen freigeben, **MakeInvalid** aufrufen und dann das ungültige Objekt ignorieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

