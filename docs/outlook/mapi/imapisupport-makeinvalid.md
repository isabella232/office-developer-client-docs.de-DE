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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792374"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Betrifft**: Outlook 
  
Markiert ein Objekt als nicht mehr verwendet werden.
  
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
  
> Reserviert. NULL muss sein.
    
 _lpObject_
  
> [in] Ein Zeiger auf das Objekt, das ungültig gemacht werden. Die Schnittstelle des Objekts muss von **IUnknown**abgeleitet werden.
    
 _ulRefCount_
  
> [in] Das Objekt vorhanden Referenzzähler.
    
 _cMethods_
  
> [in] Die Anzahl der Methoden in der Vtable des Objekts.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt wurde erfolgreich als nicht verwendbar gekennzeichnet.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::MakeInvalid** -Methode wird für alle Unterstützungsobjekte implementiert. Das Objekt, das ungültig gemacht werden muss aus die **IUnknown** -Schnittstelle oder von einer Schnittstelle abgeleitet von **IUnknown**abgeleitet werden.
  
 **MakeInvalid** markiert ein Objekt als nicht verwendbar durch Ersetzen des Objekts Vtable durch eine Stub Vtable ähnlicher Größe, in dem die **IUnknown:: AddRef** und **IUnknown** -Methoden wie erwartet ausgeführt werden. Alle anderen Methoden Fehler jedoch auftreten, den Wert MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Dienstanbieter und Message-Dienste in der Regel Aufrufen **MakeInvalid** Zeitpunkt zum Herunterfahren von. **MakeInvalid** kann jedoch jederzeit aufgerufen werden. Wenn ein Client ein Objekt ohne Freigabe einiger seiner Unterobjekte veröffentlicht, können Sie beispielsweise **MakeInvalid** sofort, um diese Unterobjekte release aufrufen. 
  
Sie müssen das Objekt verfügen, das Sie versuchen, die als ungültig zu erklären. Es muss mindestens 16 Byte lang sein und mindestens drei Methoden in der Vtable haben. 
  
Rufen Sie **MakeInvalid** und klicken Sie dann führt alle Herunterfahren, z. B. durch verwerfen zugehörigen Datenstrukturen, die während der Freigabe eines Objekts in der Regel erfolgt. Code, um das Objekt unterstützt muss nicht im Speicher aufbewahrt werden, da MAPI Speicher durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) freigibt, und das Objekt dann frei. Ressourcen freizugeben, rufen Sie **MakeInvalid**, und klicken Sie dann das Objekt ungültig zu ignorieren. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

