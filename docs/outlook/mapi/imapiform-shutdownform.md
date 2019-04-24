---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329477"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt das Formular.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parameter

 _ulSaveOptions_
  
> in Ein Wert, der steuert, ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird. Eine der folgenden Werte kann festgelegt werden:
    
SAVEOPTS_NOSAVE 
  
> Formulardaten sollten nicht gespeichert werden.
    
SAVEOPTS_PROMPTSAVE 
  
> Der Benutzer sollte aufgefordert werden, geänderte Daten im Formular zu speichern.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Formulardaten sollten gespeichert werden, wenn Sie seit dem letzten Speichern geändert wurden. Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional zur Verwendung der Funktionen für die SAVEOPTS_NOSAVE-Option wechseln.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde geschlossen.
    
E_UNEXPECTED 
  
> Das Formular wurde bereits durch einen vorherigen Aufruf von **ShutdownForm**geschlossen.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIForm:: ShutdownForm** -Methode auf, um ein Formular zu beenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie die folgenden Aufgaben in der Implementierung von **ShutdownForm**aus:
  
1. Überprüfen Sie, ob ein Viewer **ShutdownForm**nicht bereits aufgerufen hat, und geben Sie E_UNEXPECTED zurück. Obwohl dies unwahrscheinlich ist, sollten Sie überprüfen.
    
2. Rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Formulars auf, sodass der Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung abgeschlossen ist. 
    
3. Bestimmen Sie, ob ungespeicherte Änderungen an den Formulardaten vorhanden sind. Speichern Sie nicht gespeicherte Daten gemäß der Festlegung des _ulSaveOptions_ -Parameters, indem Sie die [IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md) -Methode des Viewers aufrufen. 
    
4. Zerstören Sie das Benutzeroberflächenfenster des Formulars.
    
5. Geben Sie die Nachrichten-und Nachrichtenwebsite Objekte Ihres Formulars durch Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methoden frei. 
    
6. Informieren Sie alle registrierten Betrachter des ausstehenden Herunterfahren durch Aufrufen der [IMAPIViewAdviseSink:: OnShutdown](imapiviewadvisesink-onshutdown.md) -Methoden. 
    
7. Rufen Sie die [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode auf, um die Registrierung Ihres Formulars für die Benachrichtigung abzubrechen, indem Sie den Advise-Senke-Zeiger auf **null**festlegen.
    
8. Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den Arbeitsspeicher für die Eigenschaften Ihres Formulars freizugeben. 
    
9. Rufen Sie die **IUnknown:: Release** -Methode des Formulars auf, die dem in Schritt 2 **AddRef** -Aufruf entspricht. 
    
10. Geben Sie S_OK zur�ck.
    
> [!NOTE]
> Nachdem diese Aktionen abgeschlossen wurden, sind die einzigen gültigen Methoden für das Form-Objekt, die aufgerufen werden können, die von der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ShutdownForm** zurückgegeben wird, unabhängig davon, ob ein Fehler zurückgegeben wird, lassen Sie das Formular durch Aufrufen seiner **IUnknown:: Release** -Methode los. Fehler, die von **ShutdownForm**zurückgegeben werden, können ignoriert werden.
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

