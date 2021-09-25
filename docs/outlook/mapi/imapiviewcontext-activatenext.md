---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d4d8f2b8ea54c4eaa7fd6dff7b8051e20780504
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625266"
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
  
> [in] Statuskennzeichnungen, die Informationen über die zu aktivierende Nachricht enthalten. Gültige Flageinstellungen sind:
    
  - VCDIR_CATEGORY: Der Betrachter sollte eine Nachricht in einer anderen Kategorie der Ansicht aktivieren. Die zu aktivierende Nachricht lautet: 
        
    - Die erste Meldung in der nächsten Ansichtskategorie, wenn dieses Flag OR-ed mit VCDIR_NEXT ist. 
        
    - Die letzte Meldung in der vorherigen Ansichtskategorie, wenn dieses Flag OR-ed mit VCDIR_PREV ist und die vorherige Kategorie erweitert wird. 
        
    - Die erste Meldung in der vorherigen Ansichtskategorie, wenn dieses Flag OR-ed mit VCDIR_PREV ist und die vorherige Kategorie nicht erweitert wird. In diesem Fall wird die vorherige Kategorie automatisch erweitert. 
        
  - VCDIR_DELETE: Der Betrachter sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht gelöscht wurde. 
        
  - VCDIR_MOVE: Der Betrachter sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht verschoben wurde. 
        
  - VCDIR_NEXT: Der Betrachter sollte die nächste Nachricht in der Ansichtsreihenfolge aktivieren. 
        
  - VCDIR_PREV: Der Betrachter sollte die vorherige Nachricht in der Ansichtsreihenfolge aktivieren. 
        
  - VCDIR_UNREAD: Der Betrachter sollte die nächste oder vorherige ungelesene Nachricht in der Ansichtsreihenfolge aktivieren. 
    
_prcPosRect_
  
> [in] Zeiger auf eine Windows **RECT-Struktur,** die die Größe und Position des Fensters enthält, das zum Anzeigen der aktivierten Nachricht verwendet werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aktiviert. 
    
S_FALSE 
  
> Die Nachricht wurde erfolgreich aktiviert, aber ein anderer Formulartyp wurde im Prozess geöffnet.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext::ActivateNext-Methode** auf, um zu ändern, welche Nachricht dem Benutzer angezeigt wird. Der im  _ulDir-Parameter_ übergebene Wert gibt an, welche Nachricht aktiviert werden soll und in einigen Fällen warum. Die Flags VCDIR_NEXT und VCDIR_PREVIOUS entsprechen den Benutzern, die den Befehl **"Weiter"** bzw. **"Zurück"** in einer Ansicht auswählen. Diese Vorgänge entsprechen in der Regel dem Auf- oder Abschalten einer Nachricht in der Nachrichtenliste der Formularanzeige. 
  
Die Flags VCDIR_DELETE und VCDIR_MOVE werden durch die Methoden [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) festgelegt. Implementierungen dieser Methoden rufen **ActivateNext** mit der entsprechenden Richtung auf und führen dann den angeforderten Vorgang für die Nachricht aus, wenn der **ActivateNext-Aufruf** nicht fehlschlägt. Formularanzeigen ermöglichen es Benutzern in der Regel, die Richtung anzugeben, in der die Nachrichtenliste verschoben werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre Implementierung von [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) macht die nächste oder vorherige Nachricht im Ordner, abhängig vom Wert von  _ulDir,_ der aktuellen Nachricht. Nachdem **ActivateNext** zurückgegeben wurde, rufen [Sie IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) auf, um einen Zeiger auf die neu aktivierte Nachricht abzurufen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ActivateNext** S_FALSE zurückgibt oder wenn keine aktuelle Nachricht vorhanden ist, führen Sie die normale Prozedur zum Herunterfahren aus, die das Aufrufen der [IMAPIForm::ShutdownForm-Methode](imapiform-shutdownform.md) ihres Formulars umfassen sollte. Wenn eine nächste oder vorherige Meldung angezeigt wird, verwenden Sie das Fensterrechteck, das im  _PrcPosRect-Parameter_ übergeben wurde, um sie anzuzeigen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implementiert die **IMAPIViewContext::ActivateNext-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

