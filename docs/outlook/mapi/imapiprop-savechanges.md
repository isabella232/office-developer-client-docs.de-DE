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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316632"
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
  
> [in] Eine Bitmaske mit Flags, die steuert, was mit dem Objekt geschieht, wenn die **IMAPIProp::SaveChanges-Methode** aufgerufen wird. Die folgenden Kennzeichen können festgelegt werden: 
    
NON_EMS_XP_SAVE
  
> Gibt an, dass die Nachricht nicht von einem Microsoft Exchange Server. Dieses Flag sollte in Kombination mit der [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) und dem ITEMPROC_FORCE-Flag verwendet werden, um einem PST-Speicher anzuzeigen, dass die Nachricht für die Regelverarbeitung berechtigt ist, bevor der Speicher für persönliche Ordner (Personal Folders File, PST) jeden Abhörclient benachrichtigt, dass die Nachricht eingetroffen ist. Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server erstellt werden, der kein Exchange Server ist. In diesem Fall hätte die Exchange Server bereits Regeln für die Nachricht verarbeitet. 
    
FORCE_SAVE 
  
> Änderungen sollten in das Objekt geschrieben werden, wobei alle vorherigen Änderungen überschrieben werden, die am Objekt vorgenommen wurden, und das Objekt sollte geschlossen werden. Die Lese-/Schreibberechtigung muss festgelegt sein, damit der Vorgang erfolgreich ist. Das FORCE_SAVE wird nach einem vorherigen Aufruf von **SaveChanges** verwendet, der MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Änderungen sollten mit einem "Committed" und dem Objekt zum Lesen geöffnet bleiben. Es werden keine weiteren Änderungen vorgenommen. 
    
KEEP_OPEN_READWRITE 
  
> Änderungen sollten für Lese-/Schreibzugriff geöffnet bleiben. Dieses Flag wird in der Regel festgelegt, wenn das Objekt zum ersten Mal für Lese-/Schreibberechtigungen geöffnet wurde. Nachfolgende Änderungen am Objekt sind zulässig. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **es SaveChanges,** erfolgreich zurückzukehren, möglicherweise bevor die Änderungen vollständig vorgenommen wurden. 
    
SPAMFILTER_ONSAVE
  
> Aktiviert die Spamfilterung für eine Nachricht, die gespeichert wird. Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verpflichtung der Änderungen war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges kann** das Objekt nicht für schreibgeschützte Berechtigungen öffnen, wenn KEEP_OPEN_READONLY festgelegt ist, oder Lese-/Schreibberechtigungen, KEEP_OPEN_READWRITE festgelegt ist. Es werden keine Änderungen vorgenommen. 
    
MAPI_E_OBJECT_CHANGED 
  
> Das Objekt hat sich seit dem Öffnen geändert.
    
MAPI_E_OBJECT_DELETED 
  
> Das Objekt wurde seit dem Öffnen gelöscht.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::SaveChanges-Methode macht Eigenschaftsänderungen** für Objekte dauerhaft, die das Transaktionsmodell der Verarbeitung unterstützen, z. B. Nachrichten, Anlagen, Adressbuchcontainer und Messagingbenutzerobjekte. Objekte, die Keine Transaktionen unterstützen, z. B. Ordner, Nachrichtenspeicher und Profilabschnitte, nehmen Änderungen sofort dauerhaft vor. Es ist kein **Aufruf von SaveChanges** erforderlich. 
  
Da Dienstanbieter erst nach dem Speichern aller Eigenschaften eine Eintrags-ID für ihre Objekte generieren müssen, ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft eines Objekts möglicherweise erst verfügbar, nachdem die **SaveChanges-Methode** aufgerufen wurde. Einige Anbieter warten, bis das KEEP_OPEN_READONLY für den **SaveChanges-Aufruf festgelegt** ist. KEEP_OPEN_READONLY gibt an, dass die änderungen, die im aktuellen Aufruf gespeichert werden sollen, die letzten Änderungen sind, die am Objekt vorgenommen werden. 
  
