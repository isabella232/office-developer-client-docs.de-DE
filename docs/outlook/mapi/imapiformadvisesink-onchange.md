---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4ed41bc702d6296d1c714e89f99e9fac63ca055d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579908"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass im Status der Formularanzeige eine Änderung vorgenommen wurde. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameter

 _ulDir_
  
> [in] Eine Bitmaske mit Flags, die Informationen über die Änderung im Viewer und die erwartete Antwort im Formular bereitstellt. Die folgenden Flags können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_INTERACTIVE 
  
> Das Formular sollte eine Benutzeroberfläche anzeigen. Wenn dieses Kennzeichen nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche auch als Reaktion auf ein Verb unterdrücken, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular muss an die Formularanzeige gebunden werden. 
    
VCSTATUS_NEXT 
  
> Es gibt eine nächste Meldung in der Formularanzeige. 
    
VCSTATUS_PREV 
  
> Es ist eine vorherige Meldung in der Formularanzeige vorhanden. 
    
VCSTATUS_READONLY 
  
> Lösch-, Sende- und Verschiebungsvorgänge sollten deaktiviert werden. 
    
VCSTATUS_UNREAD 
  
> Es ist eine nächste oder vorherige ungelesene Nachricht in der Formularanzeige vorhanden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormAdviseSink::OnChange-Methode auf,** um das Formular über eine Änderung des Status eines Betrachters zu benachrichtigen. In der Regel besteht die einzige Änderung darin, das VCSTATUS_NEXT oder VCSTATUS_PREVIOUS Flag basierend auf dem Vorhandensein oder Fehlen einer nächsten oder vorherigen Nachricht im Viewer festzulegen oder zu löschen. Entsprechend aktiviert oder deaktiviert das Formularobjekt alle nächsten oder vorherigen unterstützten Aktionen. 
  
Die Einstellungen von VCSTATUS_MODAL und VCSTATUS_INTERACTIVE können in einem Ansichtskontext nach der Erstellung nicht mehr geändert werden.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die spezifische Implementierung dieser Methode hängt vollständig von den Einzelheiten des Formulars ab. Die meisten Formularobjekte verwenden diese Methode, um ihre Benutzeroberfläche zu ändern (z. B. um Menübefehle oder Schaltflächen zu aktivieren oder zu deaktivieren, die dem Parameter "Viewer Status Flags" entsprechen).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

