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
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410616"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert die nächste oder vorherige Nachricht in der Ansichtsreihenfolge. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

_ulDir_
  
> [in] Statuskennzeichen, die Informationen zur zu aktivierende Nachricht enthalten. Gültige Kennzeicheneinstellungen sind:
    
  - VCDIR_CATEGORY: Der Viewer sollte eine Nachricht in einer anderen Kategorie der Ansicht aktivieren. Die zu aktivierende Nachricht lautet: 
        
    - Die erste Nachricht in der nächsten Ansichtskategorie, wenn dieses Flag **or** ed with VCDIR_NEXT. 
        
    - Die letzte Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag **or** ed mit VCDIR_PREV und die vorherige Kategorie erweitert wird. 
        
    - Die erste Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag **or** ed mit VCDIR_PREV und die vorherige Kategorie nicht erweitert wird. In diesem Fall wird die vorherige Kategorie automatisch enpaniert. 
        
  - VCDIR_DELETE: Der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht gelöscht wurde. 
        
  - VCDIR_MOVE: Der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht verschoben wurde. 
        
  - VCDIR_NEXT: Der Viewer sollte die nächste Nachricht in der Ansichtsreihenfolge aktivieren. 
        
  - VCDIR_PREV: Der Viewer sollte die vorherige Nachricht in der Ansichtsreihenfolge aktivieren. 
        
  - VCDIR_UNREAD: Der Viewer sollte die nächste oder vorherige ungelesene Nachricht in der Ansichtsreihenfolge aktivieren. 
    
_prcPosRect_
  
> [in] Zeiger auf eine Windows **RECT-Struktur,** die die Größe und Position des Fensters enthält, das zum Anzeigen der aktivierten Nachricht verwendet werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aktiviert. 
    
S_FALSE 
  
> Die Nachricht wurde erfolgreich aktiviert, es wurde jedoch ein anderer Formulartyp geöffnet.
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIViewContext::ActivateNext-Methode** auf, um zu ändern, welche Nachricht für den Benutzer angezeigt wird. Der im  _ulDir-Parameter_ übergebene Wert gibt an, welche Nachricht aktiviert werden soll und in einigen Fällen warum. Die VCDIR_NEXT und VCDIR_PREVIOUS entsprechen benutzern, die den **Befehl**  Weiter bzw. Zurück in einer Ansicht auswählen. Diese Vorgänge entsprechen in der Regel dem Verschieben einer Nachricht nach oben oder unten in der Liste der Nachrichten der Formularanzeige. 
  
Die VCDIR_DELETE und VCDIR_MOVE werden von den [Methoden IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) festgelegt. Implementierungen dieser Methoden rufen **ActivateNext** mit der entsprechenden Richtung auf und führen dann den angeforderten Vorgang für die Nachricht aus, wenn beim **ActivateNext-Aufruf** kein Fehler auftritt. Mit Formularanzeigen können Benutzer in der Regel die Richtung angeben, die in der Nachrichtenliste bewegt werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre Implementierung von [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) erstellt die nächste oder vorherige Nachricht im Ordner, abhängig vom Wert von  _ulDir_, der aktuellen Nachricht. Rufen Sie nach der Rückgabe von **ActivateNext** [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) auf, um einen Zeiger auf die neu aktivierte Nachricht zu erhalten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ActivateNext** S_FALSE oder eine aktuelle Nachricht nicht vorhanden ist, führen Sie die normale Herunterfahrensprozedur aus, die das Aufrufen der [IMAPIForm::ShutdownForm-Methode](imapiform-shutdownform.md) Ihres Formulars umfassen sollte. Wenn eine nächste oder vorherige Nachricht angezeigt wird, verwenden Sie das Fensterrechteck, das im  _prcPosRect-Parameter_ übergeben wird, um sie anzuzeigen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implementiert die **IMAPIViewContext::ActivateNext-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