Einige Nachrichtenspeicherimplementierungen zeigen neu erstellte Nachrichten erst in einem Ordner an, wenn ein Client die Nachrichtenänderungen mithilfe von **SaveChanges** speichert und die Nachrichtenobjekte mithilfe der [IUnknown::Release-Methode freilässt.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Darüber hinaus können einige Objektimplementierungen erst nach dem Aufruf von **SaveChanges** eine **PR_ENTRYID-Eigenschaft** für ein neu erstelltes Objekt generieren, und einige können dies erst tun, nachdem **SaveChanges** mithilfe von KEEP_OPEN_READONLY in _ulFlags_ aufgerufen wurde.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie das KEEP_OPEN_READONLY erhalten, haben Sie die Möglichkeit, den Zugriff des Objekts als Lese-/Schreibzugriff zu lassen. Ein Anbieter kann ein Objekt jedoch niemals in einem schreibgeschützten Zustand be lassen, wenn KEEP_OPEN_READWRITE übergeben wird.
  
Wenn ein Client mehrere Anlagen in mehreren Nachrichten speichert, ruft er die **SaveChanges-Methode** für jede Anlage und jede Nachricht auf. Häufig legen Clients MAPI_DEFERRED_ERRORS für jeden dieser Anrufe außer für den letzten Anruf ein. Sie können Fehler entweder mit dem letzten Anruf oder mit früheren Aufrufen zurückgeben. Sie können sogar das Flag ignorieren. 
  
Wenn eine KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Anforderung zur Fehlererhebung ignorieren. Wenn MAPI_DEFERRED_ERRORS in  _ulFlags_ nicht festgelegt ist, kann einer der zuvor verzögerten Fehler für den **SaveChanges-Aufruf zurückgegeben** werden. 
  
Ob ein Remotetransportanbieter eine funktionale Implementierung dieser Methode bietet, ist optional und hängt von anderen Entwurfsentscheidungen in Ihrer Implementierung ab. Wenn Sie diese Methode implementieren, tun Sie dies gemäß der hier gezeigten Dokumentation. Da Ordnerobjekte und Statusobjekte nicht transaktiviert werden, muss die Implementierung von **SaveChanges** durch einen Remotetransportanbieter mindestens S_OK zurückgeben, ohne dass tatsächlich eine Arbeit vor sich geht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client KEEP_OPEN_READONLY, die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufruft und **dann SaveChanges** erneut aufruft, kann dieselbe Implementierung fehlschlagen. 
  
Nachdem Sie MAPI_E_NO_ACCESS von einem Anruf empfangen haben, in dem Sie KEEP_OPEN_READWRITE festgelegt haben, verfügen Sie weiterhin über Lese-/Schreibberechtigung für das Objekt. Sie können **SaveChanges erneut** aufrufen, indem Sie entweder das KEEP_OPEN_READONLY oder keine Flags mit KEEP_OPEN_SUFFIX. 
  
Ob ein Anbieter das KEEP_OPEN_READWRITE unterstützt, hängt von der Implementierung des Anbieters ab. 
  
Legen Sie keine Flags für den _ulFlags-Parameter_ fest, um anzugeben, dass der einzige Aufruf für das Objekt nach **SaveChanges** **IUnknown::Release** ist. Ein Fehler von **SaveChanges** gibt an, dass die ausstehenden Änderungen nicht dauerhaft vorgenommen werden konnten. Unterschiedliche Anbieter behandeln das Fehlen von Kennzeichen für **den SaveChanges-Aufruf** unterschiedlich. Einige Anbieter behandeln diesen Zustand wie KEEP_OPEN_READONLY; andere Anbieter interpretieren sie genauso wie KEEP_OPEN_READWRITE. Andere Anbieter fahren das Objekt jedoch herunter, wenn sie keine Flags für den **SaveChanges-Aufruf** erhalten. 
  
Einige Eigenschaften, in der Regel berechnete Eigenschaften, können erst verarbeitet werden, wenn **Sie SaveChanges und** in einigen Fällen **Release aufrufen.**
  
Wenn Sie Massenänderungen vornehmen, z. B. Anlagen in mehreren Nachrichten speichern, können Sie die Fehlerverarbeitung zurückschieben, indem Sie MAPI_DEFERRED_ERRORS in _ulFlags festlegen._ Wenn Sie mehrere Anlagen in mehreren Nachrichten speichern, nehmen Sie einen **SaveChanges-Aufruf** für jede Anlage und einen **SaveChanges-Aufruf** für jede Nachricht vor. Legen Sie das MAPI_DEFERRED_ERRORS für jeden Anlagenaufruf und für alle Nachrichten außer dem letzten ein. 
  
Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde. Wenn ja, warnen Sie den Benutzer, der entweder anfordern kann, dass die Änderungen die vorherigen Änderungen überschreiben oder das Objekt an anderer Stelle speichern. Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer, ihm die Möglichkeit zu geben, das Objekt an einem anderen Speicherort zu speichern. 
  
**SaveChanges kann nicht mit** dem FORCE_SAVE für ein gelöschtes geöffnetes Objekt aufrufen. 
  
Wenn **SaveChanges** einen Fehler zurückgibt, bleibt das Objekt, dessen Änderungen gespeichert werden sollten, geöffnet, unabhängig von den im _ulFlags-Parameter festgelegten Flags._ 
  
> [!IMPORTANT]
> Die  _ulFlags-NON_EMS_XP_SAVE_ und SPAMFILTER_ONSAVE sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Werte hinzufügen: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Speichern von MAPI-Eigenschaften](saving-mapi-properties.md)

