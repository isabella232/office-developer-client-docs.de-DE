---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0aebc6236a4c364262904baa96fd1d1139c43ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571801"
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
  
> [in] Ein Wert, der steuert, wie oder ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird. Eine der folgenden Werte kann festgelegt werden:
    
SAVEOPTS_NOSAVE 
  
> Formulardaten sollten nicht gespeichert werden.
    
SAVEOPTS_PROMPTSAVE 
  
> Der Benutzer sollte aufgefordert werden, alle geänderten Daten im Formular zu speichern.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Formulardaten sollten gespeichert werden, wenn sie seit dem letzten Speichern geändert wurden. Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional zur Verwendung der Funktionalität für die option SAVEOPTS_NOSAVE wechseln.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Formular wurde geschlossen.
    
E_UNEXPECTED 
  
> Das Formular wurde bereits durch einen vorherigen Aufruf von **ShutdownForm** geschlossen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIForm::ShutdownForm-Methode** auf, um ein Formular zu schließen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie die folgenden Aufgaben in der Implementierung von **ShutdownForm aus:**
  
1. Überprüfen Sie, ob ein Viewer **shutdownForm** noch nicht aufgerufen hat, und geben Sie E_UNEXPECTED zurück, falls vorhanden. Obwohl dies unwahrscheinlich ist, sollten Sie dies überprüfen.
    
2. Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) Ihres Formulars auf, damit der Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung abgeschlossen ist. 
    
3. Bestimmen Sie, ob nicht gespeicherte Änderungen an den Formulardaten vorhanden sind. Speichern Sie nicht gespeicherte Daten entsprechend der Festlegung des  _ulSaveOptions-Parameters,_ indem Sie die [IMAPIMessageSite::SaveMessage-Methode](imapimessagesite-savemessage.md) Ihres Viewers aufrufen. 
    
4. Löschen Sie das Fenster der Benutzeroberfläche des Formulars.
    
5. Geben Sie die Nachrichten- und Nachrichtenwebsiteobjekte Ihres Formulars frei, indem Sie deren [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen. 
    
6. Benachrichtigen Sie alle registrierten Benutzer über das ausstehende Herunterfahren, indem Sie ihre [IMAPIViewAdviseSink::OnShutdown-Methoden](imapiviewadvisesink-onshutdown.md) aufrufen. 
    
7. Rufen Sie die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) auf, um die Registrierung ihres Formulars für Benachrichtigungen abzubrechen, indem Sie den Verweis auf die Rate-Senken auf **NULL** festlegen.
    
8. Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den Speicher für die Eigenschaften Ihres Formulars freizugeben. 
    
9. Rufen Sie die **IUnknown::Release-Methode** Ihres Formulars auf, die dem **AddRef-Aufruf** in Schritt 2 entspricht. 
    
10. Geben Sie S_OK zur�ck.
    
> [!NOTE]
> Nachdem diese Aktionen abgeschlossen wurden, sind die einzigen gültigen Methoden für das Formularobjekt, die aufgerufen werden können, diejenigen aus der [IUnknown-Schnittstelle.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ShutdownForm** zurückgegeben wird, unabhängig davon, ob ein Fehler zurückgegeben wird, geben Sie das Formular frei, indem Sie seine **IUnknown::Release-Methode** aufrufen. Sie können alle von **ShutdownForm** zurückgegebenen Fehler ignorieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

