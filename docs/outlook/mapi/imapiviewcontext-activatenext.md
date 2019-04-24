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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351156"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert die nächste oder vorherige Nachricht in der Ansichts Reihenfolge. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

_ulDir_
  
> in Status Kennzeichen mit Informationen über die zu aktivierende Nachricht. Gültige Flageinstellungen sind:
    
  - VCDIR_CATEGORY: der Viewer sollte eine Nachricht in einer anderen Kategorie der Ansicht aktivieren. Die zu aktivierende Nachricht lautet: 
        
    - Die erste Meldung in der nächsten Ansichtskategorie, wenn dieses Flag mit VCDIR_NEXT **oder**Ed ist. 
        
    - Die letzte Nachricht in der vorherigen Ansichtskategorie, wenn dieses Flag mit VCDIR_PREV **oder**Ed ist und die vorherige Kategorie erweitert ist. 
        
    - Die erste Meldung in der Kategorie vorherige Ansicht, wenn dieses Flag mit VCDIR_PREV **oder**Ed ist und die vorherige Kategorie nicht erweitert ist. In diesem Fall wird die vorherige Kategorie automatisch erweitert. 
        
  - VCDIR_DELETE: der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht gelöscht wurde. 
        
  - VCDIR_MOVE: der Viewer sollte die nächste oder vorherige Nachricht aktivieren, da die aktuelle Nachricht verschoben wurde. 
        
  - VCDIR_NEXT: der Viewer sollte die nächste Nachricht in der Ansichts Reihenfolge aktivieren. 
        
  - VCDIR_PREV: der Viewer sollte die vorherige Nachricht im Ansichts Auftrag aktivieren. 
        
  - VCDIR_UNREAD: der Viewer sollte die nächste oder vorherige ungelesene Nachricht in der Ansichts Reihenfolge aktivieren. 
    
_prcPosRect_
  
> in Zeiger auf eine Windows- **Rect** -Struktur mit der Größe und Position des Fensters, das zum Anzeigen der aktivierten Nachricht verwendet werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich aktiviert. 
    
S_FALSE 
  
> Die Nachricht wurde erfolgreich aktiviert, aber im Prozess wurde ein anderer Formulartyp geöffnet.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext:: ActivateNext** -Methode auf, um zu ändern, welche Nachricht dem Benutzer angezeigt wird. Der Wert, der im Parameter _ulDir_ übergeben wird, gibt an, welche Nachricht aktiviert werden soll und in einigen Fällen warum. Die VCDIR_NEXT-und VCDIR_PREVIOUS-Flags entsprechen Benutzern, die den **nächsten** oder **vorherigen** Befehl in einer Ansicht auswählen. Diese Vorgänge entsprechen in der Regel dem nach oben oder nach unten eine Nachricht in der Liste der Nachrichten des Formular Viewers. 
  
Die VCDIR_DELETE-und VCDIR_MOVE-Flags werden durch die Methoden [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) und [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) festgelegt. Implementierungen dieser Methoden rufen **ActivateNext** mit der entsprechenden Richtung auf und führen dann den angeforderten Vorgang für die Nachricht aus, wenn der **ActivateNext** -Aufruf nicht fehlgeschlagen ist. In der Formularanzeige können Benutzer in der Regel die Richtung angeben, die in der Nachrichtenliste verschoben werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) macht die nächste oder vorherige Nachricht im Ordner abhängig vom Wert von _ulDir_, der aktuellen Nachricht. Rufen Sie nach dem Zurückgeben von **ActivateNext** [IMAPIMessageSite:: getMessage](imapimessagesite-getmessage.md) auf, um einen Zeiger auf die neu aktivierte Nachricht abzurufen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **ActivateNext** den Wert S_FALSE zurückgibt oder eine aktuelle Nachricht nicht vorhanden ist, führen Sie den normalen Shutdown-Vorgang aus, der den Aufruf der [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) -Methode des Formulars umfasst. Wenn eine nächste oder eine vorherige Nachricht angezeigt wird, verwenden Sie das Fensterrechteck, das im _prcPosRect_ -Parameter übergeben wurde, um es anzuzeigen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext  <br/> |MFCMAPI implementiert die **IMAPIViewContext:: ActivateNext** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

