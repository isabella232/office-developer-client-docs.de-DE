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
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576680"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass eine Änderung in den Status des Formular-Viewers aufgetreten ist. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameter

 _ulDir_
  
> [in] Eine Bitmaske aus Flags, die Informationen zur Änderung bereitstellt, die in die Ereignisanzeige und die erwartete Antwort im Format aufgetreten ist. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es ist eine Nachricht nächste oder vorherige in einer anderen Kategorie. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche angezeigt werden. Wenn dieses Flag nicht festgelegt ist, sollte das Formular unterdrückt eine Benutzeroberfläche anzeigen, auch als Antwort auf ein Verb, das in der Regel verursacht eine Benutzeroberfläche angezeigt werden. 
    
VCSTATUS_MODAL 
  
> Das Formular ist für den Betrachter Formular gebunden sein. 
    
VCSTATUS_NEXT 
  
> Es ist eine nächste Nachricht im Formular-Viewer. 
    
VCSTATUS_PREV 
  
> Es ist eine vorherige Nachricht im Formular-Viewer. 
    
VCSTATUS_READONLY 
  
> Löschen Sie, senden Sie, und verschieben Sie Vorgänge deaktiviert werden soll. 
    
VCSTATUS_UNREAD 
  
> Es ist eine nächste oder Vorherige ungelesene Nachricht im Formular-Viewer.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IMAPIFormAdviseSink::OnChange** -Methode, um das Formular über eine Änderung in einem Viewer Status zu benachrichtigen. In der Regel ist die einzige Änderung festlegen oder Löschen der basierend auf dem Vorhandensein oder Abwesenheit einer nächsten oder vorherigen Nachricht im Viewer VCSTATUS_NEXT oder VCSTATUS_PREVIOUS-Flag. Das Form-Objekt wird entsprechend, klicken Sie dann aktiviert, oder der nächsten oder vorherigen Aktionen unterstützten deaktiviert. 
  
Die Einstellungen VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können nicht in einem Ansichtskontext ändern, nachdem es erstellt wurde.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung dieser Methode ist die Merkmale des Formulars vollständig abhängig. Die meisten Formularobjekte mit dieser Methode können Sie ihre-Benutzeroberfläche (beispielsweise zum Aktivieren oder deaktivieren Menübefehle oder Schaltflächen entsprechend der Viewer Status Flags-Parameter) ändern.
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

