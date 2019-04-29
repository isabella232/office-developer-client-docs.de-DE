---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431897"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass eine Änderung im Status des Formular-Viewers aufgetreten ist. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameter

 _ulDir_
  
> in Eine Bitmaske von Flags, die Informationen zur Änderung im Viewer und zur erwarteten Antwort im Formular bereitstellt. Die folgenden Flags können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder eine vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_INTERACTIVE 
  
> Im Formular sollte eine Benutzeroberfläche angezeigt werden. Wenn dieses Flag nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche unterdrücken, auch als Reaktion auf ein Verb, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular soll an den Formular Betrachter gebunden werden. 
    
VCSTATUS_NEXT 
  
> Es gibt eine nächste Nachricht im Formular-Viewer. 
    
VCSTATUS_PREV 
  
> Es gibt eine vorherige Nachricht im Formular-Viewer. 
    
VCSTATUS_READONLY 
  
> Lösch-, Sende-und Verschiebungsvorgänge sollten deaktiviert werden. 
    
VCSTATUS_UNREAD 
  
> Es gibt eine nächste oder vorherige ungelesene Nachricht im Formular-Viewer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormAdviseSink:: OnChange** -Methode auf, um das Formular über eine Änderung des Status eines Viewers zu benachrichtigen. In der Regel ist die einzige Änderung das Festlegen oder Deaktivieren des VCSTATUS_NEXT-oder VCSTATUS_PREVIOUS-Kennzeichens basierend auf dem vorhanden sein oder Fehlen einer nächsten oder einer vorherigen Nachricht im Viewer. Dementsprechend aktiviert oder deaktiviert das Form-Objekt alle nächsten oder vorherigen Aktionen, die unterstützt werden. 
  
Die Einstellungen von VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können nicht in einem Ansichtskontext geändert werden, nachdem Sie erstellt wurden.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die spezifische Implementierung dieser Methode ist vollständig von den Details des Formulars abhängig. Die meisten Formularobjekte verwenden diese Methode, um Ihre Benutzeroberfläche zu ändern (beispielsweise, um Menübefehle oder Schaltflächen so zu aktivieren oder zu deaktivieren, dass Sie mit dem Parameter Viewer Status Flags übereinstimmen).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

