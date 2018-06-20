---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a60b813a52779b28124ab6d69b493def35b14aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792294"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Betrifft**: Outlook 
  
Macht dauerhaft entfernt alle Änderungen, die seit dem letzten Speichervorgang auf ein Objekt vorgenommen wurden. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, was auf das Objekt geschieht, wenn die **IMAPIProp::SaveChanges** -Methode aufgerufen wird. Die folgenden Kennzeichen können festgelegt werden: 
    
NON_EMS_XP_SAVE
  
> Gibt an, dass die Nachricht von einem Microsoft Exchange Server nicht übermittelt werden konnte. Dieses Flag in Kombination mit der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode verwendet werden soll, und das Flag ITEMPROC_FORCE, um eine PST-Speichers anzuzeigen, die die Nachricht ist für Regeln für die Verarbeitung vor der Informationsspeicher für Persönliche Ordner-Datei (PST) eine benachrichtigt überwachungs-Client, der die Nachricht empfangen hat. Diese Regeln, die Verarbeitung gilt nur für neue Nachrichten, die erstellt werden mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server, der keinem Exchange-Server in diesem Fall ist der Exchange-Server würde bereits Regeln für die Nachricht verarbeitet. 
    
FORCE_SAVE 
  
> Änderungen geschrieben werden soll, auf das Objekt, das Überschreiben alle vorherigen Änderungen, die auf das Objekt vorgenommen wurden, und das Objekt geschlossen werden sollte. Lese-/Schreibberechtigung für muss für den Vorgang festgelegt werden. Das Flag FORCE_SAVE wird verwendet, nachdem ein vorherigen Aufruf von **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben. 
    
KEEP_OPEN_READONLY 
  
> Änderungen ein Commit ausgeführt werden soll, und das Objekt zum Lesen geöffnet beibehalten werden sollten. Keine zusätzlichen Änderungen werden vorgenommen werden. 
    
KEEP_OPEN_READWRITE 
  
> Änderungen ein Commit ausgeführt werden soll, und das Objekt für die Berechtigung Lese-/Schreibzugriff geöffnet beibehalten werden sollten. Dieses Kennzeichen werden in der Regel festgelegt, wenn das Objekt zum ersten Mal Lese-/Schreibzugriff geöffnet wurde. Nachfolgende Änderungen am Objekt sind zulässig. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **SaveChanges** erfolgreich, möglicherweise beendet, bevor die Änderungen vollständig übertragen wurden. 
    
SPAMFILTER_ONSAVE
  
> Ermöglicht die Spamfilterung für eine Nachricht ein, die gespeichert wird. Unterstützung der Spamfilterung steht nur, wenn der Absender e-Mail-Adresstyp Simple Mail Transfer Protocol (SMTP ist), und die Nachricht einen Speicher für Persönliche Ordner-Datei (PST) gespeichert werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Engagement der Änderungen erfolgreich war.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** kann nicht das Objekt geöffnet lassen für nur-Lese-Berechtigung Wenn KEEP_OPEN_READONLY festgelegt, oder Lese-/Schreibberechtigung für Wenn KEEP_OPEN_READWRITE festgelegt ist. Es sind keine Änderungen ein Commit ausgeführt. 
    
MAPI_E_OBJECT_CHANGED 
  
> Das Objekt wurde geändert seit es geöffnet wurde.
    
MAPI_E_OBJECT_DELETED 
  
> Das Objekt wurde gelöscht, da es geöffnet wurde.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::SaveChanges** -Methode ändert Eigenschaft permanente für Objekte, die Unterstützung für das Transaktionsmodell verarbeiten, wie Nachrichten, Anlagen, Address Book-Container und messaging User-Objekte. Objekte, die keine für Transaktionen im Ordner, Nachrichtenspeicher und Profil Abschnitte Unterstützung, nehmen Sie Änderungen permanente sofort. Kein Aufruf von **SaveChanges** ist erforderlich. 
  
Da Dienstanbieter keine generieren einen Eintrag Bezeichner für Objekte, bis alle Eigenschaften gespeichert wurden, ein Objekt **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft möglicherweise nicht verfügbar erst nach seiner **SaveChanges** -Methode wurde aufgerufen. Einige Anbieter warten Sie, bis das Flag KEEP_OPEN_READONLY festgelegt ist auf der **SaveChanges** -Anruf. KEEP_OPEN_READONLY gibt an, dass die Änderungen in den aktuellen Anruf gespeichert werden die letzten Änderungen eingefügt werden, die auf dem Objekt vorgenommen wird. 
  
