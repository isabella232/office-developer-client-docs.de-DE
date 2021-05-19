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
  
> Reserviert; muss null sein.
    
 _lpObject_
  
> [in] Ein Zeiger auf das zu ungültige Objekt. Die Schnittstelle des Objekts muss von **IUnknown abgeleitet werden.**
    
 _ulRefCount_
  
> [in] Die aktuelle Referenzanzahl des Objekts.
    
 _cMethods_
  
> [in] Die Anzahl der Methoden in der vtable des Objekts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich als nicht verwendbar gekennzeichnet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::MakeInvalid-Methode** wird für alle Supportobjekte implementiert. Das zu ungültige Objekt muss von der **IUnknown-Schnittstelle** oder von einer von **IUnknown** abgeleiteten Schnittstelle abgeleitet werden.
  
 **MakeInvalid** markiert ein Objekt als nicht verwendbar, indem die vtable des Objekts durch eine Stub-Vtable ähnlicher Größe ersetzt wird, bei der die **Methoden IUnknown::AddRef** und **IUnknown::Release** wie erwartet auftreten. Bei allen anderen Methoden ist jedoch ein Fehler zu begehen, und der Wert wird MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Dienstanbieter und Nachrichtendienste rufen **MakeInvalid** normalerweise zum Zeitpunkt des Herunterfahrens auf. **MakeInvalid** kann jedoch jederzeit aufgerufen werden. Wenn ein Client beispielsweise ein Objekt freilässt, ohne einige seiner Unterobjekte frei zu geben, können Sie **MakeInvalid** sofort aufrufen, um diese Unterobjekte frei zu geben. 
  
Sie müssen das Objekt besitzen, das Sie ungültig zu machen versuchen. Er muss mindestens 16 Byte lang sein und mindestens drei Methoden in seiner vtable enthalten. 
  
Sie können **MakeInvalid** aufrufen und dann alle herunterfahrenden Aufgaben ausführen, z. B. das Verwerfen zugeordneter Datenstrukturen, die in der Regel während der Veröffentlichung eines Objekts durchgeführt werden. Code zur Unterstützung des Objekts muss nicht im Arbeitsspeicher gespeichert werden, da MAPI den Arbeitsspeicher durch aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) und dann das Objekt freilässt. Sie können Ressourcen frei geben, **MakeInvalid aufrufen** und dann das ungültige Objekt ignorieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

