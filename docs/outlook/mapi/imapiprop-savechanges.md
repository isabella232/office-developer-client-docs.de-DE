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
  
Macht alle Änderungen, die an einem Objekt seit dem letzten Speichervorgang vorgenommen wurden, dauerhaft. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, was mit dem Objekt geschieht, wenn die **IMAPIProp:: SaveChanges** -Methode aufgerufen wird. Die folgenden Flags können festgelegt werden: 
    
NON_EMS_XP_SAVE
  
> Gibt an, dass die Nachricht nicht von einem Microsoft Exchange-Server übermittelt wurde. Dieses Flag sollte in Kombination mit der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode und dem ITEMPROC_FORCE-Flag verwendet werden, um einem PST-Speicher anzuzeigen, dass die Nachricht für die Verarbeitung von Regeln berechtigt ist, bevor der PST-Speicher (Personal Folders) benachrichtigt wird. Überwachen des Clients, dass die Nachricht eingegangen ist. Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf einem Server erstellt werden, der kein Exchange-Server ist, in dem der Exchange-Server bereits Regeln für die Nachricht verarbeitet hätte. 
    
FORCE_SAVE 
  
> Änderungen sollten in das Objekt geschrieben werden, wobei alle vorherigen Änderungen, die an dem Objekt vorgenommen wurden, überschrieben werden und das Objekt geschlossen werden sollte. Die Berechtigung Lese-/Schreibzugriff muss festgelegt werden, damit der Vorgang erfolgreich ausgeführt werden kann. Das FORCE_SAVE-Flag wird verwendet, nachdem ein vorheriger Aufruf von **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben wurde. 
    
KEEP_OPEN_READONLY 
  
> Änderungen sollten zugesichert werden, und das Objekt sollte zum Lesen geöffnet bleiben. Es werden keine weiteren Änderungen vorgenommen. 
    
KEEP_OPEN_READWRITE 
  
> Änderungen sollten zugesichert werden, und das Objekt sollte für Lese-/Schreibzugriff geöffnet bleiben. Dieses Flag wird in der Regel festgelegt, wenn das Objekt zum ersten Mal für Lese-/Schreibzugriff geöffnet wurde. Nachfolgende Änderungen am Objekt sind zulässig. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** , dass SaveChanges erfolgreich zurückgegeben wird, möglicherweise bevor die Änderungen vollständig übernommen wurden. 
    
SPAMFILTER_ONSAVE
  
> Aktiviert die Spamfilterung für eine Nachricht, die gespeichert wird. Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verpflichtung der Änderungen war erfolgreich.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** kann das Objekt nur mit Leseberechtigung öffnen, wenn KEEP_OPEN_READONLY festgelegt ist, oder Lese-/Schreibzugriff Berechtigung, wenn KEEP_OPEN_READWRITE festgelegt ist. Es werden keine Änderungen übernommen. 
    
MAPI_E_OBJECT_CHANGED 
  
> Das Objekt wurde seit dem Öffnen geändert.
    
MAPI_E_OBJECT_DELETED 
  
> Das Objekt wurde seit dem Öffnen gelöscht.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp:: SaveChanges** -Methode macht Änderungen an Eigenschaften für Objekte dauerhaft, die das Transaktionsmodell der Verarbeitung unterstützen, wie Nachrichten, Anlagen, Adressbuchcontainer und Messaging-Benutzerobjekte. Objekte, die keine Transaktionen unterstützen, wie beispielsweise Ordner, Nachrichtenspeicher und Profilabschnitte, nehmen Änderungen permanent vor. Es ist kein **** Aufruf von SaveChanges erforderlich. 
  
Da Dienstanbieter keine Eintrags-ID für Ihre Objekte generieren müssen, bis alle Eigenschaften gespeichert wurden, ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft eines Objekts möglicherweise erst nach der **SaveChanges** -Methode verfügbar. aufgerufen wurde. Einige Anbieter warten, bis das KEEP_OPEN_READONLY-Flag für den **SaveChanges** -Aufruf festgelegt ist. KEEP_OPEN_READONLY gibt an, dass die Änderungen, die im aktuellen Aufruf gespeichert werden sollen, die letzten Änderungen sind, die für das Objekt vorgenommen werden. 
  
In einigen Nachrichtenspeicher Implementierungen werden nicht neu erstellte Nachrichten in einem Ordner angezeigt, bis ein Client die Nachrichten **** Änderungen mithilfe von SaveChanges speichert und die Message-Objekte mithilfe der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode freigibt. Darüber hinaus können einige Objekt Implementierungen eine **PR_ENTRYID** -Eigenschaft für ein neu erstelltes Objekt erst generieren, nachdem **SaveChanges** aufgerufen wurde, und einige können dies nur tun, nachdem **SaveChanges** mithilfe von KEEP_OPEN_READONLY aufgerufen wurde. festgelegt in _ulFlags_.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie das KEEP_OPEN_READONLY-Flag erhalten, haben Sie die Möglichkeit, den Zugriff des Objekts als Lese-/Schreibzugriff zu lassen. Ein Anbieter kann jedoch nie ein Objekt in einem schreibgeschützten Zustand lassen, wenn das KEEP_OPEN_READWRITE-Flag übergeben wird.
  
