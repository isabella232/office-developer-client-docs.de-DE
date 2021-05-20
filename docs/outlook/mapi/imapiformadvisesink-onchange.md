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
  
Gibt an, dass eine Änderung im Status der Formularanzeige aufgetreten ist. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameter

 _ulDir_
  
> [in] Eine Bitmaske mit Flags, die Informationen über die im Viewer aufgetretene Änderung und die erwartete Antwort im Formular enthält. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche unterdrücken, auch als Reaktion auf ein Verb, das normalerweise dazu führt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular soll modal für die Formularanzeige sein. 
    
VCSTATUS_NEXT 
  
> Es gibt eine nächste Nachricht in der Formularanzeige. 
    
VCSTATUS_PREV 
  
> Es ist eine vorherige Nachricht in der Formularanzeige. 
    
VCSTATUS_READONLY 
  
> Lösch-, Absenden- und Verschiebevorgänge sollten deaktiviert sein. 
    
VCSTATUS_UNREAD 
  
> Es gibt eine nächste oder vorherige ungelesene Nachricht in der Formularanzeige.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormAdviseSink::OnChange-Methode** auf, um das Formular über eine Änderung des Status eines Betrachters zu benachrichtigen. In der Regel ist die einzige Änderung das Festlegen oder Löschen der VCSTATUS_NEXT oder VCSTATUS_PREVIOUS basierend auf dem Vorhandensein oder Fehlen einer nächsten oder vorherigen Nachricht im Viewer. Entsprechend aktiviert oder deaktiviert das Formularobjekt dann alle nächsten oder vorherigen Aktionen, die es unterstützt. 
  
Die Einstellungen von VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können sich in einem Ansichtskontext nicht ändern, nachdem er erstellt wurde.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die spezifische Implementierung dieser Methode hängt vollständig von den Besonderheiten des Formulars ab. Die meisten Formularobjekte verwenden diese Methode, um ihre Benutzeroberfläche zu ändern (z. B. zum Aktivieren oder Deaktivieren von Menübefehlen oder Schaltflächen, die mit dem Parameter "Viewer status flags" übereinstimmen).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

