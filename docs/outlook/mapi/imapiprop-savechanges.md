---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 152459c6d7111e6d5548ffbd31319d53462de5d0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620954"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nimmt dauerhafte Änderungen vor, die seit dem letzten Speichervorgang an einem Objekt vorgenommen wurden. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, was mit dem Objekt geschieht, wenn die **IMAPIProp::SaveChanges-Methode** aufgerufen wird. Die folgenden Flags können festgelegt werden: 
    
NON_EMS_XP_SAVE
  
> Gibt an, dass die Nachricht nicht von einem Microsoft Exchange Server zugestellt wurde. Dieses Flag sollte in Kombination mit der [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) und dem ITEMPROC_FORCE Flag verwendet werden, um einem PST-Speicher anzugeben, dass die Nachricht für die Verarbeitung von Regeln berechtigt ist, bevor der PST-Speicher (Personal Folders File) jeden Überwachungsclient benachrichtigt, dass die Nachricht angekommen ist. Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server erstellt werden, der kein Exchange Server ist. In diesem Fall hätte der Exchange Server bereits Regeln für die Nachricht verarbeitet. 
    
FORCE_SAVE 
  
> Änderungen sollten in das Objekt geschrieben werden, wobei alle vorherigen Änderungen überschrieben werden, die am Objekt vorgenommen wurden, und das Objekt sollte geschlossen werden. Die Lese-/Schreibberechtigung muss festgelegt werden, damit der Vorgang erfolgreich ausgeführt werden kann. Das FORCE_SAVE Flag wird nach einem vorherigen Aufruf von **SaveChanges** verwendet, der MAPI_E_OBJECT_CHANGED zurückgegeben wurde. 
    
KEEP_OPEN_READONLY 
  
> Es sollte ein Commit für Änderungen ausgeführt werden, und das Objekt sollte zum Lesen geöffnet bleiben. Es werden keine weiteren Änderungen vorgenommen. 
    
KEEP_OPEN_READWRITE 
  
> Es sollte ein Commit für Änderungen ausgeführt werden, und das Objekt sollte für Lese-/Schreibberechtigungen geöffnet bleiben. Dieses Kennzeichen wird normalerweise festgelegt, wenn das Objekt zum ersten Mal mit Lese-/Schreibberechtigung geöffnet wurde. Nachfolgende Änderungen am Objekt sind zulässig. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **SaveChanges** die erfolgreiche Rückgabe, möglicherweise bevor für die Änderungen ein vollständiger Commit ausgeführt wurde. 
    
SPAMFILTER_ONSAVE
  
> Aktiviert die Spamfilterung für eine Nachricht, die gespeichert wird. Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Engagement von Änderungen war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** kann das Objekt nicht für schreibgeschützte Berechtigungen geöffnet lassen, wenn KEEP_OPEN_READONLY festgelegt ist, oder lese-/schreibgeschützt, wenn KEEP_OPEN_READWRITE festgelegt ist. Es wird kein Commit für Änderungen ausgeführt. 
    
MAPI_E_OBJECT_CHANGED 
  
> Das Objekt wurde seit dem Öffnen geändert.
    
MAPI_E_OBJECT_DELETED 
  
> Das Objekt wurde gelöscht, seit es geöffnet wurde.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp::SaveChanges-Methode macht Eigenschaftsänderungen** für Objekte, die das Transaktionsmodell der Verarbeitung unterstützen, wie Nachrichten, Anlagen, Adressbuchcontainer und Messaging-Benutzerobjekte, dauerhaft. Objekte, die Transaktionen nicht unterstützen, z. B. Ordner, Nachrichtenspeicher und Profilabschnitte, nehmen änderungen sofort dauerhaft vor. Es ist kein Aufruf von **SaveChanges** erforderlich. 
  
Da Dienstanbieter erst nach dem Speichern aller Eigenschaften einen Eintragsbezeichner für ihre Objekte generieren müssen, ist die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) eines Objekts möglicherweise erst verfügbar, nachdem die **SaveChanges-Methode** aufgerufen wurde. Einige Anbieter warten, bis das KEEP_OPEN_READONLY Flag für den **SaveChanges-Aufruf** festgelegt ist. KEEP_OPEN_READONLY gibt an, dass die im aktuellen Aufruf zu speichernden Änderungen die letzten Änderungen sind, die am Objekt vorgenommen werden. 
  
Einige Implementierungen des Nachrichtenspeichers zeigen neu erstellte Nachrichten erst dann in einem Ordner an, wenn ein Client die Nachrichtenänderungen mithilfe von **SaveChanges** speichert und die Nachrichtenobjekte mithilfe der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) freigibt. Darüber hinaus können einige Objektimplementierungen eine **PR_ENTRYID** Eigenschaft für ein neu erstelltes Objekt erst generieren, nachdem **SaveChanges** aufgerufen wurde, und einige können dies nur tun, nachdem **SaveChanges** mithilfe KEEP_OPEN_READONLY in  _ulFlags_ festgelegt wurde.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie das Flag KEEP_OPEN_READONLY erhalten, können Sie den Zugriff des Objekts mit Lese-/Schreibzugriff belassen. Ein Anbieter kann ein Objekt jedoch nie in einem schreibgeschützten Zustand belassen, wenn das KEEP_OPEN_READWRITE-Kennzeichen übergeben wird.
  
