---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588503"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aktiviert die nächste oder vorherige Nachricht in der Anzeigereihenfolge. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

_ulDir_
  
> [in] Status Kennzeichen mit Informationen über die Meldung an, die aktiviert werden. Gültige Flageinstellungen sind:
    
  - VCDIR_CATEGORY: Betrachter sollte eine Nachricht in einer anderen Kategorie der Ansicht zu aktivieren. Wird die Meldung an, die aktiviert werden: 
        
    - Die erste Meldung in der nächsten Ansichtskategorie aus, wenn dieses Flag **oder**Ed mit VCDIR_NEXT ist. 
        
    - Die letzte Meldung in der vorherigen Ansichtskategorie ist dieses Flag **OR**Ed mit VCDIR_PREV und der vorherigen Kategorie wird erweitert. 
        
    - Die erste Meldung in der vorherigen Ansichtskategorie ist dieses Flag **OR**Ed mit VCDIR_PREV und der vorherigen Kategorie erweitert nicht verwendet werden. In diesem Fall der vorherige Kategorie Automatische Erweiterung Deklaration. 
        
  - VCDIR_DELETE: Betrachter sollte die nächste oder der vorherige Nachricht aktiviert werden, da die aktuelle Nachricht gelöscht wurde. 
        
  - VCDIR_MOVE: Betrachter sollte die nächste oder der vorherige Nachricht aktiviert werden, da die aktuelle Nachricht verschoben wurde. 
        
  - VCDIR_NEXT: Betrachter sollte die nächste Nachricht in der Anzeigereihenfolge aktivieren. 
        
  - VCDIR_PREV: Betrachter sollte die vorherige Nachricht in der Anzeigereihenfolge aktivieren. 
        
  - VCDIR_UNREAD: Betrachter sollte die nächste oder Vorherige ungelesene Nachricht in der Anzeigereihenfolge aktivieren. 
    
_prcPosRect_
  
> [in] Zeiger auf eine Windows **Rechteck** -Struktur mit der Größe und Position des Fensters, zum Anzeigen der aktivierten Nachricht verwendet werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aktiviert. 
    
S_FALSE 
  
> Die Nachricht wurde erfolgreich aktiviert, aber ein anderen Typ des Formulars im Prozess geöffnet wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte Aufrufen die **IMAPIViewContext::ActivateNext** -Methode zum Ändern, welche Meldung für den Benutzer angezeigt wird. Der im _UlDir_ -Parameter übergebene Wert gibt an, welche Meldung sein sollte aktiviert und in einigen Fällen, warum. Die Flags VCDIR_NEXT und VCDIR_PREVIOUS entsprechen den Benutzer, die Sie den **nächsten** oder **vorherigen** Befehl in einer Ansicht auswählen. Diese Vorgänge entsprechen in der Regel nach oben oder nach unten eine Nachricht in der Liste der Nachrichten der Formular-Viewer verschieben. 
  
Die Flags VCDIR_DELETE und VCDIR_MOVE werden durch die [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) -Methoden, festgelegt. Implementierung dieser Methoden rufen Sie **ActivateNext** , wobei die entsprechende Richtung, und führen Sie dann den angeforderten Vorgang für die Nachricht, wenn der Anruf **ActivateNext** nicht fehlgeschlagen ist. Formular Viewer können in der Regel Benutzer geben Sie die Richtung, in der Liste zu verschieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) wird die nächste oder der vorherige Nachricht im Ordner, abhängig vom Wert der _UlDir_, die aktuelle Nachricht. Nachdem **ActivateNext** zurückgegeben wird, rufen Sie [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) , um einen Zeiger auf den neu aktivierten Nachricht erhalten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Führen Sie Wenn **ActivateNext** S_FALSE zurückgibt, oder wenn eine aktuelle Nachricht nicht vorhanden ist, Ihre normalen Herunterfahren der enthalten sollte das Formular [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) -Methode aufrufen. Wenn eine Nachricht nächste oder vorherige angezeigt wird, verwenden Sie das Fenster Rechteck im _PrcPosRect_ -Parameter übergeben, um es anzuzeigen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI (engl.) implementiert die **IMAPIViewContext::ActivateNext** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

