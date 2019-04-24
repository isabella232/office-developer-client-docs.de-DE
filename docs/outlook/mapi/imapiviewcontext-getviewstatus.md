---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351177"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den aktuellen viewerstatus ab. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> Out Zeiger auf eine Bitmaske von Flags, die den Status des Viewers bereitstellt. Die folgenden Flags können festgelegt werden:
    
VCSTATUS_CATEGORY 
  
> Es gibt eine nächste oder eine vorherige Nachricht in einer anderen Kategorie. 
    
VCSTATUS_DELETE 
  
> Das Formular ermöglicht das Entfernen von Nachrichten. 
    
VCSTATUS_INTERACTIVE 
  
> Im Formular sollte eine Benutzeroberfläche angezeigt werden. Wenn dieses Flag nicht festgelegt ist, sollte das Formular die Anzeige einer Benutzeroberfläche auch als Reaktion auf ein Verb unterdrücken, das in der Regel bewirkt, dass eine Benutzeroberfläche angezeigt wird. 
    
VCSTATUS_MODAL 
  
> Das Formular ist für den Viewer modal. 
    
VCSTATUS_NEXT 
  
> In der Ansicht wird eine nächste Nachricht angezeigt. 
    
VCSTATUS_PREV 
  
> In der Ansicht ist eine vorherige Nachricht vorhanden. 
    
VCSTATUS_READONLY 
  
> Die Nachricht soll im schreibgeschützten Modus geöffnet werden. Lösch-, Sende-und Verschiebungsvorgänge sollten deaktiviert werden. 
    
VCSTATUS_UNREAD 
  
> Es gibt eine nächste oder vorherige ungelesene Nachricht in der Ansicht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status des Viewers wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext:: GetViewStatus** -Methode auf, um zu bestimmen, ob in einer Formularansicht in einer oder in beide Richtungen Weitere Nachrichten aktiviert werden sollen, die in der Richtung, in der ein **Nächster** Befehl Nachrichten aktiviert, in der Richtung, in der **** ein vorheriger Befehl Nachrichten aktiviert, oder in beide Richtungen. Der Wert, auf den durch den _lpulStatus_ -Parameter verwiesen wird, wird verwendet, um zu bestimmen, ob die VCSTATUS_NEXT-und VCSTATUS_PREV-Flags für [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md)gültig sind. Wenn das VCSTATUS_DELETE-Flag festgelegt ist, aber nicht das VCSTATUS_READONLY-Flag, kann die Nachricht mithilfe der [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) -Methode gelöscht werden. 
  
In der Regel werden Menübefehle und Schaltflächen von Formularen deaktiviert, wenn Sie nicht für den Kontext des Betrachters gültig sind. Ein Betrachter kann ein Formular durch Aufrufen seiner [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) -Methode auf eine Änderung des Statushinweisen. 
  
Das VCSTATUS_MODAL-Flag wird festgelegt, wenn das Formular in das Fenster gebunden werden muss, dessen Handle im früheren [IMAPIForm::D overb](imapiform-doverb.md) -Aufruf übergeben wird. Wenn VCSTATUS_MODAL festgelegt ist, kann das Formular den Thread verwenden, in dem der **DoVerb** -Aufruf vorgenommen wurde, bis das Formular geschlossen wird. Wenn VCSTATUS_MODAL nicht festgelegt ist, sollte das Formular nicht in dieses Fenster gebunden sein und den Thread nicht verwenden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetViewStatus  <br/> |MFCMAPI implementiert die **IMAPIViewContext:: GetViewStatus** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

