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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792128"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Betrifft**: Outlook 
  
Schließt das Formular.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parameter

 _ulSaveOptions_
  
> [in] Ein Wert, der steuert, wie und ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird. Eine der folgenden Werte kann festgelegt werden:
    
SAVEOPTS_NOSAVE 
  
> Formulardaten sollten nicht gespeichert werden.
    
SAVEOPTS_PROMPTSAVE 
  
> Der Benutzer sollte auf beliebige geänderten Daten im Formular zu speichern aufgefordert werden.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Formulardaten sollte gespeichert werden, wenn es seit die letzten Speichern geändert wurde. Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional wechseln Sie zur Verwendung der Funktionen für die Option SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Formular geschlossen wurde.
    
E_UNEXPECTED 
  
> Das Formular wurde bereits von einem vorherigen Aufruf von **ShutdownForm**geschlossen.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIForm::ShutdownForm** -Methode, um ein Formular zu schließen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie die folgenden Aufgaben in der Implementierung der **ShutdownForm**:
  
1. Überprüfen Sie, dass ein Viewer nicht bereits **ShutdownForm**aufgerufen wurde, und zurückgeben Sie E_UNEXPECTED, falls zutreffend. Obgleich dies unwahrscheinlich ist, sollten Sie überprüfen.
    
2. Rufen Sie das Formular [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) -Methode, sodass Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung beendet wird. 
    
3. Überprüfen Sie, ob alle nicht gespeicherten Änderungen an die Daten des Formulars. Speichern Sie nicht gespeicherte Daten entsprechend wie der Parameter _UlSaveOptions_ durch Aufrufen des Viewers [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) -Methode festgelegt wird. 
    
4. Zerstören Sie Fenster auf der Benutzeroberfläche des Formulars.
    
5. Freigeben des Formulars Nachricht und Standortobjekten Nachricht durch ihre [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methoden aufrufen. 
    
6. Benachrichtigt werden alle registrierte Leser von Berichten für die ausstehende beenden, indem Sie ihre [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) -Methoden aufrufen. 
    
7. Rufen Sie die [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode, um die Registrierung für Benachrichtigung des Formulars abbrechen, indem Sie der Advise-Empfängerzeiger auf **einen Nullwert fest**.
    
8. Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um den Speicherplatz für die Eigenschaften des Formulars freizugeben. 
    
9. Vergleich des in Schritt 2 **AddRef** -Aufrufs des Formulars **IUnknown** -Methode aufrufen. 
    
10. Geben Sie S_OK zur�ck.
    
> [!NOTE]
> Nachdem diese Aktionen abgeschlossen wurden, umfassen die einzige gültigen Methoden für das Form-Objekt, das aufgerufen werden kann, die die [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ShutdownForm** zurückgibt, unabhängig davon, ob ein Fehler zurückgegeben, lassen Sie das Formular durch Aufrufen seiner **IUnknown** -Methode. Sie können von **ShutdownForm**zurückgegebenen Fehler ignorieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)