Einige Nachricht Store Implementierungen führen keine Nachrichten in einem Ordner anzeigen, die neu erstellte bis zu einem Client speichert die Nachricht mithilfe von **SaveChanges** geändert und Nachrichtenobjekte mithilfe der [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode frei. Darüber hinaus können nicht einige Implementierungen Objekt eine **PR_ENTRYID** -Eigenschaft für ein neu erstelltes Objekt erst nach dem Erstellen **SaveChanges** aufgerufen wurde, und einige können dies tun, wenn **SaveChanges** mithilfe von KEEP_OPEN_READONLY aufgerufen wurde Legen Sie in _UlFlags_.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie die Kennzeichen KEEP_OPEN_READONLY erhalten, müssen Sie die Option verlassen das Objekt Zugriff mit Lese-/Schreibzugriff. Jedoch kann ein Anbieter nie lassen Sie ein Objekt in einem schreibgeschützten Zustand, wenn das Flag KEEP_OPEN_READWRITE übergeben wird.
  
Wenn ein Client mehrere Anlagen auf mehrere Nachrichten speichert, ruft es die **SaveChanges** -Methode für jede Anlage und jede Nachricht. Häufig Clients werden für jede dieser Anrufe mit Ausnahme der letzten MAPI_DEFERRED_ERRORS festgelegt. Sie können entweder mit dem letzten Aufruf oder einem früheren Anrufe Fehler zurückgeben. Sie können auch die Kennzeichen ignorieren. 
  
Wenn KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Fehler Aufschiebung Anforderung ignorieren. Wenn MAPI_DEFERRED_ERRORS in _UlFlags_nicht festgelegt ist, ein zuvor zurückgestellte Fehler zurückgegeben werden für den Anruf **SaveChanges** . 
  
Gibt an, ob ein remote-Transport-Anbieter eine funktionsfähige Implementierung dieser Methode bietet ist optional und hängt von anderen Designentscheidungen in Ihrer Implementierung. Wenn Sie diese Methode implementieren, führen Sie entsprechend der Dokumentation zur. Da Ordnerobjekten und Status Objekte nicht durchgeführt werden, muss mindestens eines remote Transportdienstes Implementierung der **SaveChanges** S_OK zurückgeben ohne tatsächlich keine Arbeit. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client KEEP_OPEN_READONLY übergibt, die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufgerufen und ruft dann erneut die **SaveChanges** , kann die gleiche Implementierung fehlschlagen. 
  
Nach Eingang eines Anrufs MAPI_E_NO_ACCESS in dem Sie KEEP_OPEN_READWRITE festgelegt, Sie haben weiterhin Lese-/Schreibberechtigung für das Objekt. Sie können auch das Kennzeichen KEEP_OPEN_READONLY oder keine Flags mit KEEP_OPEN_SUFFIX übergeben **SaveChanges** aufrufen. 
  
Ob das Flag KEEP_OPEN_READWRITE von einem Anbieter unterstützt, hängt von der Anbieter-Implementierung. 
  
Legen Sie keine Flags für den Parameter _UlFlags_ aus, um anzugeben, dass nur beim Aufruf von auf das Objekt nach **SaveChanges** vorgenommen werden **IUnknown**wird. Ein Fehler aus **SaveChanges** gibt an, dass es nicht die ausstehenden Änderungen dauerhaft entfernt wird konnte. Verschiedene Anbieter behandeln fehlen Kennzeichen für den Aufruf der **SaveChanges** unterschiedlich. Einige Anbieter behandelt diesen Zustand als KEEP_OPEN_READONLY. andere Anbieter interpretieren KEEP_OPEN_READWRITE identisch. Noch andere Anbieter das Objekt herunter, wenn sie keine Kennzeichen für den Aufruf der **SaveChanges** erhalten. 
  
Einige Eigenschaften, die in der Regel berechnete Eigenschaften können nicht verarbeitet werden, bis Sie **SaveChanges** aufrufen und in einigen Fällen **Version**.
  
Wenn Sie von massenänderungen vornehmen, wie Anlagen auf mehrere Nachrichten gespeichert zurückstellen Sie Fehler bei der Verarbeitung durch das Flag MAPI_DEFERRED_ERRORS in _UlFlags_festgelegt. Wenn Sie mehrere Anlagen auf mehrere Nachrichten speichern, stellen Sie eine **SaveChanges** Aufruf für jede Anlage und eine **SaveChanges** auf jede Nachricht aufrufen. Legen Sie das MAPI_DEFERRED_ERRORS-Flag für jeden Anruf Anlage und für alle Nachrichten mit Ausnahme der letzten. 
  
Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben wird, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde. In diesem Fall warnen Sie, und Benutzer entweder, dass die Änderungen die vorherigen Änderungen zu überschreiben, oder speichern Sie das Objekt an anderer Stelle angefordert werden kann. Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer um ihnen die Möglichkeit, speichern Sie das Objekt in einen anderen Speicherort zu verleihen. 
  
Sie können nicht mit dem FORCE_SAVE-Flag auf ein geöffnetes Objekt **SaveChanges** aufrufen, die gelöscht wurde. 
  
Wenn **SaveChanges** einen Fehler zurückgibt, das Objekt, dessen Änderungen wurden zu speichernde bleibt, öffnen, unabhängig von den im Parameter _UlFlags_ festgelegten Flags. 
  
> [!IMPORTANT]
> Die _UlFlags_ NON_EMS_XP_SAVE und SPAMFILTER_ONSAVE möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mithilfe der folgenden Werte hinzufügen: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Kanonische-Eigenschaft PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[Speichern von MAPI-Eigenschaften](saving-mapi-properties.md)