Wenn ein Client mehrere Anlagen in mehreren Nachrichten speichert, ruft er **** die SaveChanges-Methode für jede Anlage und jede Nachricht auf. Häufig werden Clients MAPI_DEFERRED_ERRORS für jeden dieser Anrufe festlegen, mit Ausnahme des letzten. Sie können entweder mit dem letzten Anruf oder früheren anrufen Fehler zurückgeben. Sie können die Kennzeichnung sogar ignorieren. 
  
Wenn KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Anforderung zur Fehler begärung ignorieren. Wenn MAPI_DEFERRED_ERRORS nicht in _ulFlags_festgelegt ist, kann einer der zuvor verzögerten Fehler für den SaveChanges **** -Aufruf zurückgegeben werden. 
  
Ob ein Remote Transportanbieter eine funktionale Implementierung dieser Methode bereitstellt, ist optional und hängt von anderen Entwurfsentscheidungen in ihrer Implementierung ab. Wenn Sie diese Methode implementieren, tun Sie dies gemäß der Dokumentation hier. Da Ordnerobjekte und Statusobjekte nicht transformiert werden, muss mindestens die Implementierung von SaveChanges durch einen **** Remote Transportanbieter S_OK zurückgeben, ohne dass tatsächlich eine Arbeit ausgeführt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client KEEP_OPEN_READONLY übergibt, die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode aufruft und **** dann SaveChanges erneut aufruft, kann für dieselbe Implementierung ein Fehler auftreten. 
  
Nachdem Sie MAPI_E_NO_ACCESS von einem Aufruf empfangen haben, in dem Sie KEEP_OPEN_READWRITE festgelegt haben, verfügen Sie weiterhin über Lese-/Schreibzugriff für das Objekt. Sie können **SaveChanges** erneut aufrufen, indem Sie entweder das KEEP_OPEN_READONLY-Flag oder keine Flags mit KEEP_OPEN_SUFFIX übergeben. 
  
Ob ein Anbieter das KEEP_OPEN_READWRITE-Flag unterstützt, hängt von der Implementierung des Anbieters ab. 
  
Um anzugeben, dass der einzige Aufruf für das Objekt nach SaveChanges **** ist **IUnknown:: Release**, legen Sie keine Flags für den _ulFlags_ -Parameter. Ein Fehler von **SaveChanges** gibt an, dass die ausstehenden Änderungen nicht dauerhaft vorgenommen werden konnten. Unterschiedliche Anbieter behandeln das Fehlen von Flags für **** den SaveChanges-Aufruf anders. Einige Anbieter behandeln diesen Status genauso wie KEEP_OPEN_READONLY; andere Anbieter interpretieren es genauso wie KEEP_OPEN_READWRITE. Andere Anbieter haben das Objekt jedoch heruntergefahren, wenn Sie keine Flags für den **SaveChanges** -Aufruf erhalten. 
  
Einige Eigenschaften, in der Regel berechnete Eigenschaften, können erst verarbeitet **** werden, wenn Sie SaveChanges aufrufen und in einigen Fällen **Freigeben**.
  
Wenn Sie Massenänderungen vornehmen, wie das Speichern von Anlagen in mehreren Nachrichten, verschieben Sie die Fehlerverarbeitung, indem Sie das MAPI_DEFERRED_ERRORS-Flag in _ulFlags_festlegen. Wenn Sie mehrere Anlagen in mehreren Nachrichten speichern, führen **** Sie einen SaveChanges-Aufruf jeder Anlage und einen **SaveChanges** -Aufruf jeder Nachricht aus. Legen Sie das MAPI_DEFERRED_ERRORS-Flag für jeden Anlagen Aufruf und für alle Nachrichten mit Ausnahme des letzten fest. 
  
Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgibt, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde. Wenn dies der Fall ist, warnen Sie den Benutzer, der entweder die Änderung der Änderungen überschreiben oder das Objekt an einer anderen Stelle speichern kann. Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer, Ihnen die Möglichkeit zu geben, das Objekt an einem anderen Speicherort zu speichern. 
  
Sie können **SaveChanges** nicht mit dem FORCE_SAVE-Flag für ein geöffnetes Objekt aufrufen, das gelöscht wurde. 
  
Wenn **SaveChanges** einen Fehler zurückgibt, bleibt das Objekt, dessen Änderungen gespeichert werden sollen, unabhängig von den im _ulFlags_ -Parameter festgelegten Flags geöffnet. 
  
> [!IMPORTANT]
> Die _ulFlags_ NON_EMS_XP_SAVE und SPAMFILTER_ONSAVE sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie Sie mit den folgenden Werten zu Ihrem Code hinzufügen: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Kanonische PidTagEntryId-Eigenschaft](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Speichern von MAPI-Eigenschaften](saving-mapi-properties.md)