Wenn ein Client mehrere Anlagen in mehreren Nachrichten speichert, ruft er die **SaveChanges-Methode** für jede Anlage und jede Nachricht auf. Clients legen häufig MAPI_DEFERRED_ERRORS für jeden dieser Anrufe mit Ausnahme des letzten fest. Sie können Fehler entweder beim letzten oder bei früheren Anrufen zurückgeben. Sie können das Kennzeichen sogar ignorieren. 
  
Wenn KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Fehlerverzögerungsanforderung ignorieren. Wenn MAPI_DEFERRED_ERRORS nicht in  _ulFlags_ festgelegt ist, kann einer der zuvor zurückgestellten Fehler für den **SaveChanges-Aufruf** zurückgegeben werden. 
  
Ob ein Remote-Transport-Anbieter eine funktionale Implementierung dieser Methode bereitstellt, ist optional und hängt von anderen Entwurfsentscheidungen in Ihrer Implementierung ab. Wenn Sie diese Methode implementieren, tun Sie dies gemäß der hier aufgeführten Dokumentation. Da Keine Transaktionen mit Ordnerobjekten und Statusobjekten durchgeführt werden, muss mindestens die Implementierung von **SaveChanges** durch einen Remote-Transportanbieter S_OK zurückgeben, ohne tatsächlich arbeiten zu müssen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client KEEP_OPEN_READONLY übergibt, die [IMAPIProp::SetProps-Methode aufruft](imapiprop-setprops.md) und **dann Erneut SaveChanges aufruft,** schlägt die gleiche Implementierung möglicherweise fehl. 
  
Nachdem Sie MAPI_E_NO_ACCESS von einem Anruf erhalten haben, in dem Sie KEEP_OPEN_READWRITE festlegen, verfügen Sie weiterhin über Lese-/Schreibberechtigungen für das Objekt. Sie können **SaveChanges** erneut aufrufen, indem Sie entweder das KEEP_OPEN_READONLY flag oder keine Flags mit KEEP_OPEN_SUFFIX übergeben. 
  
Ob ein Anbieter das KEEP_OPEN_READWRITE Flag unterstützt, hängt von der Implementierung des Anbieters ab. 
  
Um anzugeben, dass der einzige Aufruf für das Objekt nach **SaveChanges** **IUnknown::Release** ist, legen Sie keine Flags für den  _ulFlags-Parameter_ fest. Ein Fehler von **SaveChanges** weist darauf hin, dass die ausstehenden Änderungen nicht dauerhaft sein konnten. Unterschiedliche Anbieter behandeln das Fehlen von Flags im **SaveChanges-Aufruf** unterschiedlich. Einige Anbieter behandeln diesen Zustand genauso wie KEEP_OPEN_READONLY; andere Anbieter interpretieren sie genauso wie KEEP_OPEN_READWRITE. Andere Anbieter fahren das Objekt herunter, wenn sie keine Flags für den **SaveChanges-Aufruf** erhalten. 
  
Einige Eigenschaften, in der Regel berechnete Eigenschaften, können erst verarbeitet werden, wenn Sie **SaveChanges** aufrufen und in einigen Fällen **Release**.
  
Wenn Sie Massenänderungen vornehmen, z. B. Anlagen in mehreren Nachrichten speichern, verzögern Sie die Fehlerverarbeitung, indem Sie das flag MAPI_DEFERRED_ERRORS in  _ulFlags_ festlegen. Wenn Sie mehrere Anlagen in mehreren Nachrichten speichern, führen Sie einen **SaveChanges-Aufruf** für jede Anlage und einen **SaveChanges-Aufruf** für jede Nachricht aus. Legen Sie das flag MAPI_DEFERRED_ERRORS für jeden Anlagenaufruf und für alle Nachrichten mit Ausnahme des letzten fest. 
  
Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgibt, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde. Wenn ja, warnen Sie den Benutzer, der entweder anfordern kann, dass die Änderungen die vorherigen Änderungen überschreiben oder das Objekt an anderer Stelle speichern. Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer, dem Benutzer die Möglichkeit zu geben, das Objekt an einem anderen Speicherort zu speichern. 
  
Sie können **SaveChanges** nicht mit dem flag FORCE_SAVE für ein geöffnetes Objekt aufrufen, das gelöscht wurde. 
  
Wenn **SaveChanges** einen Fehler zurückgibt, bleibt das Objekt, dessen Änderungen gespeichert werden sollten, geöffnet, unabhängig von den im  _ulFlags-Parameter_ festgelegten Flags. 
  
> [!IMPORTANT]
> Die  _ulFlags-NON_EMS_XP_SAVE_ und SPAMFILTER_ONSAVE sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie Ihrem Code mit den folgenden Werten hinzufügen: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften.](saving-mapi-properties.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Speichern von MAPI-Eigenschaften](saving-mapi-properties.md)

